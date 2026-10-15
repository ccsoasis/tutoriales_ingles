---
tags:
- DriveTrain
- desired power
---

# Rotor Resistance control algorithm

The rotor resistance control algorithm takes into account the following concepts:

- 1.The rotor resistance is made up of the rotor winding's own resistance plus an external resistance (see scheme in [Control electronic circuit](Circuitoelectrnicodelcontrol.md)).

- 2.There is a *desired power* value that can be regulated to a value below the Generator Maximum Power. In the following figure 1 it corresponds to the horizontal line D-C (*Pref.n*).

- 3.While the power extracted from the wind is below the *desired power*, the rotor resistance will be the minimum; that is, the external resistance will be the minimum. This means that, in this case, the operating point will be on the A-D line, which corresponds to the squirrel-cage generator case.

- 4.There is a Maximum Resistance of the Rotor winding, which corresponds to the A-C line.

- 5.The generated power will therefore be determined by the segments: A-D, D-C and to the right of C on the A-C line.

![](<lib/RRC algoritmo de control.jpg>)

Fig 1.

In figure 1, the ordinates correspond to the generated power relative (*Pref*) to the maximum *desired* power value (*Pref.n*).

The algorithm to use is a control loop that tries to make the Power Train operating point (its speed) be related to the generated power so that it *tries* to always be on the A-D, D-C segments and to the right of C on the A-C line.

An explanation of this control is illustrated in Fig 1.

Let us suppose we have a wind below the nominal: the operating point would be point P, located on the A-D segment. If the wind rises, point P will move upwards, if it decreases downwards, always on the A-D segment.

If the wind rises above the nominal, the operating point will be a rest point, fixed at point B. If, being at point B, the wind rises, the operating point will move to point F, on the A-B line, which corresponds to the current total resistance, which we assume does not change instantaneously. The algorithm will change said resistance, as fast as it can, so that the operating point becomes M, on the D-C segment. Since the control mechanism is electronic acting on a fast-response electronic device (see [Control electronic circuit](Circuitoelectrnicodelcontrol.md)) this change is very fast (milliseconds).

Meanwhile, the Pitch control algorithm, which runs in parallel, will adjust the Pitch again so that the wind mechanical torque becomes the one corresponding to point B again. However, since this algorithm acts on heavy mechanical elements (the blades), it is considerably slower. As a consequence it is possible, depending on the wind change speed, that the Power Train keeps racing to point I and subsequently to point N.

When the Pitch mechanism starts, increasing it (see [Cp](Coeficienteaerodinmicodelaspalas.md)), the mechanical torque decreases, and the operating point movement is similar to the one described before, but in the opposite direction. If we start from point M, it will go to point H and then to B, which is the objective.

As seen, this equipment uses two independent controls to maintain the desired operating point.

In the B-F-M and M-I-N transitions the Power Train kinetic energy increases, since the final points M and N correspond to rotation speeds higher than the initial ones (B and M). These kinetic energy increases are the ones that absorb the pitch mechanism inability to adequately follow (that is, in time) the wind changes.

In the [simulator](PotenciavsDeslizamientodelRotor.md) the Fig 1 graph is presented, where the operating point is superimposed at each moment (in <mark>yellow</mark>). In figure 2 this point is shown on the "*target point*" in <mark>red</mark>.

![](<lib/Pot vs Deslizamiento viento mayor que nominal.jpg>)

Fig 2
