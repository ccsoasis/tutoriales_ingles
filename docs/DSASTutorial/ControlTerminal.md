---
tags:
- control terminal
- controller
- access control
- maintenance
---

# Operator Control Terminal

Each wind turbine manufacturer delivers a device known as a "Control Terminal" or "Terminal de Control" intended to serve as the main interface tool between the Operator and the wind turbine control system, known as the *Controller*, to carry out the operations related to the wind turbine *maintenance* and *tuning*.

They are portable devices capable of operating in adverse (*rugged*) environments, including temperature and humidity extremes.

They connect to the Controller through a specific communications port, generally an RS-485 port or similar.

They have a display, generally small, and a keyboard. The following figure shows a typical example.

![](<lib/ControlTerminalKKElectronics-1.png>)

In the figure above, two parts fold for transport.

## Functions

With the Control Terminal, the Operator can do the following operations:

- **Know exactly the wind turbine situation**, accessing *the internal variables*. Many of these variables are accessible only through the Control Terminal and not, for example, through the connection to the Wind Farm SCADA system.

- Access the **historical incident data**.

- **Change parameters** that influence the general behavior of the wind turbine. For this, the Controller has "*access control*" mechanisms, with several levels, through which different change operations are allowed depending on the Operator profile.

## Description of some messages presented on the Terminal display

This display type does not allow a general view of all wind turbine parameters and variable values. Therefore, the system groups values in a way that makes sense for the operation being carried out. Examples are shown below (reduced).

Example of initial position display:

| STATUS | BREAKS | YAW | GEN | POWER | WIND | ROTOR |
|---|---|---|---|---|---|---|
| b | = | \| | \* | 0.0 | 8.3 | 0.0 |
| Manual yawing &lt; or &gt; |  |  |  |  |  |  |

Where:

| **b** | There is enough wind to start a cut-in operation (START) |
|---|---|
| **=** | The brake system is released |
| **\|** | Yaw mechanism inactive |
| **\*** | Generator not connected to the grid |
| **0.0** | No electrical energy is being produced |
| **8.3** | The current wind speed is 8.3 meters per second |
| **0.0** | Blade rotation speed |

The last line indicates that in this state, the "** < **" and "**> **" keys can be used to orient the nacelle manually.

Example of display with access to error messages:

| PENDING ERRORS | 1/4  - Page indicator (Error 1 of 4 actual errors). |
|---|---|
| ##nnn - Frequency on mains too low | - (Error number and text) |
| 01-03-02 10:26:59 to 00-00-00 00:00:00             -(Time register) |  |

Example of display with access to production data:

| P | 733.5 kW | GEN | 1507.3 rpms | 5/8 |
|---|---|---|---|---|
| Ref.: | -0.5 º | EffErr: | 338 |  |
| In Production |  |  |  |  |

To access each panel, use the up ("**↑**") and down ("**↓**") arrow keys. Becoming familiar with these information panels is part of the training required to operate this wind turbine model. **These panels are not standardized**, so knowing a given wind turbine's panel set only serves as a guide for becoming familiar with another model's, even within the same manufacturer.

## Description of the functions associated with each key

The key labeled "**START**" indicates to the Controller that it should start the grid connection operation and begin producing electricity. The Controller takes the act of pressing this key as a *request*, not as an order to be executed immediately. It becomes effective after the Controller confirms the general state of the wind turbine subsystems and that the wind value is within the appropriate limits.

The "**STOP**" key serves to order the Controller to start a *protocolized disconnection* from the Electrical Grid. The objective is to minimize mechanical stresses during stops and perform the grid disconnection safely.

The other keys allow:

- Navigating through the available displays ("**↑**" and "**↓**" keys).

- Changing the subsystem parameter values.

- The "** < **" and "**> **" keys also allow controlling the nacelle turning motors, provided the adequate conditions are met.
