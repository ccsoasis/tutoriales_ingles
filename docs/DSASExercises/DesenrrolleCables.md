---
tags:
- ControllerYawing.MaxCableTwist
- ControllerYawing.MaxCableTwistBeforeCutin
- cutin + cutout + production
---

# Power cable unwinding

!!! tip "🎯 Cable unwinding"
    ***Objective:*** Understand why it is necessary to control the cable twisting in the orientation (yaw).
    ***What to observe:*** Accumulated yaw position and event that activates the unwinding.
    ***What to note:*** Condition that triggers the correction and system behavior during the process.
    💡 relate repeated orientation changes with turn accumulation in the wiring.

The objective of this practice is to check the power cable unwinding treatment. Read in [Orientation control and Power Cable unwinding algorithms](../DSASTutorial/Yawingofthenacelle.md) the foundation of the expected behaviors.

The concepts to check are the following:

- 1.If the wind direction keeps changing **while the generator is connected to the grid** (in production), the Controller monitors the number of power cable turns: if it reaches the value indicated by the "*ControllerYawing.MaxCableTwist*" parameter (by default, 2.5), the Controller starts an unwinding process, which implies first disconnecting the generator from the grid (cutout), and at the end reconnecting it (cutin).

- 2.If the generator is disconnected from the grid and a grid connection condition occurs (cutin), either because the wind has risen to the sufficient level, or because the operator has given the "START" order, and the number of power cable turns is higher than the "*ControllerYawing.MaxCableTwistBeforeCutin*" parameter value (by default, 1.5), then the Controller starts the unwinding process, and then continues with the connection process (cutin).

For 1):

- Make sure the generator is connected to the grid (in production)

- Keep changing the wind direction in the same direction, until the 2.5 power cable turn limit is reached. To change the wind direction, in the "SynopticWindNacelle" synoptic, "Wind direction" indicator, click with the mouse on the value part (white background), and use the "Page Up", "Page Down", "Up arrow" and "Down arrow" keys, softly (one press per second, for example) and observe how the Nacelle orientation 'follows' the new wind direction value.

- Observe that when the new orientation makes the number of power cable turns exceed 2.4, the Controller will start the generator grid disconnection process (cutout) and will proceed to turn the Nacelle in the direction that makes the turns decrease, until this value is within 0.5 turns.

For 2):

- Make sure the generator is disconnected from the grid (stopped). Press "STOP" if necessary and wait.

- Using one of the "Manual turn" buttons in the "Control Terminal" synoptic force the turn, always in the same direction, until the number of power cable turns is above 1.5.

- Make sure there are no open incidents, apart from "Manual STOP". Click on the "Ok" column of this incident, and press "START".

- Observe that the Nacelle does not look for the wind direction, but begins the cable unwinding. When the turns are in the 0.5 range (in absolute value), it starts the orientation and generator grid connection operation.

In this practice you can use two recorders, one with the "*Yawing*" panel and another with the "*Cutin + Cutout + Production*" panel to observe the pertinent signal evolution.
