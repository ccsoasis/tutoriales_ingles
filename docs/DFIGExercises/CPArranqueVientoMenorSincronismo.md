---
tags:
- Cp
---

# With wind below the one necessary for operation at the Generator synchronism speed

!!! tip "🎯 Start-up with wind below the synchronism one"
    ***Objective:*** Study the DFIG behavior in the wind range between ~5.6 and 7.8 m/s, where the Power Train operates in **subsynchronous** mode.
    ***What to observe:*** The Cp evolution (always at its maximum), the rotor flux (same direction as the mechanical shaft), and the power that the RSC supplies to the rotor.
    💡 In this range the MPPT algorithm always keeps the Cp at its maximum value. Check it in the "Cp vs TSR and Pitch" panel.

As can be seen in the following graphs, this case corresponds to winds between about 5.6 and 7.8 m/s.

![](<lib/Viento para punto B.jpg>)

![](<lib/Viento para rpms sincronismo espanol.jpg>)

Note that it corresponds to the MPPT algorithm application zone, and therefore the Cp always remains at its maximum value, when the steady state is reached.
