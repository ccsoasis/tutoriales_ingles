---
tags:
- power factor
---

# Influence of the Reactive Power on the Generator

!!! tip "🎯 Influence of the Reactive Power on the Generator and B2B"
    ***Objective:*** Analyze how the changes in the "Desired Reactive Power" affect the rotor signals in the B2B, and understand why this capacity is a differential value of DFIGs.
    ***What to observe:*** The evolution of the "Electric variables 2: Rotor signals" signals when changing the reactive power between +726 kW, +305 kW, 0, -305 kW and -726 kW.
    💡 In this simulator all the reactive power "comes out" through the Stator. How does the B2B control it?

!!! warning "❓ Guiding questions"
    1. When changing the Reactive Power, which rotor variables change (modulus and/or angle)? Which remain the same?
    2. What is the difference between supplying positive and negative reactive power to the grid? How is it reflected in the grid current?
    3. Why does the capacity to control the reactive power have a significant economic value for the Electrical Grid operation?

The objective of this experiment is to see the influence of the changes in the "*Desired Reactive Power*" on the Back-to-Back converters.

Contrary to the "*Desired Active Power*" which can only be positive, and in a certain range, the "*Desired Reactive Power*" has a sign: that is, the reactive part of the current sent to the grid can be leading or lagging with respect to the voltage.

This characteristic of DFIG wind turbines derives from the Back-to-Back converters, which are Power Electronics elements. The reactive part of the grid current can be contributed both by the Generator Stator and directly by the GSC converter. In this simulator a common policy has been adopted, consisting of making all the grid reactive power "come out" through the Stator: this is achieved by changing the angle of the flux created by the Rotor winding, and facilitates the GSC design.

This characteristic is very important because for the Electrical Grid operation, being able to have Electrical Plants capable of supplying/consuming reactive power greatly helps controlling its stability. Due to this, the reactive power has an important value.

- Put the wind turbine in disconnection mode (press STOP if in production).

- Set the wind above the Nominal value (for example, 13 m/s).

- Open a Recorder and select the panel "*Electric variables 2: Rotor signals*".

- Press START.

- When the cutin operation ends, change "<mark>Desired Reactive Power</mark>" to 305 kW in the "*Control Terminal ...*" synoptic, typing directly (double click on the text, type "305" and press "Enter"). This value corresponds to a power factor of 0.98 for an active power of 1,500 kW.

- Let a few seconds (30) pass, to allow the signals to stabilize and now change the value to 726 kW, which corresponds to a power factor of 0.9.

- After another 30 seconds, change the value to -726 kW.

- After another 30 seconds, change the value to -305 kW.

- After another 30 seconds, change the value to 0 kW.

You must obtain a graph similar to the following:

![](<lib/DFIG Cambio Reactiva 90  98 -98 -90 0.jpg>)
