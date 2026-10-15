---
tags:
- LdP
- framework
- datalogger
- datalogging
- striprecorder
- signal
- symbols
- synoptic
- operating state
- in production
- stopped
- not available
---

# Wind Farm Simulator Description

The ACM SL "Wind Farm Simulator", corresponding to the "WFSSCADAr12.conf" configuration of LdPv1r12, has been designed to create a *virtual space* where the basic functionalities existing in a real Wind Farm can be exercised, and observe the consequences of said actions.

The base ideas for this simulator are:

- Show the **real-time operation of the wind turbine set of a wind farm**.

- Show the **SCADA system functionalities of a wind farm**:

-   -**Wind turbine command**.

-   -**Production and state data collection** of the wind turbines.

-    -The **communications system with the wind turbines**.

-    -The **interface with the meteorological condition measurement unit**.

-    - The **visualization of the evolution of different variables in the wind turbines, environmental and demand**.

-    - Some **typical control algorithm examples** used for the management.

-    - The **user interface**, through which the operator can exercise these functionalities.

- Functionalities for the **wind turbine operating state change**.

- Functionality to **emulate the demand**.

- **3D visualization** of the wind farm.

- Meteorological Tower simulation

The Wind Farm model chosen for the simulation is composed of 29 variable pitch wind turbines, with aerodynamic stall entry control (Active Stall), similar to the one used as reference in the "*Two-Speed Wind Turbine Simulator*".

The wind speed in each one of them is simulated through a distribution similar to the influence of a real distribution in a territory, from the speed and direction specified in the Meteorological Tower simulator.

The wind turbine operating state has been reduced to three: "*In Production*", "*Stopped*", "*Not available*", in order to facilitate the general understanding of the operations.
