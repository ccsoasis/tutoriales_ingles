# Panel 'Controller State Machines'

The following figure shows the panel called 'State Machines', which contains 4 channels.

![](<lib/RegistradorMaqEstado.jpg>)

- 1.In the first 'channel' a signal is presented that corresponds to the **last event** received by the **Safety state machine** implemented in the Controller. See [Safety State Machine](SecurityStateMachine.md).

- 2.In the second 'channel' a signal is presented that corresponds to the **current state value** of the Safety state machine.

- 3.In the third 'channel' a signal is presented that corresponds to the **last event** received by the **Operation state machine** implemented in the Controller. See [Operation State Machine](OperationStateMachine.md).

- 4.In the fourth 'channel' a signal is presented that corresponds to the **current state value** of the Operation state machine.

This panel is very useful to follow the **action protocols** implemented in the Controller to respond to different circumstances and operations.
