---
tags:
- main switch
- grid
- thyristors
- bypass contactors
- contactors
- over temp
- gate control
- bimetallic
- bypass
- soft starter
- manual
- safety
---

# Connection circuit detail

The following figure shows a detail of the electric Generator grid connection.

![](<lib/Conexion electrica de potencia en un aerogene.png>)

Fig 1

The main components are:

- 1.The "*Main switch*" that connects with the Grid, on the left of the figure.

- 2.The *Thyristor* block and its *Bypass contactors*, which are part of the [Soft-starter](Softstarter.md), the soft grid connection mechanism.

- 3.The thyristor temperature sensors.

- 4.The contactor block for the Generator connection change between 4 and 6 poles.

- 5.The Controller, which monitors the state of these elements and generates their control signals.

### Important details:

- The "*Main switch*" can be put On or Off manually. Being On it can be switched to Off from the Controller, through the "*Main Circuit Breaker Reset*" signal. This occurs when the Controller executes some Safety sequence.

- The *contactors* have a mechanism to report their state to the Controller, consisting of two contacts attached to the main *contactors*: one named "NC" and another "NO". The wire connected to the "NO" terminal is active (has voltage) when the contactor is in Off mode, while the "NC" is active (has voltage) when the contactor is in On mode. These two signals reach the Controller and serve to:

- ○Know the contactor state (open or closed).

- ○Know if there is any circuit error: that is, if there is any broken cable or the corresponding contacts in the contactor are damaged, etc. The logic of this detection is explained in [Contactor problem detection logic](Detalledelcircuitodeconexin.md).

- The Thyristors have *bimetallic* type temperature sensors, which open when the temperature exceeds a certain value. These sensors are connected in series to the "*Over Temp*" Controller input, so this signal is "closed" if the temperature *in all* the Thyristors is below the limit, and "open" if *in any* of the Thyristors that limit has been exceeded.

- The "*Gate Control*" signal is actually 6 signals that are applied to the corresponding Thyristor gates, as explained in [Soft starter (soft connection) to the grid](Softstarter.md).
