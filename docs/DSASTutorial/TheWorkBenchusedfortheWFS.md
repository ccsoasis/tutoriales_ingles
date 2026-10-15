---
tags:
- controller
- framework
- simulation workstation
- graphic indicator
- wired blocks
- Nacelle emulator
- controller emulator
- command mode
- processes
---

# The Simulator as a Laboratory Workbench

A simulator corresponds to the execution of a certain configuration on the LdP platform (©ACM).

Each configuration can specify a number of:

- **Processes**:  
For example, in this simulator, a process is the monitoring and control of the nacelle orientation with respect to the wind direction. Another is the control of the number of power cable turns. Another is the Pitch control, etc.

- **Synoptics**:  
These constitute the simulator graphic interface. They can contain Processes. They present graphic indicators, which can also be control ones, to present the values of certain variables, or change their values.

- **Parameters**:  
Each of the defined processes can have a certain number of parameters. The Parameters in LdP allow the user to access their visualization and modification, as well as their recording. (See the "*Introduction to LdP*" tutorial.)

- **Connections** between the previous elements.

- **Striprecorders**:  
These are sets of graphic recorders of the evolution of a selected set of variables, designed specifically for a simulator.

(See a detailed description in the "***Introduction to LdP***" tutorial).

These processes behave as *virtual replicas of real physical elements in electrical cabinets*, so that they can be interconnected with each other: with output terminals connected with input terminals.

These connections, as well as the parameter values, can be modified in real time; that is, eliminated or created even when the simulation is "running". These concepts correspond to those of changing the connections in an electrical cabinet or certain element parameters in said cabinets, while the simulation is running. In this way the LdP-based simulators behave as very flexible "***Laboratory Workbenches***".

The following figure shows an example of these possible connections in this simulator.

![](<lib/Ejemplo conectividad en LdP espaol.png>)

In this figure two blocks are shown that group the detailed processes. Both process sets must be connected with each other adequately. One of the signals, in this case the electric Generator revolutions, comes from one of the processes in the nacelle group and must be connected to one or more processes in the Controller. In the case of the figure this signal "is passed" through the indicator set: text, slider and clock, where the current value is shown, before connecting to the Controller.

Since some of these graphic indicators, for example, the text box or the slider, can be "put" in *command mode* (pressing the "F6" key), this arrangement allows simulating (*without making any change in the simulator configuration*) a fault that could be equivalent to a breakage of the Generator shaft revolutions sensor. For a complete description of the graphic indicator functionalities in the LdP Synoptics, see the "**The LdP as a workbench**" topic in the "*Introduction to LdP*" Tutorial.
