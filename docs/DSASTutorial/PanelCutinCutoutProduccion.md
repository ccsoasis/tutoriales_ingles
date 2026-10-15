---
tags:
- nacelle orientation
- wind direction
- power cables
- right turn of the nacelle
- left turn of the nacelle
---

# Panel 'Yawing'

The following figure shows the panel called **'Yawing'**, which contains 2 channels.

![](<lib/RegistradorYawing.jpg>)

- 1.In the first 'channel' two signals are presented:

- 1.The **wind direction**.  
Signal "SynopticWindNacelle.WindDirectionOut". The value of this signal is between 0º and 360º.

- 2.The **nacelle orientation**.  
Signal "Nacelle.Yawing.OrientationOut". The value of this signal can be between -900 and 900, to take into account the number of power cable turns.

- 2.In the second 'channel' three *digital* signals are presented, corresponding to:

- 1.The activation signal of the limit switch associated with the **power cables**, which is activated when the absolute maximum number of turns has been reached, in either of the two directions.

- 2.The activation signal of the **nacelle right turn** (CW) motor.

- 3.The activation signal of the **nacelle left turn** (CCW) motor.
