# Evolution of key variables

!!! tip "🎯 Evolution of key variables during start-up"
    ***Objective:*** Record in the StripRecorder the key signals during the cutin operation with low wind (~7 m/s) and measure the production start time.
    ***What to observe:*** Pitch, mechanical and electrical powers, brake signal, generator RPMs, real and effective wind.
    💡 Use the "Set as time reference" function of the recorder to accurately measure the operation duration.

!!! warning "❓ Guiding questions"
    1. How long does the wind turbine take from brake release to production stabilization with 7 m/s?
    2. What happens to the Pitch during start-up? At what value does it stabilize when the MPPT point is reached?
    3. When do the real wind and the effective wind diverge? When do they converge? What does that convergence indicate?

Repeat the practice [Evolution in the Power vs rpms plane](CPArranqueVientoMenorSincPotRPMs.md) but focus your attention on the variables recorded in the "Registradores_X" synoptic corresponding to the Panel "Cutin + Cutout + Production: Panel to monitor cutin and cutout operations".

- If the simulator is running, press STOP and wait for the Power Train to stop.

- If a striprecorder with the panel "*Cutin + Cutout + Production: Panel to monitor cutin and cutout operations*" is not visible, open one. See [Practical classes](Clasesprcticas.md).

- Set the wind to 7 m/s.

- Check that there are no "Incidents" to acknowledge other than "Manual STOP". Otherwise acknowledge them. Press START in the Control Terminal.

- In the striprecorder you will be able to see the evolution of the following signals:

- When the system reaches the connection point and stabilizes you will be able to see an evolution of these signals as shown in the following figure.

![](<lib/Evolucion de cutin a 7 ms.jpg>)

- Measurement of the time in which the production start operation was carried out: Make a working copy (Registradores_X -> Copy) of the striprecorder.  
On this copy mark the time origin (right mouse button, "Set as time reference" option) previously placing the recorder cursor on the edge where the brake release signal changes (yellow line). From that moment, when moving the cursor the time delta with respect to the chosen reference instant will be indicated. You can see that in this case, with the 7 m/s wind the time used is in the order of 186 seconds.

![](<lib/Evolucion de cutin a 7 ms - medida tiempo cut.jpg>)

In a later practice you will be able to check how this value depends not only on the wind but also on the Power Train "Moment of Inertia", which depends on physical parameters, such as the blade length, their weight, the Hub weight, etc.
