---
tags:
- generator
- rpms
- rotor speed
- VCU
- HCU
- overspeed
---

# Speed indicators in the Power Train

The *SynopticDriveTrain* also contains two sets of rotation speed indicators of the Power Train ("Rotor rpms") and of the Generator rotor shaft ("*Generator rpms*"). Both sets are made up of a linear indicator with the ability to switch to "Force" mode (F6) and a clock.

![](<lib/DriveTrain RPMs.jpg>)

In the clocks the "operating zones" discussed in [Implications for the Power Train](ImplicacionesparaelTrendePotenci.md) are also indicated. The color code is the following.

![](<lib/Regiones en RPMs.png>)

The VCU and HCU signals are digital signals related to the Power Train and Generator rotor revolutions that indicate whether those values exceed or not a certain threshold. These signals are used by the Controller to start emergency stops that avoid the Power Train racing.

The following scheme shows the relationships between the signals associated with the Power Train and Generator revolutions, and the VCU and HCU signals.

![](<lib/Esquema RPMs.png>)

With this structure of indicators and connections, the creation of "anomalous" situations that allow knowing the Controller reactions is facilitated.
