# Observation of the effect of a pump with incorrect operation

!!! tip "🎯 Pump with fault observation"
    ***Objective:*** Recognize the symptoms of a fault in the hydraulic system pump.
    ***What to observe:*** Circuit pressure, pump state, associated alarms and actuator behavior.
    ***What to note:*** Differences between normal operation and fault, and which evidence confirms the diagnosis.
    💡 compare with the behavior in normal conditions before the fault.

!!! warning "❓ Guiding questions"
    1. When a stop process is started while in production, is the hydraulic brake used?
    2. What criterion does the controller use to detect a problem in the hydraulic system and which variables does it monitor?

In this practice the objective is to see how the protocol implemented by the Controller is to detect that the pump has some problem. The pump can have several problems:

a) it can have 'pressure losses' when it is not activated. This case is presented in the [Observation of an excessive pressure loss fault in the circuit](ObservacionPerdidasCircuitoHidra.md) class.

b) it may have lost impulse capacity, that is, the flow is not the due one when it is activated.

c) there can also be electrical problems, for example a protection fuse.

d) etc.

In the wind turbine on which this simulator is based, the normal pump and accessories behavior detection mechanism is detected by the time it takes to raise the hydraulic circuit pressure above the green zone corresponding to the pressure switch. This method does not discern between all the possible causes however, it is a very reliable procedure and does not use sensors that need calibration.

In this simulator, all these problems are emulated using the "*NacelleBrake.PumpCaudal*" parameter.

![](<lib/parámetro-pump-caudal-a-05.jpg>)

Fig 1.

You must make sure the wind turbine is in production (connected to the grid) and observe the "*Brake circuit pressure*" indicator in the "*SynopticDriveTrain*" synoptic. Likewise make sure you have a recorder with the "*Brake hydraulic circuit*" panel.

To create the fault situation we can decrement the default value (5 out of a maximum of 100) to a 50 times lower value (0.1). To change the value follow the instructions described in [Parameter value change](../DSASTutorial/Cambiodelasconexionesdelaconfigu.md).

You will see that the Controller emits an incident with description "*Pumping time too long*" (*too much time pumping*), and disconnects the generator from the grid. This occurs after quite a long time, since it is necessary for the hydraulic circuit pressure to drop below the lower green zone value, so that the Controller activates the pump.

In the recorder you will see a signal evolution similar to the one in the following figure.

![](<lib/registrador-circuitohidraulico-bomba-sincauda.jpg>)
