---
tags:
- configuration
- synoptic
- squirrel cage
- function
- active stall
- active stalling
---

# Active Stall and Two-Speed Wind Turbine Simulator

The "**Two-Speed Wind Turbine Simulator**" is an **LdP application** that simulates the behavior of a wind turbine with a *squirrel-cage electric generator*, with the capacity to operate at *two speeds* (corresponding to two generator *synchronism* speeds, corresponding to the 2 possible stator winding connections), and that has *blade pitch control*.

The Power Train control algorithm used is known as "*Active Stalling*" (that is, *active entry into aerodynamic losses*), which is described in [By entry into losses (Stalling)](Stalling.md). The concept of *'active'* refers to the blade angle (pitch) being governed so that the entry into losses occurs with a wind lower than the characteristic one of the blade used. This method has the advantage that the angle range that must be handled for its control is much smaller than in the case of control by *'letting the wind pass'* (*'to the feathers'* in English), which implies greater simplicity of the pitch actuation mechanism.

The blade entry into losses is necessary to decrease the energy collected from the wind, when it is above the Nominal Wind.

The Controller simulator implements, additionally to the functionalities related to:

- the Operation (start-up, stop, nacelle orientation, Pitch control, etc.)

- the Safety (various stop incidents)

- the Generator stator connection mode change algorithm, that is, the two possible operating speeds. This facility allows the wind turbine to adapt better to wind speeds below the nominal.

The LdP configuration for this simulator is called (for Spanish language) "*DSASSpanish.conf*", and defines a set of "*Processes*", "*Synoptics*", "*Parameters*" and "*Connections*".

A "Process" is an LdP code block that does not have 'per se' an associated synoptic. This configuration uses the following.

| **Process** | **Internal name** | **Description** |
|---|---|---|
| NacelleEmulator | Nacelle |  |
| DriveTrainDynamics | Nacelle.DriveTrain | Power Train simulator |
| YawingNacelle | Nacelle.Yawing | Nacelle Yawing Mechanism simulator |
| BrakeHydraulicCircuit | Nacelle.Braking | Brake Hydraulic Circuit simulator |
| YawingControl | Controller.Yawing | Nacelle Yawing Controller simulator: wind direction tracking, and power cable unwinding. |
| ControllerEmulator | Controller.Control | Wind Turbine Controller simulator, including the Operation (cutin / cutout) and Safety functions. |

A "Synoptic" is an LdP code block that contains a certain user interface, through which the user accesses the value of certain variables and, some of them can also be modified.

This configuration uses

| **Synoptic** | **Internal name** | **Description** |
|---|---|---|
| ControllerEmulator | Controller.Control | User interface that emulates the wind turbine 'Control Terminal' and also the Controller itself. |
| IFDriveTrain | SynopticDriveTrain | Synoptic that presents two wind turbine views: in 3D and internal of the nacelle, together with a set of graphic elements related to the Power Train, the brake system and the electric generator. |
| IFWindNacelle | SynopticWindNacelle | Synoptic through which the following variables and functionalities can be accessed: a) See and change the wind speed and its orientation b) See the nacelle orientation. c) See the Wind Vane signal. d) See the state of the Power Cables that go down from the nacelle e) See the section of one of the blades where the following are presented: oThe Pitch angle value ordered by the Controller. oThe real Pitch angle value in the Hub. oThe effective wind speed value. oThe equivalent wind due to the blade rotation. oThe composed total wind incident on the blade. |
| IFElectricPanel | WTElectricPanel | Synoptic that presents the main Electrical Cabinet. |

A "Parameter" is a named value that is used by some of the Processes or Synoptics in their emulation of the mechanical, hydraulic, aerodynamic, etc. subsystems, and/or of their control mechanisms.

In this configuration the following parameters exist;

| **ProcessID** | **Name** | **Type** | **Value** | **Value max** | **Value min** | **units** | **Description** |
|---|---|---|---|---|---|---|---|
| NacelleYawing | CCWYawingSpeed | A | 10 | 10 | 0 | º /second | Counter Clock Wise motor speed in degress/second |
| NacelleYawing | CWYawingSpeed | A | 10 | 10 | 0 | º /second | Clock Wise motor speed in degress/second |
| NacelleYawing | MaxCableTwist | A | 2.5 | 100 | 0 | turns | max number of turns of the power cables in any direction |
| Nacelle | DriveTrainMomentOfInertia | A | 3500000 | 6000000 | 1000000 | kg \* m2 | Moment of Inertia of the whole DriveTrain |
| Nacelle | GeneratorSpeedVCU | A | 1803 | 2000 | 0 | rpms | Generator rpms that set the VCU - overspeed electrical centrifugal contact |
| Nacelle | RotorSpeedforHCU | A | 26.4 | 30 | 0 | rpms | HCU - High speed Centrifugal Unit contact |
| NacelleBrake | HydrPumpMaxRunTime | A | 40 | 200 | 4 | seconds | Max time for reaching operating pressure |
| NacelleBrake | HydrPumpMinTimeBetweenStarts | A | 20 | 100 | 2 | seconds | Min time between successive starts of the hydraulic pump |
| NacelleBrake | LeakageBrakeHydrCircuit | A | 0.01 | 10 | 0 | bars / second | Overall leakage of the brake hydraulic circuit |
| NacelleBrake | PumpCaudal | A | 5 | 100 | 0 | per cent of the oil tank | Caudal of pump. Volumen of the reservoir is assumed to be 100 units |
| NacellePitch | BladeSlewRate | A | 10 | 100 | 0.5 | degrees / second | Blade's control maximum speed of change |
| Controller | TempMaxGenerator | A | 150 | 180 | -10 | degrees | Generator's maximum temperature to operate |
| Controller | TempMaxGearBox | A | 80 | 180 | -10 | degrees | GearBox's maximum temperature to operate |
| Controller | TempMaxRotorBearing | A | 80 | 180 | -10 | degrees | Rotor Bearing's maximum temperature to operate |
| Controller | TempMaxAmbient | A | 50 | 180 | -10 | degrees | Max ambient temperature to operate |
| Controller | WindMaxForOperation | A | 25 | 35 | 3 | m/s | Max wind for continuous operation |
| Controller | WindMaxForTemporalOperation | A | 28 | 35 | 3 | m/s | Max wind to operate during 100 seconds |
| Controller | WindAbsolutMax | A | 30 | 35 | 3 | m/s | Wind for immediate shutdown |
| ControllerYawing | WindMinForAutomaticYawing | A | 1.5 | 10 | 0.1 | m/s | Wind speed below which the WindTurbine does not yaw |
| ControllerYawing | MaxCableTwistForReorientation | A | 1.5 | 5 | 1 | turns | Number of Cables turns that will force reorientation before trying to Cutin. Must be smaller than NacelleYawing.MaxCablesTurns |
| ControllerYawing | MaxYawingTime | A | 120 | 1000 | 0 | seconds | Max time for arriving to up-to-wind |
| ControllerCutin | MaxWindForCutin | A | 18 | 25 | 5 | m/s | Wind above which the Cutin operation does not start. |
| WindFarm | MainSwitch | D | -1 |  |  |  | WindFarm's Main Switch |
