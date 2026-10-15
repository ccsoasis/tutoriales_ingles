---
tags:
- low speed connection
- grid disconnection
- cutout
- grid connection
- cutin
---

# Being in production, wind modification to change the Generator connection from Large to Small

!!! tip "🎯 Change from 1500 to 1000"
    ***Objective:*** Understand the inverse transition and why the system returns to 1000.
    ***What to observe:*** Return condition, stability, states and power/speed evolution.
    ***What to note:*** Return threshold and time until stable regime.
    💡 Check whether the return is made for safety, for efficiency or for speed control.

!!! warning "❓ Guiding questions"
    1. How much time elapses in the generator/mode change from high wind (&gt; 7 m/s) to low wind (&lt; 6.2 m/s)?
    2. What variable or condition marks the exact change instant?

This practical class carries out an operation similar to the one described in [Being in production, wind modification to change the Generator connection from Small to Large](Cambiode1000a1500.md), but with a wind speed evolution from higher to lower.

Use the "Page Up" key to reduce the wind speed below 6.2 m/s, which corresponds to the "Min for large generator" value (see [Functional wind values](../DSASTutorial/DatosTecnicosValoresVientos.md)). For example, leave it at 6 m/s.

In a recorder with the "Cutin + Cutout + Production" panel you will be able to see the following signal evolution.

![](<lib/Paso-12-6-MS.jpg>)

You can observe how first a grid disconnection occurs (cutout), preceded by a pitch value change that lowers the power obtained from the wind. Once the Thyristor Bypass Contactors deactivation has occurred, the generator connection type change occurs, from 4 poles (Large generator) to 6 poles (Small generator). The pitch value causes a power train deceleration, which is maintained until the generator shaft turning speed "drops" below the synchronous speed (now 1,000 rpms). From that moment the Controller follows a normal grid connection process (cutin).
