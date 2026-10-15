---
tags:
- SCADA
- data request
- grid disconnection
- cutout
- grid connection
- cutin
- active power setpoint
- reactive power setpoint
---

# Remote control from the SCADA

In Automatic mode, the Controller is pending commands sent to it through the data line, normally connected to the Wind Farm Control Center where the wind turbine is.

The commands are generally:

- **Data request:** the Controller responds with a message in which various wind turbine operating data are included: State (in Production/Stopped/With Fault), measured wind, wind direction, instantaneous Power (Active and Reactive), accumulated produced Energy, temperatures in various elements, etc.

- **STOP**: start the *grid disconnection* (*cutout*) operation.

- **START**: start the *grid connection* (*cutin*) operation.

- Change of the **Active Power setpoint**: this functionality is not implemented in the wind turbine simulated by this configuration.

- Change of the **Reactive Power setpoint**: this functionality is not implemented in the wind turbine simulated by this configuration.
