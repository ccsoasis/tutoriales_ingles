---
tags:
- electric generator shaft rotation speed
- generator
- pitch
- safety states machine
- safety
- current state value
- operation
- operation states machine
- action protocols
- controller
---

# Panel 'RPMs + Pitch + State Machines'

The following figure shows the panel called 'RPMs + Pitch + State Machines', which contains 6 channels.

![](<lib/RegistradorRPMsMaqEstado.jpg>)

- 1.In the first 'channel' a single signal with the **electric generator shaft rotation speed** (in rpms) is presented.

- 2.In the second 'channel' two signals are presented:

- 1.Signal generated in the Controller that serves as the blade **Pitch** *setpoint value*.

- 2.Signal coming from the hub simulator, with the real blade Pitch value.

- 3.In the third 'channel' a signal is presented that corresponds to the **last event** received by the **Safety state machine** implemented in the Controller. See [Safety State Machine](SecurityStateMachine.md).

- 4.In the fourth 'channel' a signal is presented that corresponds to the **current state value** of the Safety state machine.

- 5.In the fifth 'channel' a signal is presented that corresponds to the **last event** received by the **Operation state machine** implemented in the Controller. See [Operation State Machine](OperationStateMachine.md).

- 6.In the sixth 'channel' a signal is presented that corresponds to the **current state value** of the Operation state machine.

This panel is very useful to follow the **action protocols** implemented in the Controller to respond to different circumstances and operations, in relation to key mechanical variables.
