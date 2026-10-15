---
tags:
- coupler
- cutin
- cutout
- pitch
- aerodynamic brake
- stop
- control terminal
- thyristor bypass contactors
---

# Observation of the reaction to the "STOP" command

!!! tip "🎯 Cut-out (stop due to high wind)"
    ***Objective:*** Identify the safety condition that causes the high wind stop and describe the stop sequence.
    ***What to observe:*** Wind speed, alarms/protections, state changes and control actuation.
    ***What to note:*** Approximate trigger threshold, final system state and conditions to operate again.
    💡 check whether the turbine enters power limitation first.

!!! warning "❓ Guiding questions"
    1. How much time elapses from pressing **Stop** (grid connection and in production) until the blades stop?
    2. In the same situation, how much time elapses until there is no longer power exported to the grid?

In this practice the objective is to observe the important signal evolution when the generator is disconnected from the grid (*cutout*). The cutout operation can be triggered manually from the "Control Terminal" with the "**STOP**" button.

The cutout operation is triggered when the wind turbine is in production (with the generator connected to the grid) and the "**STOP**" button is pressed in the "*Control Terminal*" synoptic, and ends with the generator grid disconnection in an orderly way.

The main characteristic is the pitch control so that the generated power decreases practically to 0 before deactivating the *Thyristor Bypass Contactors*. See the following figure. Note that the recorder sampling speed ("Seconds per pixel xx") has been placed at 200 ms.

![](<lib/Parada-a-6-conregistrador-200ms.jpg>)
