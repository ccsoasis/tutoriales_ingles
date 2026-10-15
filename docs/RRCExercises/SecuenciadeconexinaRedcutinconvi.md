---
tags:
- cutin
- power vs slip
- power vs slip graph
---

# Grid connection sequence (cutin) with wind above the nominal

!!! tip "🎯 Cutin with wind above the Nominal"
    ***Objective:*** Compare the cutin sequence with high wind (15 m/s) with the low wind one, observing how the Controller uses the Pitch to guarantee a constant acceleration slope during the Softstarter connection, and how the RRC control comes into action in production.
    ***What to observe:*** The Pitch evolution during the final cutin phases, the instant the DutyCycle stops being 100% and the operating point in "Power vs Slip" (point B).
    💡 With high wind, the stable operating point is point B. Why does it not follow the red line as with low wind?

!!! warning "❓ Guiding questions"
    1. Why does the Controller modify the Pitch so that the acceleration slope is constant in the last instants before the connection, regardless of the wind?
    2. Comparing the 6 m/s and 15 m/s cutin records, in which signal do you notice the most striking difference? Is it the Pitch, the PWM or the RPMs?
    3. With 15 m/s wind in stable production, what is the DutyCycle value? Is the operating point on the red line or at point B?

In this practice the objective is to repeat the [Grid connection sequence (cutin) with wind below the nominal](SecuenciadeconexinalaRedcutincon.md) practice but with a wind above the nominal, and observe the differences between the key variable evolutions.

- 1.In "Control Terminal" press "STOP" if the wind turbine is in production, and wait for it to stop.

- 2.In "SynopticWindNacelle" set the wind to **15 m/s**.

- 3.Click on the "Manual STOP" incident box, in "Control Terminal".

- 4.In "Control Terminal" make sure the "Power vs Slip" synoptic is visible. Press the "*Power vs Slip Graph*" menu option.

- 5.In "Control Terminal" press the "START" button.

- 6.Observe the signal evolution in the "General" recorder, until the production entry (cutin) occurs. You must have a record similar to the one in the following figure.

![](<lib/Cutin con 15 ms.jpg>)

Comments:

If you compare with the graph obtained in the [Grid connection sequence (cutin) with wind below the nominal](SecuenciadeconexinalaRedcutincon.md) practice, you will be able to observe that the Controller modifies the Pitch value so that in the last part of the rpms evolution before the connection, the slope is fixed, regardless of the wind. This is a requirement of the grid connection mechanism (Softstarter, explained in the Two-Speed and Active Stall wind turbine tutorial).

| ![](<lib/Detalle cutin a 6.jpg>) | ![](<lib/Detalle cutin a 15.jpg>) |
|---|---|
| Cutin at 6 m/s | Cutin at 15 m/s |
