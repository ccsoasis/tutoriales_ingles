---
tags:
- brake hydraulic circuit
- brake circuit pressure
---

# Normal operation observation

!!! tip "🎯 Excessive losses fault observation"
    ***Objective:*** Analyze a fault caused by excessive losses in the system.
    ***What to observe:*** Variables that destabilize first and generated alarms.
    ***What to note:*** Evidences that allow concluding that the origin is an excessive loss.
    💡 look for coherence between pressure, flow and actuator response.

!!! warning "❓ Guiding questions"
    1. When a stop process is started while in production, is the hydraulic brake used?
    2. What criterion does the controller use to detect a problem in the hydraulic system and which variables does it monitor?

In this practice the objective is to observe the brake circuit behavior in a normal situation.

You must make sure the wind turbine is in production (connected to the grid) and observe the "*Brake circuit pressure*" indicator in the "*SynopticDriveTrain*" synoptic. Likewise make sure you have a recorder with the "*Brake hydraulic circuit*" panel.

Note that the hydraulic circuit pressure is kept in the green zone, with an evolution that is the following.

- While the pump is not active, the pressure descends very slowly (which corresponds to a circuit with very few pressure losses), until its value drops below the green zone minimum value.

- When the value drops below the green zone minimum value, the Controller starts the pump, which quickly makes the pressure rise.

- When the pressure becomes higher than the green zone maximum value, the Controller stops the pump.

The following figure is an example of the involved signal evolution.

![](<lib/PanelCircuitoHidraulico-ciclo-normal.jpg>)
