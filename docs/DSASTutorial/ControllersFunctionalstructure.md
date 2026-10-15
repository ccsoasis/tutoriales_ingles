---
tags:
- controller
- PLCs
- programmable logic controllers
- real-time operating systems
- RTOSs
- states machine
- state transitions
- events
- operation
- safety
---

# Controller functional structure

The wind turbine **Controller** is a concept that encompasses the signal monitoring and element control processes to achieve the purpose of maximizing the produced energy, maintaining the necessary safety mechanisms.

Its implementation is very varied, and, in general, Controllers implemented with one or several **PLCs** (*Programmable Logic Controllers*) are found, or through Industrial Computers, generally, running *Real-Time operating systems* (RTOSs).

PLCs are monitoring and control units that do not have an operating system, and that are programmed to implement the logic of certain processes.

Industrial Computers are computers created for industrial environments and where Real-Time operating systems run: unlike other common operating systems for Office applications, RTOSs guarantee known response times for their operations. This characteristic is fundamental to be able to attend certain Industrial Plant operations, which must be carried out in short times and must not exceed certain limits.

The algorithms implemented must be those corresponding to the different sub-processes, the general coordination among all of them, and the attention to 'external' commands (both from the Operator, in local connection, and from the Control Center, through the remote connection).

Examples of sub-processes are:

- The nacelle yawing.

- The pressure maintenance in the brake hydraulic circuit.

- The electric generator cooling fan control.

- Etc.

The coordination and safety functionalities are usually programmed using the "**State Machine**" paradigm. This programming method has several advantages, among them, being able to visualize the different evolution possibilities (*State transitions*) and the possible reasons for each of these evolutions (*events*).

In general, in a wind turbine Control there are two State machines, one to implement the **Operation** functionalities, and another that implements the **Safety** functionalities.

In the Controller of this simulator the [following State machines](StateEventsDiagramsoftheimplemen.md) are implemented.
