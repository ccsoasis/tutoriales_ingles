---
tags:
- pump
- reservoir
- valve
- disc
- brake shoe
- spring
- tank
- pressure switch
- hysteresis
---

# Brake mechanism

## The hydraulic brake system

The mechanical brake mechanism of the Power Train is implemented by means of a disc brake, actuated through a hydraulic circuit. This mechanism implements the "Fail Safe" paradigm (safe operation when there is a fault), so that in conditions where there is no grid connection, the Power Train is locked.

<u>*The design of this brake is not to be used as the habitual mechanism to stop the Power Train*</u> during normal grid disconnection operations (STOP order): these operations are carried out by acting on the blade Pitch, since their aerodynamic coefficient can become very negative when the Pitch is at values above 20º and the Power Train is at production rpms. With this procedure the kinetic energy stored in the Power Train is used to "drive" the air.

The brake system is indeed designed so that it can perform an emergency stop, that is, to dissipate in a very short time the kinetic energy of the Power Train when it is at production rpms, although this usually implies a destruction of the friction pads and/or a deformation of the disc or of the caliper that holds the pads; that is, even if that stop implies a breakdown of the wind turbine.

The habitual use of the disc brake is as a locking mechanism for the Power Train, <u>once it is stopped</u>. This is useful in several situations, for example, during maintenance operations in the nacelle.

| ![](<lib/Sistema hidraulico con textos.png>) | Components: The **disc**, where the kinetic energy of the Power Train is dissipated. The **brake shoe**, forced to be at high pressure against the disc, when it is desired that the brake be active. This is done by means of a powerful **spring**. That spring is forced, in a single direction, through a hydraulic circuit. The **pump**, which forces the hydraulic pressure in the spring circuit, through the liquid that exists in the **tank**. When the **valve** is closed and the pump is active, the liquid of the hydraulic circuit increases the pressure, making the spring compress, which makes the brake shoe separate from the disc, releasing the Power Train to which it is attached, so that it can rotate freely. When the valve opens, the hydraulic liquid passes to the tank, decreasing its pressure, so that the spring forces the brake shoe against the disc, braking the Power Train rotation. There is a **pressure switch** (which is not shown in the synoptic, although the state of its switch is shown. See below). There is also a limit switch (**actuator switch**) that activates when <u>*the distance between the disc and the brake pads exceeds a certain value*</u>. |
|---|---|
| ![](<lib/Freno de disco - espanol.jpg>) | Detail of the disc brake components. |
| ![](<lib/Presotato detalle.jpg>) ![](<lib/Histeresis presostato.png>) | Detail of the **pressure switch:** The pressure P must overcome the opposing force produced by the springs (12) and (8). The force of the latter is adjustable (within a certain margin) through the screw (9). When this happens the microswitch (7) switches by closing its electrical contact. When the pressure drops the microswitch changes state and opens. **Hysteresis behavior of the pressure switch:** The value of the pressure at which the microswitch closes is not exactly equal to the value at which it opens. This characteristic is called hysteresis and is common in many sensors. The following figure shows this behavior. When the pressure is lower than P1 and rising, when it exceeds that value the state changes to On. When the pressure is higher than P2 and falling, when it exceeds that value the state changes to Off. |

## Brake mechanism control

The brake control algorithm is in the wind turbine Controller. The only signals used for this control (Controller outputs) are:

- Pump start signal. This is a digital signal. Within the simulator its name is "*Controller.Control.PumpOut*".

- Valve opening signal. It is a digital signal. Within the simulator its name is "*Controller.Control.HardBrakeOut*".

The Controller only receives the following signal from the hydraulic circuit:

- The pressure switch output. It is a digital signal that indicates whether the pressure in the hydraulic circuit is higher than P1 (On), or lower than P2 (Off). See previous graph. Within the simulator its name is "*Controller.Control.PressureSwitchIn*".

Additionally it receives another digital signal from the limit switch that indicates that the brake pads are separated from the disc by a distance that guarantees that the Power Train is released. Within the simulator its name is "*Controller.Control.BrakeReleaseIn*". This limit switch is adjusted so that it turns On with a hydraulic circuit pressure well below the P2 value mentioned above.

It is interesting to note that the Controller does not receive an analog signal corresponding to the pressure in the hydraulic circuit. However, the Controller's state supervision algorithm allows detecting a set of problems such as:

- That the pump has a power fault: this is detected by looking at the time from when the Controller starts the pump until the pressure switch reports that the P1 pressure level has been exceeded.

- That there is a pressure loss fault in the hydraulic circuit. This fault is detected by measuring the time interval from when the pump is deactivated because the pressure has exceeded the P1 level, until the pressure switch indicates that the pressure has dropped below the P2 level. This fault can have several causes: the hydraulic circuit itself, the valve, etc.

- That there is a problem in the brake release limit switch. This situation is detected because the pressure switch indicates that the P1 level has been exceeded and yet this limit switch has not activated.

In order to make it more comfortable to observe the evolution of the state and the variables of the brake system, this synoptic includes a specific panel, which is described below. It includes a clock-type indicator where the following are reflected:

- The pressure switch actuation levels (P1 and P2): green zone.

- The level from which the limit switch indicates that the brake is released (yellow mark).

It also includes a linear control ("*Brake circ. pressure*") that is habitually used to indicate the relative value of the pressure, but which can also be used to *force* an arbitrary value of this pressure and check the Controller's reaction. It is a convenient mechanism to simulate faults. To switch to "force" mode you must press the "F6" function key.

| ![](<lib/DriveTrain circuito frenos espanol.jpg>) | This panel includes the state presentation and/or control buttons for a set of signals. The buttons labeled "Pump", "Hard brake", "Soft brake", "Pressure switch" and "Brake released" present or control the associated signals. See the diagram below. The same occurs with the linear indicator labeled "Brake circ. pressure" that presents or controls the pressure in the circuit. The limits of the green zone correspond to the pressure switch limits. The yellow mark corresponds to the pressure that makes the limit switch activate. |
|---|---|

The following list shows the connections of these buttons and indicators with the associated signals. The "Soft brake" is not used in this simulator, although it is kept in the synoptic since there are models that include it. It refers to a second discharge valve, which has a flow rate when open that is lower than the one corresponding to "Hard brake".

| **Button or indicator** | **Controlled output signal** | **Signal indicated when not in "force" mode** | **Output signal to which the input signal is connected** |
|---|---|---|---|
| Pump | *Nacelle.Braking.PumpIn* | *SynopticDriveTrain.PumpIn* | *Controller.Control.PumpOut* |
| Pressure switch | *Controller.Control.PressureSwitchIn* | *SynopticDriveTrain.PressureSwitch* | *Nacelle.BrakingPressureSwitchOut* |
| Hard brake | *Nacelle.Braking.ValveHardBrake* | *SynopticDriveTrain.HardBrakeIn* | *Controller.Control.HardBrakeOut* |
| Soft brake | *Nacelle.Braking.ValveSoftBrake* | *SynopticDriveTrain.SoftBrakeIn* | *Controller.Control.SoftBrakeOut* |
| Brake released | *Controller.Control.BrakeReleaseIn* | *SynopticDriveTrain.BrakeReleasedIn* | *Nacelle.Braking.BrakeReleaseOut* |
| Hydraulic circuit pressure | *--* | *SynopticDriveTrain.BrakeHydrPressureIn* | *Nacelle.BrakeCircuitPressure* |

The following diagram shows the relationship between:

- The Controller control signals.

- The indicators and buttons in the synoptic.

- The input signals to the Controller.

- The simulator elements: Pump, Valve, Pressure Integrator, Pressure switch, Brake released limit switch.

![](<lib/Esquema circuito frenos.png>)

The "F6" icons indicate that those signals can be interrupted, so that the corresponding indicator switches to "Force" mode, i.e. its output is not a replica of the input but of the value chosen by the user. This functionality allows creating "anomalous" situations very easily.

For example, if we put the linear indicator "Brake circ. pressure" in "Force" mode, we can observe that the state of "Valve" and "Pump" do not affect the pressure. Also, by modifying the pressure manually with the indicator we can quickly check the functionality of the "Pressure switch" and "Brake released" simulators. By doing these manipulations we will begin to have messages in the [Control Terminal](TerminaldeControl.md).
