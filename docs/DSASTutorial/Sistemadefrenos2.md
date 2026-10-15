---
tags:
- vibrations
- tower vibrations
---

# Tower vibration sensor simulation

The Tower has a vibration sensor. It is of 'pendulum' type, that is, it gives a digital output that becomes active when the pendulum mass touches a ring that defines the maximum tolerated limit for the oscillations.

This signal is simulated through the button titled **'Tower vibrations'**.

![](<lib/Indicador vibraciones torre.jpg>)

The Controller takes it into account only when the time this signal remains 'active' is at least the time specified in this parameter. In the simulator case this parameter is set to 2 seconds.

When this signal is activated and is maintained for a certain time, the Controller starts an immediate stop, using even the hydraulic brake.
