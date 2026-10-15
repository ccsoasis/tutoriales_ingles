---
tags:
- states
- events
---

# During the Generator connection change processes (Small to Large and vice versa)

!!! tip "🎯 State machine — Change 1000→1500"
    ***Objective:*** See how the state machine represents the mode change associated with the 1000 to 1500 jump.
    ***What to observe:*** Origin state, destination state and the condition/threshold that triggers the change.
    ***What to note:*** State sequence and visible effects on power/speed during the transition.
    💡 note whether the change is direct or passes through intermediate preparation states.

In this practice the objective is to explore the evolution of the **states** and **events** that occur during the electrical generator connection mode change processes.

Repeat the experiment of the [Being in production, wind modification to change the Generator connection from Small to Large](Cambiode1000a1500.md) and [Being in production, wind modification to change the Generator connection from Large to Small](Cambiode1500a1000.md) practices. Make sure you have a recorder open with the "*RPMs + Pitch + State Machines*" panel, with "*Seconds per pixel xx*" at 200 ms.

Track in the state machine graphs that you have in [Internal control State Machines](../DSASTutorial/StateEventsDiagramsoftheimplemen.md).

![](<lib/DSAS estados de small a large.jpg>)
