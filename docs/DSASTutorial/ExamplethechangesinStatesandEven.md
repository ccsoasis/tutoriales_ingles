---
tags:
- grid connection
- cutin
---

# Example of State and Event changes in the S.M. during a connection operation (cutin)

This simulator has a signal "Panel" defined (see [Panel 'RPMs + Pitch + State Machines'](PanelCircuitohidrulicodefrenos.md)) that allows observing the evolution of two key variables (the generator shaft rotation speed and the pitch angle) together with the events and state changes of the two state machines.

The following figure shows the evolution of these signals in a grid connection operation (cutin).

![](<lib/DSAS Evolucion de estados en cutin a 6 ms.jpg>)

The previous figure shows the evolutions of the relevant signals:

- the Generator rpms -GeneratorRPMsOut-

- the commanded blade angle signal -Controller.PitchOut-

- the real angle in the nacelle -PitchNacelleOut-

- the events of the Safety state machine -STOPSeqEvent-

- the state changes of the Safety state machine -STOPSeqState-

- the events of the Operation state machine -OperationEvent-

It can be seen that the final state of the Safety machine is "SOBOn", which indicates entry into production.

It can also be seen that the last event is the one of activating the thyristor Bypasses, with the "Small" generator.

|  |
|---|
