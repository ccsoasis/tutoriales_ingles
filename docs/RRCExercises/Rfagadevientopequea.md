---
tags:
- wind gusts
- duty cycle
- PWM
- force
---

# Small wind gust

!!! tip "🎯 Small wind gust"
    ***Objective:*** Observe the wind turbine response with 6 m/s starting wind against a slow, small-amplitude gust (StandardGust120x4: +4 m/s in ~30 s), and check that the RRC control remains in "squirrel cage" mode (PWM = 100%) during the whole gust.
    ***What to observe:*** In the "General" recorder: the generated power shape with respect to the wind profile, the DutyCycle value (always 100%) and the small Pitch changes.
    💡 If the PWM remains at 100% during the gust, has the rotor resistance control acted?

!!! warning "❓ Guiding questions"
    1. Does the generated power profile faithfully follow the wind evolution during the gust? What does that indicate about the system response capacity?
    2. Does the DutyCycle (PWM) change at any moment of this gust? Why does the resistance control not act?
    3. Does the Pitch vary during the gust? In which direction and how much? What function does that small change fulfill?

In this practice we start from the wind turbine in production with 6 m/s wind. See [Grid connection sequence (cutin) with wind below the nominal](SecuenciadeconexinalaRedcutincon.md).

We will select the gust named "StandardGust120x4" that will increase the wind up to a maximum additional value of 4 m/s, which occurs in approximately 30 seconds, and then it will decrease to 0 m/s.

To do so:

- 1.In "*SynopticWindNacelle*" select the "*Wind gusts*" option and place yourself on "*StandardGust120x4*". There you can choose between "*Edit*" or "*Force*". If you choose "*Edit*" you will be able to see this gust variation profile. As in the following figure:  
![](<lib/RRC wg 120x4.jpg>)

- 2.Choose "*Force*" and observe in the "General" recorder the evolution of the different key variables. You must obtain a graph like the following.  
![](<lib/Evolucion rafaga 120x4 con viento 6.jpg>)

Comments:

- Note that the generated power profile follows the wind evolution.

- Note that the IGBT *DutyCycle* (the *PWM* signal) always remains at 100%.

- Note that the wind variation causes a small Pitch variation.
