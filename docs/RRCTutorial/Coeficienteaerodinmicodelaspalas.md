# Blade aerodynamic coefficient

The aerodynamic coefficient is a function that characterizes the force that makes the blades rotate in a wind turbine, and therefore the extractable wind power.

It depends on two variables:

- the blade attack angle with respect to the blade rotation plane (**Pitch**)

- the relationship between the blade tip linear speed with respect to the wind incident on the blade rotation plane: (**TSR**)

TSR = 2 \* π \* BladeRadius \* (BladeRotationSpeed(rpms)/60) / Wind (m/s)

In the following figure the *Wind* is shown as "Effective wind", assuming it comes from the upper part of the figure. The blade end speed (2 \* π \* BladeRadius \* (BladeRotationSpeed(rpms)/60)) corresponds to the "Rotational wind" vector. The TSR corresponds to the tangent of the angle defined by the "Total wind" and the horizontal.

![](<lib/Panel de viento.jpg>) Fig 1

In the following figures several views of this function are shown.

![](<lib/Vista 3D desde la izquierda.jpg>)Fig 2

![](<lib/Vista cenital con isozonas.jpg>)Fig 3

![](<lib/Vista 3D desde la derecha.jpg>)Fig 4

In Fig 3 it can be seen that there is a maximum Cp value that occurs with a TSR of 8 (approx) and with a Pitch of 0º.
