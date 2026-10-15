# With slow changes

!!! tip "🎯 Low wind gusts with slow changes"
    ***Objective:*** Observe how the wind turbine responds to "Standard120x4" type gusts with low base wind (7–10 m/s), understanding why the Pitch practically does not change and how the B2B manages the Power Train kinetic energy.
    ***What to observe:*** The evolution of the working point in "Operational Curves", the Cp response to the gust and the B2B behavior to facilitate the Power Train acceleration towards the new MPPT point.
    💡 During the gust, the B2B temporarily reduces the power sent to the grid. Why? What objective does it pursue?

!!! warning "❓ Guiding questions"
    1. With a base wind of 7 m/s and a "Standard120x4" gust (peak of 11 m/s), does the Pitch change? Why not, if the wind exceeds point C of the operational curve?
    2. Why does the B2B temporarily reduce the power sent to the grid during the rising edge of the gust?
    3. What difference do you observe in the response when the base wind is 9 m/s vs 7 m/s? What is it due to?

In this practice the wind turbine behavior is explored when the existing wind is low and a "slow" gust is received.

Put the wind turbine into production (see [Evolution in the Power vs rpms plane](CPArranqueVientoMenorSincPotRPMs.md))

- Make sure the simulator is in "*Execution*" (Synoptic "*Execution ..*" --> "*Run*" or "*Continue*")

- Set the wind to 7 m/s.

- Make visible a StripRecorder with the Panel "*Cutin + Cutout + Production: Panel to monitor cutin and cutout operations*".

- Check that there are no unrecognized entries in "*Open incidents*" (synoptic "*Control Terminal ..*.").

- Press the START button.

- Observe the evolution of the two power indicators (mechanical and electrical) in the "Power vs RPMs" panel in the "*Operational curves ..*" synoptic (In the "*Control Terminal ..*" synoptic --> "*Work Curves*"). Also observe the evolution of the *Cp* point in the lower left panel.

- Wait for the two power indicators to stabilize. Check that the generator stator connection indicator is activated (synoptic "*Control Terminal ...*" indicator "*Contact. Stator*").

- Apply a "Standard120x4" type gust and observe the evolution of the indicators in the 4 panels of the "*Operational Curves*" synoptic (In "*Control Terminal ..*." press "*Work Curves*") especially the Pitch panel (bottom right).

You will obtain a graph similar to the following.

![](<lib/WindGust 120x4 sobre 7 m-s.jpg>)

You will be able to verify the following:

- Although the wind reaches 11 m/s, the Pitch value practically does not change.

- The rpms evolution follows the wind evolution quite well.

- The evolution of the Mechanical Power extracted from the wind (*Nacelle.DriveTrain.ActualWindPowerOut*) also follows the wind evolution quite well.

- The evolution of the Electrical Power delivered to the grid (*Nacelle.DFIGB2B.GridActivePower*) follows the wind, but with some strange changes.

## Explanation

With 7 m/s wind the stationary working point is within the MPPT region (maximum wind power algorithm). Therefore the Pitch value is the "optimum" (0º).

When the wind changes from 7 to 8 m/s we can observe the following:

![](<lib/DFIG Evolucion 7 a 8 m-s.jpg>)

When the wind goes from 7 to 8 m/s the working point goes from the initial point to point "X", located on the "8 m/s" green curve. However, the controller must follow the MPPT Algorithm that guarantees the extraction of optimal energy from the wind, which implies moving the operating point to "F", also on the "8 m/s" green curve, but with more revolutions per minute, and a bit more power (the optimal power of 8 m/s). If the B2B transferred the "new" mechanical energy (point "X") to the grid, there would be no energy available to accelerate the transmission, so "X" would become the new "stable" working point. Instead, the B2B not only does not use the extra power of point "X", but even reduces the existing power transfer to the grid, so that there is more energy available to accelerate the transmission in order to reach the rpms of point F.
