---
tags:
- moment of inertia
---

# Influence of the Power Train Moment of Inertia

!!! tip "🎯 Influence of the Power Train Moment of Inertia"
    ***Objective:*** Check how the Power Train Moment of Inertia (parameter "Nacelle.DriveTrain.MomentOfInertia") affects the wind turbine response speed against wind gusts.
    ***What to observe:*** The acceleration speed during start-up and the RPMs response against "Standard120x4" type gusts with two different Moment of Inertia values.
    💡 Lower Moment of Inertia → faster or slower response? And against gusts?

!!! warning "❓ Guiding questions"
    1. With a Moment of Inertia of 2,500,000 kg·m² (vs 3,500,000 by default), how much does the start-up time until grid connection change?
    2. How does the lower Moment of Inertia affect the amplitude of the RPMs variations against a wind gust?
    3. What real physical factors of the wind turbine determine the Moment of Inertia? What circumstances can modify it in real operation?

The Power Train (Hub + Blades + Hub-to-Gearbox connection + Gearbox + Generator) has a *Moment of Inertia*, which depends on the weight distribution of these components and their distance from the rotation axis.

The *Moment of Inertia* value does not influence the power that can be obtained from the wind, but it does influence the wind turbine response speed against changes, for example, during wind gusts. It can change due to blade changes, or due to the presence of ice on them.

In this experiment the influence of the *Moment of Inertia* changes on the Power Train rpms evolution under the influence of wind gusts is checked. The Moment of Inertia value is controlled by the parameter "*Nacelle.DriveTrain.MomentOfInertia*".

To do so, repeat the wind turbine start-up with a high wind (e.g., 13 m/s) and apply a long gust (*Standard120x4*) with two values of "*Nacelle.DriveTrain.MomentOfInertia*": first with the default value (3500000 kg * m<sup>2</sup>) and then with a different value and you will obtain a graph similar to the following (the second value used is 2500000).

![](<lib/DFIG 2 momentos de inercia.jpg>)

## Comments:

It can be observed that the influence is quite noticeable in the Power Train rpms evolution, during the rising ramp until reaching the grid connection. When the Moment of Inertia is lower, this ramp is faster. It also has influence on the response to gusts. As expected, the Pitch evolution is small.
