# Observation of an excessive pressure loss fault in the circuit

!!! tip "🎯 Hydraulic circuit losses observation"
    ***Objective:*** Analyze the effect of pressure losses on the hydraulic system performance.
    ***What to observe:*** Pressure evolution, pump operation and actuator behavior.
    ***What to note:*** Difference between expected and real pressure, and consequences on the system.
    💡 a progressive loss usually causes slower or incomplete responses.

!!! warning "❓ Guiding questions"
    1. When a stop process is started while in production, is the hydraulic brake used?
    2. What criterion does the controller use to detect a problem in the hydraulic system and which variables does it monitor?

In this practice the protocol implemented by the Controller to face a common problem of excessive pressure loss in the hydraulic circuit will be observed.

These losses can come from any of the elements: hoses, tubes, the valves themselves or the pump.

The way to simulate this problem is carried out in this simulator by modifying the "*NacelleBrake.LeakageBrakeHydrCircuit*" parameter.

![](<lib/parámetro-leakage-normal.jpg>)

To create the fault situation we can increase the default value (0.01 out of a maximum of 10) to a 100 times higher value (1). To change the value follow the instructions described in [Parameter value change](../DSASTutorial/Cambiodelasconexionesdelaconfigu.md).

You will see that shortly after the Controller emits an incident with description "*Pump starts too often*" (*the pump starts operating too often*), and disconnects the generator from the grid. In the recorder you will see a signal evolution similar to the one in the following figure.

![](<lib/registradocircuitohidraulico-perdidas-1.jpg>)

If now you restore the default losses value, which is equivalent to having repaired the fault, you will see that the Controller does not start a grid connection process immediately: this is because the mechanism for checking that 'everything is fine' requires that: a) the circuit pressure is restored, and b) the time between two pump starts is 'sufficiently long'.
