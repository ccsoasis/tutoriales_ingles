---
tags:
- controlled
- negative frequency
---

# Wind turbine start-up (cutin) with wind above the Nominal

!!! tip "🎯 Start-up with wind above the Nominal"
    ***Objective:*** Compare the DFIG behavior during cutin with wind above the nominal with the cases of lower wind, focusing attention on the operational curve and the generator mode.
    ***What to observe:*** The operating point in "Power vs RPMs" (point D), the Cp (far from its maximum), the Pitch (greater than 0°) and the rotor power flow towards the RSC.
    💡 With wind above the nominal, the Cp is not maximum. Why? What limitation does the Controller impose?

!!! warning "❓ Guiding questions"
    1. On which point of the Operational Curve does the system stabilize with wind above the nominal? Does it coincide with the MPPT line?
    2. Why is the Cp far from its maximum when the wind exceeds the nominal? What role does the Pitch play?
    3. In supersynchronous mode with high wind, what is the rotor signal frequency? Is it positive or negative? What does it mean?

The idea in this experiment is to repeat the previous experiments ([Wind turbine start-up (cutin) with wind below the nominal](CPArranqueconvientosbajos.md)) but with winds above the Nominal, focusing attention on the signal evolution in other synoptics:

- In the panels of the "*Operational curves for Variable Speed Wind Turbines*" synoptic:

- In the "*Doubly-fed induction generator with Back-to-Back converter*" panel, the rotor winding generates an electrical power that it delivers to the RSC, which acts as a "*controlled rectifier*" to feed the DC Link, while the GSC behaves as an inverter that takes the energy from the DC Link and creates a power that it sends to the grid.  
The Generator works in supersynchronous mode (slip < 0) and the rotor voltage and current have a "*negative frequency*", which reflects the fact that the magnetic flux vector that the rotor "sees" rotates in the opposite direction to the rotor shaft rotation direction.
