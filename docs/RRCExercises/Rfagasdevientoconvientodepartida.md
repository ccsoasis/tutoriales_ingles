# Wind gusts with starting wind above the nominal

!!! tip "🎯 Gusts with starting wind above the nominal"
    ***Objective:*** Observe the response to slow and fast gusts when the starting wind is already above the nominal (15 m/s), and check that in this case the Pitch mechanism (and not the RRC control) is the main responsible for keeping the power constant.
    ***What to observe:*** The constancy of the generated power against both gust types, the small DutyCycle and RPMs variations, and the Pitch actuation to follow the wind profile.
    💡 With high starting wind, the Pitch is the main actor. Why does the DutyCycle vary only slightly?

!!! warning "❓ Guiding questions"
    1. Does the generated power remain constant both with the slow gust (StandardGust120x4) and the fast one (StandardGust60x10)? In which of the two does it vary more?
    2. Does the DutyCycle (PWM) vary significantly during the gusts? What does that indicate about the RRC control role in this regime?
    3. Compare the behavior with the "Gusts with wind below the nominal" practice: what is the main difference in the generated power shape?

In this practice the objective is to observe the wind turbine reaction to gusts, both slow and fast, and observe the key variable evolution.

Follow the sequence:

- 1.Press STOP.

- 2.Change the wind to 15 m/s.

- 3.Choose the "*StandardGust120x4*" gust type and force it. Wait for it to end.

- 4.Choose the "*StandardGust60x10*" gust type and wait for it to end.

You must obtain a graph similar to the one in the following figure in the "General" recorder.

![](<lib/Rafagas sucesivas a 15 ms.jpg>)

## Comments:

Note that both in the slow gust and the fast one the generated power remains constant. There are only small shaft rpms variations, corresponding to small IGBT DutyCycle (PWM) variations.

This behavior derives from having a Pitch mechanism that is capable of following the wind changes of these two gust types.
