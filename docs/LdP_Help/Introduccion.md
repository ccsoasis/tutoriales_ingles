---
tags:
- datalogging
---

# Introduction

### Introduction

**LdP** is a development and execution environment for Real Time Simulators, developed by Automated Computing Machinery S.L. ([www.acm-sl.com](https://www.acm-sl.com)) (ACM SL in the rest of this document).

Its main features are:

- It is a Windows Desktop application.

- It is based on the extensive use of Windows ActiveX components, and DLLs. These components can be developed in various programming environments (MS Visual Studio VC++, Visual Basic, Delphi, etc.)

- Each Simulator is described in a configuration file.

- The connections of the configuration file components can be edited at any moment, even while the simulation is running. The connections mimic the connection concept between electrical or electronic components: the outputs of some can be connected to the inputs of others. Both the output and input connections are called "signals" in LdP. The signal names have a three-field nomenclature: "*ComponentName*"."*ProcessWithinComponent*"."*OwnName*". For example: "*Controller.Control.PitchOut*" refers to an output named "PitchOut", of the "Control" process, of the "Controller" component, declared in the configuration file.

- The basic functionalities, available for each Simulator without additional programming, are:

-   - Real-time record of the changes in each one of the signals (*datalogging*) in normalized database files.

-   - Availability of record forms (*Recorders* or *StripRecorders*) through which the signal evolutions are visualized, in real time.

-   - Connections and parameters can be changed during the execution of the simulation, without the need to restart it.
