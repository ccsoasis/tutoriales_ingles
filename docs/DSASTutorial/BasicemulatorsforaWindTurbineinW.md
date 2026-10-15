---
tags:
- operational blocks
- PLCs
- PLC
- interconnections
- sensors
- control algorithms
---

# Basic structure of the emulation used in this simulator

This Simulator consists of *two sets of simulation subsystems*: one set contains simulators for each physical element in the nacelle, and the other simulates the controllers for each subsystem. Usually, these controllers are implemented on duly programmed industrial computers (as this simulator does) or on PLCs (**P**rogrammable **L**ogic **C**ontrollers).

The following figure illustrates the resulting structure.

![](<lib/Diagrama bloque LdP.png>)

The lines with arrows indicate the data flow:

- The emulation of the real *sensors* (left part) supplies data to the corresponding controllers (right part).

- The control algorithms, which run in the right part, supply commands and setpoint values to the *physical element simulators*, which are in the left part.

The arrows indicate *interconnections* between these elements and are made through *output and input signals*. These connections correspond to physical connection cables, or to elements connected to a bus system (e.g., CANBus, FieldBus, etc.) existing in real wind turbines, and are 'editable'. That is, they can be *created or deleted at will* by the simulator operator. This is one of the basic characteristics of the framework on which this simulator is developed (LdP). See the "Introduction to LdP" tutorial for a detailed description of these concepts.
