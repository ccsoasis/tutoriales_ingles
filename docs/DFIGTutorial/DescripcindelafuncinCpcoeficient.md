---
tags:
- TSR
- tip speed ratio
---

# Description of the Cp function (aerodynamic coefficient)

To achieve the objective of obtaining the greatest power from the existing wind, we have to control the aerodynamic Coefficient of the blades (Cp function) for that wind. The shape of the Cp function depends on the blade geometry, and, given a certain geometry, the value depends on three variables:

1. The wind speed.

2. The blade rotation speed.

3. The blade attack angle (pitch).

Fortunately these three variables can be reduced to two by using the artifice of a variable that relates the wind speed with the blade rotation speed. This variable is known as TSR (from Tip Speed Ratio: ratio between the linear speed of the blade tip and the wind speed, which is assumed perpendicular to the blade rotation plane).

Its definition is:

**TSR = 2 \*** **π** **\* BladeRadius \* (BladeRotationSpeed** <sub>**rpms**</sub>**)/60) / WindSpeed**

In this way the Cp function remains dependent on two variables: the TSR and the Pitch:

**Cp**(***TSR***,***Pitch***)

In the case of the DFIG Simulator, a blade type is used whose Cp (TSR, Pitch) function is presented in several 3D and 2D forms. See the following.

![](<lib/Vista 3D desde la izquierda.jpg>)

![](<lib/Vista 3D desde la derecha.jpg>)

![](<lib/Vista cenital con isozonas.jpg>)

The following figure shows the 2D representation that is used as a reference in the graph where the evolution of the Cp value as a function of the TSR and Pitch values is shown (black circular symbol).

![](<lib/Vista Cp en MPPT en espaol.png>)

See [Aerodynamic coefficient: Cp function](CoeficienteaerodinmicofuncinCp.md).
