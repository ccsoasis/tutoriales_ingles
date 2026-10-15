---
tags:
- brake hydraulic circuit
---

# Brake hydraulic circuit monitoring

!!! tip "🎯 Hydraulic circuit observation"
    ***Objective:*** Identify the hydraulic circuit function and recognize anomalous operation symptoms.
    ***What to observe:*** Pressure, pumps/valves, actuator states and related alarms.
    ***What to note:*** Normal vs anomalous values and which evidence supports your diagnosis.
    💡 If there are alarms, note the first one that appears and which variable changes just before.

!!! warning "❓ Guiding questions"
    1. When a stop process is started while in production, is the hydraulic brake used?
    2. What criterion does the controller use to detect a problem in the hydraulic system and which variables does it monitor?

In the following practices the objective is to become familiar with the *brake hydraulic circuit*, and explore several problems that can occur in its operation, and the procedures implemented by the Controller for their detection, and incident generation.

You must first become familiar with the behavior of this system, basic for the wind turbine safety. In [Brake System](../DSASTutorial/Mecanismodecambiodeangulodelaspa.md) you have the general description and some industrial examples. In [Brake system](../DSASTutorial/IndicadoresSistemaFreno.md) you have a description of the graphic elements presented in the "SynopticDriveTrain" synoptic that present and/or control the variables associated with this system. The following figure shows the relationship of the indicators and each one of the physical components, as well as the control and input signal connections to the Controller.

![](<lib/Esquema circuito hidraulico.png>)

Fig 1.

The signals involved are the following:

| **Output signals** |  |
|---|---|
| *Nacelle.Braking.BrakeReleasedOut* | Comes from the physical brake simulator in the Nacelle. If it is 'On' it indicates that the shoe does not touch the disc, that is, the Power Train is released. This occurs when the hydraulic circuit pressure is higher than the value indicated by the yellow line in the circular indicator "Brake circuit pressure". |
| *Nacelle.Braking.PressureSwitchOut* | Corresponds to the pressure switch output: if it is 'On' the hydraulic circuit pressure is higher than the upper green zone value. If it is 'Off' it is below the lower green zone value. |
| *Controller.Control.HardBrakeOut* | Brake valve control signal. |
| *Controller.Control.PumpOut* | Pump control signal. |

| **Input signals** |  |
|---|---|
| *Nacelle.Braking.PumpIn* | Control input to the pump. |
| *Nacelle.Braking.ValveHardBrake* | Control input to the fast discharge valve. |
| *Nacelle.Braking.ValveSoftBrake* | Control input to the normal discharge valve. |
| *Nacelle.Braking.PumpCaudalIn* | Descriptive value of the pump flow. Connected to "*Parameter.NacelleBrake.PumpCaudal*". |
| *Nacelle.Braking.LeakageBrakeHudrCircuit* | Descriptive value of the 'pressure loss state' in the circuit. Corresponds to the aggregated pressure loss value in hoses, tubes, valves, and pump. Connected to "*Parameter.NacelleBrake.LeakageBrakeHudrCircuit*". |
| *Controller.Control.PressureSwitchIn* | Pressure sensor input in the circuit. This is a digital signal, so it does not correspond to a proper meter. |
| *Controller.Control.BrakeReleaseIn* | Separation sensor input between the disc and the brake shoe. |
