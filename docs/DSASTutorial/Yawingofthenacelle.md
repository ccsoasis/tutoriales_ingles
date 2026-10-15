---
tags:
- yawing operation
- Parameter.ControllerYawing.MaxCableTwistBeforeCutin
- cutin
- minimum wind to proceed with cable unwinding
- maximum number of power cable turns before starting cut-in
---

# Yaw and Power Cable unwinding control algorithms

The Controller contains an independent process, specific for the functions related to:

- Nacelle yawing to the wind direction.

- Power cable unwinding.

The implemented algorithm takes into account the concepts of:

- *'maximum number of power cable turns before starting the connection* (cutin)'.

- *'maximum number of power cable turns'*. This value is not equal to the maximum limit value set by the limit switch associated with these cables, which is controlled by the parameter "*Parameter.NacelleYawing.MaxCableTwist*", with an initial value of 3.5 turns.

- *'minimum wind to proceed with cable unwinding'*.

In addition, this process takes into account the current operating mode: "Manual" and "Automatic". See [Modes](Modes.md).

For the power cable unwinding process, it is necessary to first disconnect the wind turbine from the grid (cutout), using the normal protocol (without imposing short response times).

When the cable turns number is within the first turn, the Controller starts, without any operator intervention, the grid connection process (cutin).

The following graph shows the relationship between the mentioned parameters and the states.

![](<lib/Grafico numero vueltas cables.png>)

- If the wind turbine is in the grid connection (cutin) phase and the turns number is greater than 1.5, then it first starts the unwinding process, before continuing.

- If the wind turbine is in Production and the turns number exceeds 2.5, the Controller starts a grid disconnection process, followed by unwinding and grid connection.

- In any case, for example, using a manual control for the nacelle yawing, if the turns number reaches 3.5 the Controller stops the nacelle rotation.
