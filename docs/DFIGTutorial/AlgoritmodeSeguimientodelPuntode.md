---
tags:
- MPPT
- maximum power point tracking
- Cp
- TSR
- power train
---

# Maximum Power Point Tracking algorithm (Maximum Power Point Tracking)

The Maximum Power Point Tracking (MPPT) algorithm derives from the study of the aerodynamic response of the blades with respect to their parameters and the Power Train operating conditions. As described in [Description of the Cp function (aerodynamic coefficient)](DescripcindelafuncinCpcoeficient.md) and as can be observed from the 3D views, there is a line that would be the "mountain ridge" that gives the maximum value of Cp.

On the other hand, it is also observed that there is a value, or range of TSR values, where the absolute maximum value of this Cp is concentrated. A representation of the maximum Cp value for a certain TSR value, for the blade used in the DFIG Simulator, is shown in the following figure.

![](<lib/Cp vs TSR for MPPT.jpg>)

Figure Cp max vs TSR

It can be seen that this Cpmax is maximum (that is, the absolute maximum) for a TSR value around 8. A clear conclusion is that **we must make our blade operate so that it is always at TSR=8**, regardless of the wind value. Remembering that the TSR relates the wind with the blade rotation speed and their radius, the previous statement implies that, given a wind, **there is a blade rotation speed that gives us a maximum exploitation of the energy of that wind**, and it is given by the following formula (TSRmax corresponds to 8 in this case):

**OptimalRotationSpeed** <sub>**optima**</sub> **(Wind) = Wind \* TSRmax / (2 \*** **π** **\* BladeRadius)**

Logically this implies that the Pitch must be controlled so that, for the value TSR = TSRmax and the given wind, the Cp value is the maximum possible. See [Power and Pitch vs Wind](DFIGWTTCPotenciaPitchvsViento.md).

As a result of these conditions to remain in MPPT mode, the power obtainable from the wind is proportional to the square of the blade Rotation Speed. See [Implications for the Power Train](ImplicacionesparaelTrendePotenci.md).

For a theoretical discussion on this topic see [Reference list](Listadereferencias.md) 1, section 4.4.
