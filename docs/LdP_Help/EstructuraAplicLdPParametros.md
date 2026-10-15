---
tags:
- parameters
- output signal
- parameter
---

# Parameter Overview

## Parameters

The concept of parameters in LdP implements the idea of values that are used in certain processes and do not need to be changed often during the execution of a simulation. For example, the rotation speed of the motor that rotates the nacelle of a wind turbine clockwise.

![](<lib/Sinoptico parametros.jpg>)

Each parameter is an "*output signal*" declared in the configuration file, where they are given a name (e.g., "NacelleYawing.CWYawingSpeed" for the parameter mentioned above).

The above synoptic allows you to modify the value of each of these parameters within the range of values defined for each of them.
