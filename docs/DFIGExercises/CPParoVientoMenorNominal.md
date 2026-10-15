# Stop with wind below the Nominal

!!! tip "🎯 Stop with wind below the Nominal"
    ***Objective:*** Analyze the sequence of events during the ordered stop (cutout) of the wind turbine with low wind (~7 m/s) and understand the Pitch and B2B role during the disconnection.
    ***What to observe:*** The Pitch evolution (towards 90°), the mechanical power (which becomes negative), the electrical power sent to the grid and the RPMs until the total stop.
    💡 Why does the electrical power continue a few instants after the mechanical power becomes negative?

!!! warning "❓ Guiding questions"
    1. How long does the Pitch take to reach 90° (feathered position) from the moment STOP is pressed?
    2. Why does the B2B continue sending power to the grid during the initial seconds of the stop, even when the Pitch is already changing?
    3. At what RPMs speed does the B2B stop sending power to the grid? What technical limit of the converter determines that moment?

In this practice the signal evolution during the stop process is analyzed. To do so we set the initial conditions as in the practice [Evolution of key variables](CPArranqueVientoMenorSincVarClav.md).

- Make sure the wind turbine is in production, with a low wind, e.g., 7 m/s.

- Make sure a StripRecorder with the panel "*Cutin + Cutout + Production: Panel to monitor cutin and cutout operations*" is visible.  
We will focus the observation on the following panel signals:

- In this situation press the STOP button in the "Control Terminal ..." synoptic and observe the evolution of these signals. You must obtain a graph similar to the one in the following figure.

![](<lib/DFIG Cutout a 7.jpg>)

## Explanation

The Power Train comes to a total stop shortly after the power delivered to the grid drops to 0, which occurs after the mechanical power reaches a negative value.

The DriveTrain arrives to stop after the Electric Power drops to 0, and that happens after the Mechanical Power reaches 0.

The sequence is:

1. When the Controller receives the STOP command, it sets the Pitch at a value such that the Cp goes from positive (pushing the Power Train) to negative (braking the Power Train), this value is typically the "feathered" one (90º).

2. This operation takes about 17 seconds, since the real Pitch takes a few seconds to follow the desired Pitch (90º).

3. In the initial seconds until the mechanical power contribution becomes negative, there is kinetic energy that is used by the B2B to send power to the grid. This functionality helps braking the Power Train further.

4. When the Power Train rpms drop below those corresponding to the lower frequency limit at which the B2B can operate, it ceases to send power to the grid, which becomes 0.

5. At that moment it is assumed that the Pitch mechanism makes the Cp sufficiently negative to make the remaining kinetic energy still in the Power Train serve to "drive" the wind, braking it in that way.
