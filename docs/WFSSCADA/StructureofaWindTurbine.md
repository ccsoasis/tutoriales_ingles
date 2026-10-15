---
tags:
- anemometer
- controller
- electric diagram
- generator
- grid
- operator terminal
- pitch
- SCADA
- wind vane
- nacelle orientation
- wind turbine
- control terminal
- point of common connection
- meteorological station
- PLC
---

# Operational structure

The mechanical, electrical and hydraulic elements that have been presented in [What is a Wind Turbine?](WhatisaWindTurbine.md) can be summarized in:

- **Power Train**: Blades, Hub, Rotor shaft

- **Gearbox**

- **Electrical generation system**

- **Brake system**

- **Orientation system**

- **Sensors** of wind speed and direction, temperatures, pressures, etc.

which are in the **Nacelle**, which is on the **Tower**.

Inside the Tower is the electrical cabinet through which the grid connection is made, through cables that connect the generator with a transformer. This transformer can be located in the Nacelle, or in the Tower base, or it can be in a nearby external shed.

In addition the wind turbine has a control unit, known as **Controller**, in charge of its operation. The Controller can be constituted by industrial computers, or **PLC**s (*Programmable Logic Controllers*) or combinations of them. The Controller receives sensor signals and commands the different elements to achieve at all times the required functionality. Given the complexity of the functions to carry out, its programming is usually done using the *"State Machines*" concept. In general there are two: one in charge of the operations themselves (cutin, cutout, Nacelle orientation, pitch adaptation as a function of the wind and the desired power, generator connection and disconnection, etc.), and another that supervises the general operation safety (voltage or power excesses, excessive Power Train or electrical generator speeds, alarms, excessive temperatures, etc.) Both work in a coordinated way.

The following figure shows the simplified schematic of the connections of a variable pitch and fixed speed wind turbine, which incorporates a generator that requires a "*softstarter*" for its grid connection (set of thyristors and bypass contactors).

![](<lib/Esquema DSAS.png>)
