---
tags:
- cutin
---

# In the connection process (Cutin)

!!! tip "🎯 State machine — Cut-in"
    ***Objective:*** Identify the state sequence that leads from stop to operation entry (cut-in).
    ***What to observe:*** Current state, state changes during the start, permissions and variables associated with the start.
    ***What to note:*** Order of states and the condition that causes each change (wind, permission, time, setpoint).
    💡 look for the point where the system passes from preparation to effective generation.

Repeat the [Set the conditions for the Production entry with low wind to occur](CutinVientoBajo.md) practice but make sure you have a recorder open with the "*RPMs + Pitch + State Machines*" panel. With the states and events description you have in [Internal control State Machines](../DSASTutorial/StateEventsDiagramsoftheimplemen.md) track the evolution of these states.

![](<lib/DSAS Evolucion de estados en cutin a 6 ms.jpg>)
