---
tags:
- orientation operation
- turn motors
- wind direction
---

# Wind direction change effects

!!! tip "🎯 Wind direction change"
    ***Objective:*** Understand how a wind direction change causes an orientation correction (yaw) to recover alignment.
    ***What to observe:*** Wind direction, alignment error, yaw state/order and system response.
    ***What to note:*** When the correction begins, how much it corrects and whether there is a dead zone (minimum threshold).
    💡 identify whether the yaw acts continuously or in steps.

!!! warning "❓ Guiding questions"
    1. The wind vane signal is analog: what indicates that its value is continuously the maximum or the minimum?

These practices are to study the implications of the wind direction change and the mechanisms to keep the Nacelle orientation facing the wind.

The first is to check the mechanism that makes the Nacelle turn. Consult [Orientation mechanism (yaw)](../DSASTutorial/SistemadeFrenos1.md) about the devices the wind turbine has for these turns.

The activation of the *turn motors* (*yaw* in English) is carried out by the Controller, taking into account several concepts:

- The number of power cable turns.

- The wind vane signal.

- Whether the operation mode at that moment is "*Manual*" or "*Automatic*".

There is a limitation imposed by the maximum number of power cable turns: the Controller prevents the activation of the turn motor that tries to exceed this value.
