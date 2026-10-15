---
tags:
- PitchOut
- blade angle
- SynopticDriveTrain
---

# Indicator connections

The following figure shows the connections related to the blade angle.

The Controller has an output variable (*Controller.PitchOut*) that in reality goes to the servo-system that physically modifies the blade angle. In the simulator, this pitch mechanism is part of the nacelle simulator (*Nacelle*) and that Controller signal reaches it through *Nacelle.DriveTrain.PitchIn* passing through the "*Blade angle*" indicator that is in the "*SynopticDriveTrain*" synoptic. This indicator is normally in "*presentation only*" mode, so that it presents the value indicated by the Controller. But it can be put in "command" mode (F6), in which case the value that the pitch mechanism follows can be varied by changing the *slider* position, or by changing the text. In this way it is possible to force error situations.

![](<lib/Esquema conexiones Pitch.png>)
