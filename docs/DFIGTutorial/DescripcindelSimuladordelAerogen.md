---
tags:
- wound rotor
- incident manager
- recorders
---

# Description of the DFIG Wind Turbine Simulator

The **ACMSL(****©****) DFIG-type Wind Turbine Simulator** simulates the behavior of a DFIG wind turbine with Back-to-Back converters, and is developed on the **ACMSL(****©****) LdP platform**, and therefore incorporates the following set of functionalities:

- These simulators are created from a set of simulators for each of the specific *parts* and *subsystems* of the system to be simulated.

- These subsystems (modules) are assembled together following the "electrical schematic paradigm", so that the output signals of some are connected with the input signals of others, thus building a complete simulator. The specification of the subsystems and their connections is done through a configuration file. These configuration files also include the values of specific parameters of the involved subsystems.

- The execution of a simulation can be stopped at will and restarted later.

- It is possible to change the values of the subsystem parameters <u>*while the simulation is running*</u>.

- It is possible to change the connections between the subsystems <u>*while the simulation is running.*</u> This capability allows creating configurations corresponding to faults: for example the breakage of a real connection cable.

- All the changes of the variables, both external and internal, are recorded (logged) in a database, and are available for later analysis.

- During the simulation, the evolution of the signals can be visualized through the use of *Recorders* ("*Striprecorders*").

In particular, the DFIG Simulator includes simulation subsystems (modules) for:

- The hydraulic brake system (in the nacelle).

- The control of the hydraulic brake mechanism (in the Controller).

- The yawing mechanism (in the nacelle).

- The control of the yawing mechanism (in the Controller).

- The blade angle (pitch) control mechanism (in the Hub).

- The blade angle control mechanism (in the Controller).

- The simulator of the set formed by the Wound-Rotor Electric Generator and the associated Back-to-Back converters, **including the real-time calculations of all the Generator variables**.

- The power control algorithms in the Power Train (MPPT and fixed point), using the real-time calculation of the aerodynamic coefficient (Cp) corresponding to the design of the blades used.

- Control algorithm of the desired "Active Power" and "Reactive Power".

- Specific graphs that allow following, in real time, the evolution of key variables to understand the behavior of the wind turbine against changes in working conditions.

- The Controller simulator also implements two state machines:

The user interface is done through a set of specific synoptics that are described below.
