---
tags:
- squirrel cage
- fixed pitch
- active stall
- test bench
- pitch
---

# Introduction

This tutorial corresponds to the "Two-Speed and Active Stall Wind Turbine Simulator", from the ACM SL family of Real-Time Wind Turbine Simulators. Its design models the wind turbines that use squirrel-cage electric generators (*squirrel cage* in English), that is, with short-circuited rotor winding, and with the stator connected directly to the grid. The generated power control system is carried out by varying the blade angle on the wind (Pitch), using the [Active Stall](Stalling.md) principle (induced entry into aerodynamic losses). Additionally it implements the concept of adaptation to the wind range through switching between two Generators (or with a single Generator that has two windings).

This Simulator operates on the ACM SL LdP platform, through the "*DSASr12.conf*" configuration, which uses a set of LdP components (see [Active Stall and Two-Speed Wind Turbine Simulator](SimDSAS.md)).

With this Simulator the commands admitted by a real wind turbine can be executed, as well as observing its reactions. For each of the wind turbine subsystems there is a dedicated simulator, with its specific parameters and signals, which can be observed. Through specialized synoptics the values of these signals can be modified (even during the simulation execution), so that the simulator can be used as a "***Test bench***". The design of the subsystem simulators and the synoptics allows observing the evolution of these signals with general operating conditions similar to those faced by a real wind turbine in a Wind Farm.

For example, the reaction against extreme winds can be observed. Or how it reacts to excessive generator heating. Or to a breakage of the blade angle variation mechanism. Or the influence of the weight increase on the blades (due to ice, for example).

The simulated wind turbine is of the HAWT type (horizontal axis), oriented to the wind (upwind, "*up wind*" in English), with three blades.

In this tutorial the physical principles used in the design of wind turbines that use the power control principle through ["entry into losses" (stalling)](Stalling.md) are explained.

The objectives of this Simulator are:

- To emulate the behavior of each subsystem within the wind turbine, including the Controller, so that the observed behavior is very close to that of the real wind turbine.

- To present the user a set of visualization tools with which they can observe, effectively and easily, the values of all the internal signals, and their evolution.

- To allow interacting with the wind turbine, changing its environmental conditions (wind, electrical grid connection, temperatures, etc.), to introduce most of the real operating conditions.

- To present, in an easy way, the aspects related to Safety in the Operation of wind turbines.

- To act as a "*Test bench*", where the following can be forced: a) external conditions (extreme winds, for example), b) internal conditions (connection faults, equipment malfunction, etc.), and observe the wind turbine reaction, even of signals that are not accessible in real wind turbines.

As a consequence this Simulator, together with this Tutorial allows:

- **Knowing and exploring the internal structure** of this type of wind turbines.

- **Understanding the physical principles** on which the industrial wind turbines installed in Wind Farms are based.

- **Knowing the algorithms** used in each wind turbine subsystem and the parameters that characterize them.

- **Knowing the state machines** used for the wind turbine control.
