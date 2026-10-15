---
tags:
- generator
- power cables
- cable unwinding
- anchoring
- maximum allowed turn value
- substation
---

# Power cables

Details of the power cables and associated sensors.

The Generator connects to the Electrical Grid through the **power cables**, which "hang" from the nacelle (where the Generator is) down to the Tower base, where the transformer that raises the Generator voltage (690 V) up to a Medium Voltage value (15 kV / 22 kV) is, which is where the cable that joins it with the Farm electrical Substation connects.

Since the nacelle has to yaw to the wind, its position is not fixed, so these power cables internal to the wind turbine twist in the descent from the nacelle to the Tower base, depending on the wind direction. See the following figure.

![](<lib/Lapp_Wind_Portfolio.jpg>)

![](<lib/Cables esquema bajada.png>)

![](<lib/Long-loops-of-Lapp-cable-in-a-nacelle.jpg>)

These cables have two fixed **anchoring** points, one on each side of the nacelle base, which is the zone where this twisting occurs. Logically, there is a maximum turns value, which is typically **2.5 turns in each direction**.

There is no sensor of these cables turns number, but the maximum limit is detected through a limit switch that is fixed to the Tower, and whose sensing end is tied to the final end of the cable rotation zone.

The Controller uses the state of this limit switch to automatically stop the wind turbine, and start the **cable unwinding** process. See [Yaw and Power Cable unwinding control algorithms](Yawingofthenacelle.md).
