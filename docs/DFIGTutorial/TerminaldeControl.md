---
tags:
- start
- stop
- control terminal
- cutin
- cutout
- idle
- supersynchronous
---

# Control Terminal

The "*Control Terminal ..*." synoptic is designed with the following objectives:

![](<lib/Terminal de Control en produccion en espanol.jpg>)

- To mimic as much as possible the functionalities and operation of the device known as "**Control Terminal**", which is used by the wind turbine service personnel, inside the wind turbine itself. With it, the following operations can be carried out:

- To facilitate the learning of the access to the previous functionalities. In some cases Control Terminals with very limited graphic and interactive capabilities are used, which forces the access to certain functionalities or the query of certain variables to be done through "cascade menus", which forces a knowledge (memorization) of the navigation through those menus. In the design of the "Control Terminal" simulation, the option chosen has been to facilitate as much as possible the visualization of the most common variables and the access to the control functions, in order to facilitate the student's familiarization with the wind turbine functionalities, instead of forcing them to memorize the navigation through those menus.

- To facilitate the direct access to the evolutions of the two state machines that the Controller uses to monitor and control the overall operation of the wind turbine.

- To facilitate the access to the state and the evolutions of the two state machines ("Operation" and "Safety") that the Controller uses, which allows a better understanding of the interactions of the wind turbine with its environment: wind, Electrical Grid, etc. and the operating conditions of its subsystems.

| ![](<lib/DFIG OutSignals espanol.jpg>) | **Pitch**: *desired value* of the blade angle (Pitch), in degrees. **Disc brake**: when active (yellow background) it indicates that the Power Train cannot rotate. **Brake released**: when active (yellow background) it indicates that the Power Train can rotate. **Brake pump**: when active (yellow background) the brake hydraulic circuit pump *must* be running. **Grid phases**: when active (yellow background) it indicates that one of the grid phases is out of voltage limits. **Contactor.Stator**: when active (yellow background) it indicates that the Generator Stator is connected to the grid. "**&lt;--**" and "**--&gt;**": when one is active (yellow background) it indicates that the corresponding nacelle turning motor must be activated, in the corresponding direction. **Vibrations**: when active (yellow background) it indicates that the vibration sensor signal has been received in the tower (see [nacelle synoptic](DFIGWTSensorVibracionesTorre.md)). **HCU**: when active (yellow background) it indicates that the overspeed sensor on the gearbox low-speed shaft has been activated (see nacelle synoptic). **VCU**: when active (yellow background) it indicates that the overspeed sensor on the gearbox high-speed shaft has been activated (see nacelle synoptic). |
|---|---|
| ![](<lib/DFIG START STOP.jpg>) | **START**: Pressing this button orders the wind turbine to begin the operation of connecting the generator to the grid and starting production (*cutin*). This will happen if two conditions are met: there is enough wind and there are no incidents to acknowledge. **STOP**: Pressing this button orders the wind turbine to start the operation of stopping production in an orderly way (*cutout*) and remain in standby (*Idle*). |
| ![](<lib/Giros manuales espanol.jpg>) | When the wind turbine is not in production, these two buttons allow commanding the corresponding nacelle yawing motors. |
| ![](<lib/Terminal Control viento espanol.jpg>) | In these indicators the data related to the wind are shown (real and effective, taking into account the nacelle misorientation with respect to the wind direction), its direction and that of the nacelle. |
| ![](<lib/Terminal control RPMs.jpg>) ![](<lib/Terminal Control slip espanol.jpg>) ![](<lib/Terminal control Aceleracion espanol.jpg>) | **Gen RPMs:** revolutions of the Electric Generator Rotor. **Rotor RPMs:** revolutions of the Hub (Blades). **Slip** (in %): = (1 - GenRPMs / SynchronismRPMs). (SynchronismRPMs = revolutions at which the Generator is in synchronism with the grid.) If it is negative it means that the Generator is rotating at rpms *higher* than the synchronism ones (supersynchronous state). If it is positive the state is subsynchronous. **Cp:** value of the blade aerodynamic coefficient (under the current conditions). |
| ![](<lib/Terminal Control Potencias espanol.jpg>) | Active and reactive powers, and Power Factor. |

| ![](<lib/Term Control UCPotenciaActiva espanol.jpg>) | ![](<lib/Term Control UCPotenciaReActiva espanol.jpg>) |
|---|---|
| *Control of the desired active power.* | *Control of the desired reactive power. It can be positive or negative.* |

| ![](<lib/DFIG StateMachines.jpg>) These indicators show the "state" and the "last event" that occurred in each of the two Controller state machines ("Operations" and "Safety"). ![](<lib/Term Control Mensajes espanol.jpg>) The "Messages" tab shows the series of events that have occurred with date, affected state machine and name. ![](<lib/DFIG Opened incidencies.jpg>) If there are open incidents they are shown in this tab. The case of the existence of a problem in one of the grid phases is shown (in this case produced by opening the Main Switch, see [Electrical cabinet](DFIGArmarioElectrico.md)). When the cause of each incident disappears, the date is recorded in the "Recovered" column. When the cause of an incident has disappeared, they pass to the "incident history", provided that one of the two following circumstances occurs: The incident does not require being "acknowledged by the operator". The incident requires being "acknowledged by the operator" and the latter effectively acknowledges it ("Open incidents" tab, "Ok" column). When this happens the "Incident history" tab shows the historical record of them. ![](<lib/DFIG Historic Incidencies.jpg>) |
|---|
