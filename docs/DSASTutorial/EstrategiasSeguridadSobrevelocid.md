---
tags:
- aerodynamic brake
- brake
- fail-safe
- HCU
- VCU
- safety
- wind brake
- hard brake
---

# Overspeed safety strategies

One of the critical safety problems in wind turbines is the overspeed prevention. Typically, the way to guarantee this safety consists of:

- Reduction of the energy extracted from the wind, modifying the blade pitch angle. This is known as *'wind brake'* (*air braking*).

- Reduction of the power train kinetic energy using the hydraulic brake, known as *'hard brake'* (*hard braking*).

If the power train rpms evolution is such that certain limits are exceeded (which are above the 'normal production speeds'), the Controller tries to reduce them using the previous procedures: if it does not succeed, the wind turbine has physical devices that try to act, first, on the electric generator shaft, and if this mechanism fails, on the blade shaft. These two procedures cause important wind turbine deteriorations, so they are only used in extreme cases, in which it is preferable to cause these damages than personal or object damages outside the wind turbine occurring.

In the case of the wind turbine taken as reference for this simulator, the generator shaft overspeed detector *Nacelle.GeneratorSpeedVCU* is activated at around 1803 rpms (in production the maximum value is around 1520 rpms), and is a centrifugal sensor.

If the power train exceeds this speed, 3 other sensors are used, located in each of the blades, which are activated if the blade speed exceeds 25 rpms (in production this value is below 20 rpms).
