---
tags:
- cutout
- states
- events
- normal stop
---

# In the disconnection process (Cutout)

!!! tip "🎯 State machine — Cut-out"
    ***Objective:*** Understand the protection sequence that leads to the stop when the wind exceeds a limit (cut-out).
    ***What to observe:*** States prior to the stop, trigger event, protection actions and safe final state.
    ***What to note:*** Approximate threshold, final state, and whether there is a reset or hysteresis condition.
    💡 distinguish between power limitation and safety stop.

!!! warning "❓ Guiding questions"
    1. Which states does the state machine go through from production to complete stop?
    2. In which state does power export to the grid stop?

In this practice the objective is to explore the evolution of the **states** and **events** that occur during a *normal stop* (*cutout*).

Repeat the experiment of the [Observation of the reaction to the "STOP" command](Cutout.md) practice. Make sure you have a recorder open with the "RPMs + Pitch + State Machines" panel, with "Seconds per pixel xx" at 200 ms.

Track in the state machine graphs that you have in [Internal control State Machines](../DSASTutorial/StateEventsDiagramsoftheimplemen.md).

![](<lib/DSAS cutout a 6 y evolucion maquinas estado.jpg>)
