---
tags:
- generated power
- slip
- SlipTarget
---

# Power vs Rotor Slip

This menu option presents the "*Power vs Rotor Slip*" synoptic.

![](<lib/Pot vs Deslizamiento viento mayor que nominal.jpg>) Fig 1

In this synoptic the current wind turbine operating point (yellow point) is presented in relation to the *generated power* and the *slip*. See description in [Rotor Resistance control algorithm](AlgoritmodecontroldelaResistenci.md).

![](<lib/Pot vs Desliz con puntos indicados.jpg>) Fig 2

The *rotor resistance* and *pitch angle* control systems try to keep the operating point always on the A-D-C-E segments. And when the wind is above the nominal, and the steady state is reached, both force the operating point to be on point B.

The **D-C** line corresponds to the desired power that is modifiable in the "[Desired Active Power](ControlTerminal.md)" indicator.

The red line defined by the **A-D** points corresponds to the IGBT continuous conduction case. The C-E section is on the line defined by the A and C points, which corresponds to the situation in which the IGBT never conducts.

Point B is regulated by the *Controller*.*SlipTarget* parameter, which has a default value of 4% (0.04).
