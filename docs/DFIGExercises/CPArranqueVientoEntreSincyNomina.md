---
tags:
- synchronous
- supersynchronous
---

# With wind below the nominal but above the synchronism one

!!! tip "🎯 Start-up with wind between synchronism and nominal (~7.8–11.2 m/s)"
    ***Objective:*** Observe the DFIG behavior in **supersynchronous** mode in the wind range between the synchronism speed (~7.8 m/s) and the nominal (~11.2 m/s), distinguishing the A-C and C-D sections of the operational curve.
    ***What to observe:*** The rotor flux direction (now opposite to the mechanical shaft), the RSC power sign, and how the operating point evolves in the Power vs RPMs plane.
    💡 In this range the RSC "receives" power from the rotor: what does that mean in terms of energy flow?

!!! warning "❓ Guiding questions"
    1. In which direction does the rotor flux vector rotate with respect to the mechanical shaft in supersynchronous mode? Why?
    2. What difference do you observe in the stable operating point between the 7.8–9 m/s section (A-C) and the 9–11.2 m/s section (C-D)?
    3. Why does the Operational Curve separate from the Maximum Power line (blue) from point C?

In this practice the experiments described in [Evolution in the Power vs rpms plane](CPArranqueVientoMenorSincPotRPMs.md), [Evolution of key variables](CPArranqueVientoMenorSincVarClav.md) and [Evolution of the Magnetic Fluxes in the Generator and of the B2B signals](CPArranqueVientoMenorSincFlujos.md) must be repeated, but the wind range must be between 7.8 m/s and 11.3 m/s, as can be deduced from the two following graphs. First in the section between 7.8 m/s and 9 m/s (from synchronism to point C) and then in the section 9 m/s and 11.2 m/s (point C to point D).

The wind at which the Power Train target speed corresponds to the electric Generator synchronism speed, for this case, is around 7.8 m/s (see [With wind below the one necessary for operation at the Generator synchronism speed](CPArranqueVientoMenorSincronismo.md)).

![](<lib/Viento para rpms sincronismo espanol.jpg>)

![](<lib/Curvas operacionales Viento nominal espanol.jpg>)

As can be seen in the Operational Curve graph, in this wind range there is a slope change, in which said curve separates from the derivative of the Maximum Power algorithm (blue line), at the point marked C. The corresponding wind is somewhat below 9 m/s.

![](<lib/Curva operacional Potencia vs RPMs.png>)

In this practice you must repeat the previous experiment but placing the wind first in the section between 7.8 m/s and 9 m/s (from synchronism to point C) and then in the section 9 m/s and 11.2 m/s (point C to point D).

In both sections you will be able to check in the "*Induction generator ...*" synoptic that the rotor current flux (green vector) rotates in the opposite direction to the Power Train shaft rotation direction: this indicates that we are in the zone above synchronism (supersynchronous).

You will also be able to check that the RSC "receives" power from the rotor: that is, part of the mechanical power that forces the Power Train "comes out" through the generator rotor.

![](<lib/B2B con viento a 11 3 ms.jpg>)
