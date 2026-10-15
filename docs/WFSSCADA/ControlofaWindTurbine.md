---
tags:
- control terminal
- active power
- reactive power
---

# Operation modes

The wind turbine has two **operation modes**:

- 1.*Manual:* this mode is used for the wind turbine maintenance. It allows the manual control of different subsystems (orientation, pitch, etc.), and access to the sensor variables, electrical measurements, etc. Due to the large number of options, when entering this operation mode a device with keyboard and screen (laptop computer, PDA, etc.) is used, known as "**Control Terminal**".

- 2.*Automatic:* this is the normal mode. In it, the wind turbine monitors the environmental variables and carries out the necessary operations to produce electrical energy according to them, or remain in standby. In this mode the Controller remains attentive to the orders that may arrive through the communications channel it has with the Wind Farm SCADA system.

The Controller functionalities can be grouped according to the following criteria:

- **Production control**.

There are at least two functions "START" and "STOP" through which the wind turbine Controller is indicated that it must start a "cutin" process (grid connection and production start) and "cutout" (production exit and grid disconnection).

Some wind turbines also allow the **maximum active power** to be set, always for a value equal to or lower than the nominal, and the **reactive power** level.

- **Production data access**.

The wind turbine Controller sends through the communications link the values of the important variables (voltages, currents, powers, produced energy, temperatures, etc.) as well as incidents (alarms, warnings, messages, etc.) that have occurred.

- **Internal control parameter access**.

Generally this functionality can only be done locally, and requires restricted access managed with passwords.

- **Manual control** of certain elements.

For example, the control of the motors that allow the orientation. These functionalities can only be done locally, generally also with password access.

*In general*, there is no standardization of the communications protocols, nor of the data formats, for the remote access to these functionalities.
