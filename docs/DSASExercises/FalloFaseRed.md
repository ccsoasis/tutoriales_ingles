---
tags:
- WTElectricalPanel
- electrical cabinet
- thyristor bypass
---

# Observation of the reaction to a fault in one of the grid phases

!!! tip "🎯 Grid phase fault"
    ***Objective:*** Understand the system behavior against the loss or fault of a grid phase.
    ***What to observe:*** Electrical alarms, generator/converter state and transition to safe mode.
    ***What to note:*** Final state, alarm type and conditions necessary to reset.
    💡 relate the fault with the electrical protection mechanisms.

In this practice the objective is to observe the Controller reaction to a grid fault.

Visualize the "*Electrical cabinet*" synoptic.

![](<lib/Armario electrico frontal.png>)

The three checkboxes below "*Thyristor bypass*" allow "opening/closing" each of the three grid phases.

Place the wind turbine in production (see [Set the conditions for the Production entry with low wind to occur](CutinVientoBajo.md)).

Change the state of any of these three checkboxes and observe that the Controller starts, with a few seconds delay, a generator grid disconnection process (cutout).

In the "Control Terminal" synoptic *incidents* related to this protocol will appear. See the following figure.

![](<lib/CT-despues-fallo-red.jpg>)

If the phase is restored, the dates of the "*Recovered*" column will appear filled. These incidents must be manually "acknowledged" by the operator.
