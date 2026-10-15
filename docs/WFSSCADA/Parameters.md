---
tags:
- parameter
- dispatching
- random
- parameters
- demand
---

# Parameters

This simulator uses the parameters listed in the following figure, for the internal processes. They can be accessed from the execution control synoptic "*Synoptics*" -&gt; "*Parameters*"

![](<lib/Parametros SCADA.png>)

The "***RandomCoefficient***" parameter of the "***Wind***" process regulates the wind speed randomness in each wind turbine.

The "***WaitingTimeToCancelProposal***" parameter of the "***AutoDispatcher***" process regulates the maximum time the operator has to cancel the proposal of the start or stop algorithm of a wind turbine set as a response to a wind speed or demand change. See [Automatic management](AutomaticDispatching.md).

The "***SetPointTolerance***" parameter of the "***AutoDispatcher***" process determines which is the produced *power range* considered acceptable. In % over the [demand](Externaldemandsetpoint.md).

To remove this form or synoptic from the screen you must use the "X" icon in the upper right part.
