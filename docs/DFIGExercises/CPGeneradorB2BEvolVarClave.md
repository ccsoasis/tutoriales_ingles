# Evolution of key variables with the wind

!!! tip "🎯 Evolution of the Generator and B2B variables with the wind"
    ***Objective:*** Observe how the generator electrical variables (powers, currents, angles) change when the wind descends from supersynchronous to subsynchronous, especially at the synchronism speed crossing.
    ***What to observe:*** The Rotor Power sign, the rotor current angle, the rotor voltage near synchronism, and the sub/supersynchronous transition.
    💡 What happens to the rotor voltage exactly at synchronism? And to the current?

!!! warning "❓ Guiding questions"
    1. When is the Rotor Power negative? When is it positive? What does the sign indicate in terms of energy flow?
    2. What happens to the rotor voltage when the RPMs approach the synchronism speed? Is it consistent with the theory?
    3. How does the rotor current angle vary between supersynchronous and subsynchronous mode?

- Put the wind turbine in disconnection mode (press STOP if in production).

- Set the wind above the Nominal value (for example, 13 m/s).

- Open a Recorder and select the panel "*Electric variables: Monitoring the variables of the Generator and B2B*".

- Press START.

- When the grid connection occurs, begin to slowly decrease the wind using the "Down arrow" key (press it with a cadence of 1 time every 2 seconds). You will obtain a graph similar to the following.

![](<lib/DFIG Evolution Generador y B2B.jpg>)

## Comments

- The graph includes the cutin phase: the observations that follow correspond to the part of the graph in which the wind turbine is already in production, that is, from when the wind begins to descend.

- There are significant changes around the wind at which the operation at synchronous speed occurs (in this case 1500 rpms).

- When the Generator rpms are above synchronism (supersynchronous mode), the sign of the Rotor Power is negative: this indicates that the power "comes out" of the rotor. When the rpms are below (subsynchronous mode), the Rotor Power is positive, which means it "enters" the rotor.

- The rotor current angle is always positive. The Rotor Power sign change comes from the sign change in the rotor voltage.

- The rotor current angle varies between about 180º (that is, in the opposite direction to the Stator voltage angle, which is the one taken as reference for the angles) when we are supersynchronous, to about 0º in subsynchronous.

- At the synchronism speed, the rotor voltage is very small (almost 0 V) in effective value. However, the rotor current is notable.

The following graph is obtained by the same procedure as the previous one but using the "*Electric variables 2*" panel. It shows the Active and Reactive Powers, the Rotor and Stator ones, in modulus and angle, the evolution of the Rotor signal frequency.

![](<lib/DFIG Evolution Generador y B2B 2.jpg>)
