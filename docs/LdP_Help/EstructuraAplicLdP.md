---
tags:
- human machine interface
- processes
- connections
- simulation workstation
- output signals
- input signals
- process
- synoptics
---

# Structure of LdP applications

Structure of LdP applications

***LdP*** (acronym of "*Lenguaje de Procesos*") is an execution and development platform of Real Time Simulators, that implements the concept of "***simulation workstation***" in which it is possible to interact with said simulators.

The user interface is carried out by means of ***Synoptics***, both general LdP ones and specific to each Simulator. Said Synoptics contain indicators and/or buttons associated with different internal Simulator signals.

*LdP* handles the concept of "***Process***" as an element where the behavior of some of the Simulator components is implemented.

The *Synoptics* and the *Processes* of a Simulator are components that connect with the paradigm of electronic components in an electrical circuit: the ***output signals*** of any of them can connect with one or several ***input signals*** of any of them.

The *Synoptics* can contain none, one or several *Processes*. The Processes can be components in themselves, independent of the Synoptics.

- Each *Process* carries out the simulation of some subsystem in the equipment to simulate.

- The Human Machine Interface is materialized in the Synoptics design, which must have the adequate indicators so that the user can know at all times and in the best way, the internal signal values. The value of a signal can be visualized and/or used in more than one Synoptic.
