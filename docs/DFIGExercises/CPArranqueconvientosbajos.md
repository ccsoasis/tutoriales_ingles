---
tags:
- synchronous speed
---

# Wind turbine start-up (cutin) with wind below the nominal

!!! tip "🎯 Start-up with wind below the Nominal"
***Section objective:*** Explore DFIG behavior during start-up (cutin) when wind is below the nominal (~11 m/s).

***What to observe:*** The operational curve (Power vs RPMs panel), the evolution toward the MPPT point, and how behavior differs depending on whether the wind is above or below the synchronism wind speed (~7.8 m/s).
    💡 Notice whether the stable operating point remains on the Maximum Power curve (blue line).

In this series of experiments, we will explore DFIG behavior when the wind is below nominal.

We will distinguish two cases, depending on the wind value: below or above the wind that makes the Generator shaft rotate at its *synchronous speed*. This point can be seen using the "*Operational curves for Variable Speed Wind Turbines*" synoptic, accessed through the "*Visualize Working curves*" menu of the "*Control Terminal*" synoptic.

In the "*Power vs rpms*" graph (upper left), that point appears at the intersection of the vertical line corresponding to "rpms = 1" (in pu's) and the power curve (red line). The value of this wind, in this case, is around 7.8 m/s.

![](<lib/Curvas operaciones Potencia vs rpms parado.jpg>)
