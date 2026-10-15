---
tags:
- cutout
- grid codes
- overspeed
- VCU
---

# Evolution against long voltage drops

!!! tip "🎯 Evolution against long voltage drops"
    ***Objective:*** Observe how the DFIG Controller reacts to a long-duration voltage drop (more than 1 second) in one grid phase, and analyze the orderly disconnection protocol that is activated.
    ***What to observe:*** The rapid drop of the electrical power to 0, the Power Train RPMs surge, the Pitch actuation to limit that surge, and the possible activation of the VCU signal.
    💡 Why does the sudden loss of electrical load cause an increase in the RPMs?

!!! warning "❓ Guiding questions"
    1. How long does the Controller wait before starting the disconnection when it detects the voltage drop? Why does it wait that time?
    2. Why do the Power Train RPMs increase sharply when the electrical power drops to 0?
    3. What distinguishes this emergency stop from a normal ordered stop (for example, the one in the "Stop with wind below the Nominal" experiment)?

Most of the currently installed DFIG wind turbines have the capacity to face grid micro-cuts, known as *Low-Voltage-Fault-Ride-Through*, as described in [Grid codes](../DFIGTutorial/RedElectricaExigenciasGridCodes.md). These micro-cuts have a duration of less than a second. If the voltage drop lasts longer, the Controller implements an orderly disconnection (*cutout*) protocol.

This experiment shows the evolution of the electrical power and the Power Train rpms during this cutout phase.

If eventually the voltage drop is longer than allowed, and out of the profile described there, then the Controller implements a protocol that basically consists of the initiation of a normal Cutout (orderly disconnection from the Grid).

In this experiment you should provoke such case, observe the reaction of the Controller and learn what should be done in a real WindTurbine.

- Put the wind turbine in disconnection mode (press STOP if in production).

- Set the wind above the Nominal, e.g., 13 m/s.

- Press START.

- Wait for the grid connection.

- Create a voltage drop in any phase: show the "*Electrical cabinet ...*" synoptic and press any of the checkboxes marked "F1", "F2" or "F3", so that it remains unchecked. Keep this situation for at least 3 seconds.

You must obtain a graph similar to the following:

![](<lib/DFIG Fallo de fase.jpg>)

### Comments:

During a short period of time after the voltage drop has been detected, the Controller waits for the voltage to recover. If this does not happen, a rapid disconnection is started. Unlike other disconnections (see for example the [Stop with wind above the Nominal](CPVientoSupNominal.md) experiment), in this case, the electrical power drops rapidly to 0 and this causes a Power Train rpms surge, due to the loss of load equivalent to the electrical power that was being sent to the grid. The Pitch rises as fast as it can (that is, we force lowering the Cp and therefore the mechanical power taken from the wind) to try to reduce this rpms surge.

Eventually the Controller may receive the Power Train overspeed notification (VCU signal), which would trigger the start of another stop operation, of higher priority, that includes the use of the brake.
