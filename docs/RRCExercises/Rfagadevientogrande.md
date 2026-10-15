---
tags:
- duty cycle
- PWM
---

# Large wind gust

!!! tip "🎯 Large wind gust"
    ***Objective:*** Observe the wind turbine response against a large-amplitude gust (StandardGust60x10: +10 m/s) that exceeds the nominal wind, and check how the RRC control stabilizes the power at the nominal value by modifying the IGBT DutyCycle.
    ***What to observe:*** The moment the wind exceeds the nominal, the power stabilization at 660 kW, the DutyCycle (PWM) changes and the associated generator RPMs changes.
    💡 When the wind exceeds the nominal and the power is set at 660 kW, which variable absorbs the excess wind energy?

!!! warning "❓ Guiding questions"
    1. From which wind speed does the power stop following the wind and stabilizes at 660 kW? Is it the nominal wind?
    2. How does the DutyCycle (PWM) vary when the wind exceeds the nominal? Does the rotor effective resistance increase or decrease?
    3. Do the generator RPMs increase during the gust? Why does the mechanical power excess not exceed the nominal but does increase the RPMs?

In this practice the objective is to repeat the [Small wind gust](Rfagadevientopequea.md) practice but with a stronger wind gust. In this case we will use the one named "*StandardGust60x10*", whose profile is the following:

![](<lib/Standard60x10.jpg>)

You must obtain a graph similar to the one in the following figure.

![](<lib/Evolucion rafaga 60x10 con viento de 5.jpg>)

## Comments:

- Note that when the wind exceeds the nominal (around 12 m/s) the power is stabilized at the nominal power (660 kW) and that what is modified is the IGBT *DutyCycle* (*PWM*). This is accompanied by generator shaft rpms changes. That is, the gust part not compensated by the Pitch is compensated by the rpms increase.
