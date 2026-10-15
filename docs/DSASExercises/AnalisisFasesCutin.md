---
tags:
- cutin
- inductive
- PAveInd
- RPM GENERATOR
- induction machine
- capacitive
- PAveCap
- active power
- PAveAct
- thyristor bypass contactors
- reactive power
- slip
---

# Detailed analysis of the grid connection phases (Cutin)

!!! tip "🎯 Cut-in phases analysis"
    ***Objective:*** Break down the start (cut-in) into phases and understand which condition triggers each transition.
    ***What to observe:*** Machine states, permissions and variable evolution during the start.
    ***What to note:*** State sequence, duration of each phase and the value that causes the change.
    💡 record the exact instant of each transition (previous state → next state).

!!! warning "❓ Guiding questions"
    1. How much time does the controller take to make sure the hydraulic brake system works?
    2. How much time are the thyristors in conduction (partial or total), approximately?

This practice uses real data from a wind turbine like the simulated one, taken with a sampling of 1 sample per second.

Fig 1, below, shows a temporal zoom corresponding to the generator grid connection. Fig 2 shows an enlarged detail with the interval immediately before and after the generator grid connection.

The objective is to observe how the key variable evolution is. In particular observe the abrupt change of the power train acceleration in this wind turbine type, and of the main electrical variables.

![](<lib/DataloggerCutin-completo.png>)

Fig 1.

The zone in <mark>blue</mark> shows how the Controller modifies the pitch value so that the power train acceleration (signal "*RPM GENERATOR*") is kept constant, until the connection is reached. The acceleration in this zone is of the order of 23 rpms/second (= (1500 rpms - 800 rpms)/ 30 seconds). When passing to production that acceleration is practically 0 rpms/second: this occurs because, in production, the power extracted from the wind is equal to the (electrical) power delivered to the grid. These values give an idea of the mechanical stress to which the power train components, and the Tower, are subjected at the grid connection moment.

Just when the generator connection occurs (first limited by the Thyristor conduction and then by the activation of the *Thyristor Bypass Contactors*) an (important) peak of "*Inductive*" type reactive power consumption occurs (signal "*PAveInd*"). This power corresponds to the current circulating through the generator stator in the initial moments, to constitute the magnetic flux necessary for the "*induction machine*" to exist.

Immediately afterwards a "*Capacitive*" type reactive power peak occurs (signal "*PAveCap*") characteristic of the slip adjustment (*slip*), from the synchronism passage (slip = 0) to the final value, corresponding to the mechanical power that forces the shaft. See [Introduction to induction machines](../DSASTutorial/IntoductiontotheInductionMachine.md). Note that the initial value of this power is significant with respect to the **active power** (signal "*PAveAct*") that is finally delivered to the grid.

The following figure shows the same signals but with a zoom with more temporal resolution, just at the connection moment.

![](<lib/DataloggerCutin.png>)

Fig 2.
