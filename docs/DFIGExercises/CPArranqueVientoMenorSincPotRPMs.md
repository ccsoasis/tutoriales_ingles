# Evolution in the Power vs rpms plane

!!! tip "🎯 Evolution in the Power vs RPMs plane"
    ***Objective:*** Observe how the operating point moves from start-up to stabilization on the MPPT curve in the "Power vs RPMs" panel.
    ***What to observe:*** The trajectory of the Mechanical Power indicator (cross) and Electrical Power (circle) until both coincide on the Operational Curve.
    💡 Compare the small difference between mechanical and electrical power: what is it due to?

!!! warning "❓ Guiding questions"
    1. On which line of the operational curve does the operating point stabilize? Does it coincide with the Maximum Power line (blue)?
    2. What is the difference between the wind Mechanical Power and the Electrical Power sent to the grid? Where is that energy lost?
    3. What value does the Cp have at the stable point? Is it its maximum? Check it in the "Cp vs TSR and Pitch" panel.

- If the simulator is running, press STOP and wait for the Power Train to stop.

- If it is not running, start it (in "Executing .." press "Run").

- Set the wind below 7.8 m/s, for example, at 7 m/s.

- Check that there are no "Incidents" to acknowledge other than "Manual STOP". Otherwise acknowledge them. Then press START in the Control Terminal.

- Make the "Operational Curves" synoptic visible (In "Control Terminal ..." press "*Work Curves*").

- Observe the evolution of the Wind Mechanical Power indicators (cross) and of the Electrical Power sent to the grid (circle), in the Power vs rpms panel (upper left). Also follow the evolution of the Cp value as a function of the TSR and the pitch (lower left panel).

- Wait for these two indicators to stabilize: you will see that then both practically coincide.

- You will obtain a graph similar to the following.

![](<lib/Curvas operacionales estables a 7 ms.jpg>)

Note the following details:

1. The electrical power delivered to the grid is slightly lower than the one taken from the wind. The difference corresponds to the power dissipated in the Generator and the B2B. Check it in the "Doubly-fed induction generator with Back-to-Back converter" synoptic, as shown in the following figure.

![](<lib/Potencia de perdidas en rotor y estaro con vi.jpg>)

2. The stable operating point is on the Operational Curve (red line), which in this section coincides with the Maximum Power line, according to the MPPT algorithm (blue line). And therefore:
