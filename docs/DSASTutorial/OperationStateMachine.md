---
tags:
- connection
- grid disconnection
- safety
---

# Operation State Machine

The following figure shows the states (squares) and events (arrows) of the Operation State machine.

This programming is responsible for the operations:

- grid connection and disconnection,

- power cable unwinding,

- electric generator connection type change (4 or 6 poles).

The "Production" states are "Sg" and "SGG". The 'operative but disconnected from the grid' state is "St". The initial state is "SSTOPSM".

This machine is a slave of the [Safety](SecurityStateMachine.md) one, that is, it receives events from it. In [Legend of the Operation S.M. Diagram](LegendforOperationStateMachinedi.md) you have the list of possible states and events.

![](<lib/OperationSM-grafico.gif>)
