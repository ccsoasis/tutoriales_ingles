---
tags:
- synchronous speed
---

# Wind turbine start-up (cutin) with wind below the nominal

!!! tip "🎯 Start-up with wind below the Nominal"
    ***Section objective:*** Explore the DFIG behavior during start-up (cutin) when the wind is below the nominal (~11 m/s).
    ***What to observe:*** The operational curve (Power vs RPMs panel), the evolution towards the MPPT point and the behavior difference depending on whether the wind is higher or lower than the synchronism one (~7.8 m/s).
    💡 Notice whether the stable operating point remains on the Maximum Power curve (blue line).

In this series of experiments we will explore the behavior of a DFIG when the wind is below the nominal.

We will distinguish two cases, depending on the wind value: below or above the wind that makes the Generator shaft rotate at its *synchronous speed*. This point can be seen using the "*Operational curves for Variable Speed Wind Turbines*" synoptic, accessed through the "*Work curves*" menu of the "*Control Terminal*" synoptic.

In the "*Power vs rpms*" graph (upper left) that point can be seen at the intersection of the vertical corresponding to "rpms = 1" (in pu's) and the work curve (red line). The value of this wind, in this case, is around 7.8 m/s.

![](<lib/Curvas operaciones Potencia vs rpms parado.jpg>)
