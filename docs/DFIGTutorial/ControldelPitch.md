# Pitch control

In this synoptic the blade Pitch value is shown in two places:

| ![](<lib/Hub con pitch a 1 5 grados.jpg>) In the Hub | ![](<lib/Indicador Pitch a 1 5 grados.jpg>) In a linear indicator |
|---|---|

This value is also shown in the right panel in the "*SynopticWindNacelle*" synoptic.

![](<lib/WindNacelle panel hub 1 5 grados.jpg>)

In the wind turbine there is a signal that is generated in the Controller and that reaches the Pitch mechanism servo-control in each blade. In the simulator the following circuit is implemented, which includes other signals related to the Pitch.

![](<lib/Esquema conexiones Pitch.png>)

The signal generated in the Controller (*Controller.Control.PitchOut*) is sent to the nacelle simulator, which is accessed through the SynopticDriveTrain. This synoptic has a linear indicator that can work in indicator mode of the value of the signal that reaches its input (*PitchOut* in this case) or in "Force" mode. This mode is reached by pressing the F6 function key. When it is in this mode, the value of its output does not reflect the value of the signal that reaches its input (90º in the example shown), but the value imposed by the user through the sliding needle (*slider*) or by directly typing the desired value (finishing with an "Enter"). This value is the one used in the Hub graph, which is refreshed in real time. Both values are indicated in the Hub panel in the SynopticWindNacelle: the Controller's as a pink vector; the value in the nacelle to position the blade direction.

The real Pitch value in the blades also reaches the Controller, which continuously monitors it.

This arrangement of indicators and signals allows creating "anomalous" situations very easily, in order to study the Controller's reaction. For example, the Pitch indicator mode can be switched in SynopticDriveTrain (F6), or the connection between *Controller.Control.PitchOut* and *SynopticDriveTrain.PitchIn* can be "cut", while a start-up operation is launched, and observe when the Controller generates an incident that aborts that operation.

The simulation of the servo-system that governs the Pitch, which can be unique for the three blades (e.g., in wind turbines where these servo-systems have hydraulic actuators) or one per blade, includes a parameter that is key for the stability of the wind turbine operation: "*NacellePitch.BladeSlewRate*". This parameter indicates the Pitch angle rate of change. This value determines the adaptation of the Power Train to rapid wind changes or its maximum stop speed. By modifying the value of this parameter it is possible to observe different behaviors of the wind turbine against different operations (start-up, stop, response to wind gusts, etc.).
