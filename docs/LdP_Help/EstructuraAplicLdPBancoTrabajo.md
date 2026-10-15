---
tags:
- LdP
- building blocks
- test bench
- simulation workstation
- indicators / controls
---

# The LdP as a workbench

As indicated in [Basic concepts](EstructuraAplicLdPConceptosBasic.md), a simulator developed in LdP can be represented as an electrical schematic in which there are different **blocks** that are assumed to carry out certain operations (parts of the simulator) that receive a set of signals and that generate other signals that, it is assumed, will serve other blocks.

These blocks are interconnected by "connections," equivalent to physical cables in an electrical panel. The following figure illustrates this concept.

![](<lib/NacelleyController conectados.png>)

Additionally, LdP has mechanisms that allow it to function as a "test bench" or "workbench." The idea is to facilitate changing the conditions under which the simulator runs and observe its responses to those changes. To this end, it is assumed that each simulator has the appropriate synoptics, adapted to the simulation needs of the equipment or system to be simulated. Here are some examples:

| ![](<lib/Brake system.jpg>) | Hydraulic Brake Circuit Subsystem. |
|---|---|
| ![](<lib/Reloj presion hidraulica.jpg>) | Pressure indicator in a hydraulic circuit. |
| ![](<lib/GeneradorConFlujosYFlechas.jpg>) | Magnetic flux vector indicator in an induction machine. |
| ![](<lib/Vista Cp en MPPT en espaol.png>) | Current value of a function of several parameters. |
| ![](<lib/Potencia vs rpms con cursores en produccion e.jpg>) | Value of two signals (mechanical and electrical power) on a map of possible operating areas. |
| ![](<lib/RRC PowervsSlip en produccion.jpg>) | Operating point and associated slope. |

In addition LdP has [indicators / controls](EstructuraAplicLdPIndicadores.md) that are graphic elements used to present signal values and also to *force* the values of other signals. These indicators, available for the LdP-compatible synoptic developers, have been designed to minimize the screen space required to design a User Interface that is both complete and not overwhelming.

These LdP components are described in the following section and their main feature is that they can be used both to indicate the value of a signal and to force that value manually.

Additionally, LdP has "[Recorders](EstructuraAplicLdPRegistrador.md)" to visualize the evolution of changes of certain signals chosen as significant, as well as a [connections editor](EstructuraAplicLdPEdicionConex.md), (which allows simulating the cut cable concept) and another [parameters editor](EstructuraAplicLdPParametros.md), characteristic values of simulation units within the general simulator.
