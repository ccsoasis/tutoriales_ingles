---
tags:
- orientation operation
- manual turn
- SynopticWindNacelle
- incident history
- recovered
- NacelleYawing.CWYawingSpeed
- NacelleYawing.CCWYawingSpeed
---

# Manual orientation

!!! tip "🎯 Manual orientation (Yaw)"
    ***Objective:*** Understand the manual orientation control and its operational limits.
    ***What to observe:*** System response to manual commands and permission states.
    ***What to note:*** In which conditions the system allows or blocks the manual action.
    💡 compare behavior in automatic and manual mode.

In this practice you must use the "**Manual turn**" buttons in the "*Control Terminal*" to command the Nacelle turn manually. The arrows in each one of them indicate the turn direction.

![](<lib/ControlTerminal-espanol-parado.jpg>)

Make sure to visualize at the same time the "*SynopticWindNacelle*" synoptic and a recorder with the "Yawing" panel.

![](<lib/SynopticWindNacelle espaol.png>)

![](<lib/RegistradorYawing-con-valores.jpg>)

Observe that the Nacelle turns when you use the "Manual turn" buttons. When one of these buttons is pressed the corresponding indicator is indicated as active in "*SynopticWindNacelle*", and in the recorder.

As an exercise, keep one of the "Manual turn" buttons pressed. Check that the Nacelle stops turning when the number of power cable turns reaches the physical limit (3.5 turns). If this case occurs you will see that an "Open incident" appears with description "**Cables max twisting**". If you press the other "Manual turn" button you will see that this incident passes to "*Recovered*", and that you must fill in the "Ok" box so that it passes to "*Incident history*".

The turn speed (in degrees per second) is determined by the "*NacelleYawing.CWYawingSpeed*" and "*NacelleYawing.CCWYawingSpeed*" parameters. The default values, identical in both directions, is 10 degrees/second. In a real wind turbine this speed is around 0.5 degrees/second.
