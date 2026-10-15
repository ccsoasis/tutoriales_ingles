---
tags:
- squirrel cage
- soft starter
- soft connection
---

# Operating principle of a wind turbine with squirrel-cage generator directly connected to the grid

The wind turbine object of this simulator uses a <mark>*short-circuited rotor induction electric generator*</mark> (also known as *squirrel cage* rotor), with the **stator directly connected to the grid**.

This type of generator, with this connection, determines the conditions in which the wind turbine operates and also its way of operating. In the graph of figure 1 the characteristic of this induction *machine* is shown, which can behave as a *motor*, if its shaft speed is a speed below the synchronism one, or as a *generator*, if it is above.

![](<lib/MaquinaInduccionParvsRPMs2Puntos.jpg>) Fig 1

Therefore, its use as a generator implies that an *external mechanical torque* source moves the shaft and keeps it above the synchronous speed. It has a more detailed explanation in [Introduction to induction machines](IntoductiontotheInductionMachine.md). The external mechanical torque source is, in this case, the wind incident on the blades, which makes them rotate. See more details in [Why do the blades rotate?](PFAPorquegiranlaspalas.md).

This type of machine and its grid connection way, also conditions the wind turbine '**operating**' way. By operating we now understand how and when the stator connection with the grid is made. It is necessary that the stator remains *disconnected* from the grid until the rotor shaft speed is immediately above the synchronous speed, since otherwise, it would behave as a motor. The above implies that the stator grid connection is a delicate operation in which the generator is kept without electrical load until the frequency of the voltage it generates, and its phase, coincide with those of the grid. This situation occurs in other electrical generation installations and is solved with a specific device. See [Soft starter (soft connection) to the grid](Softstarter.md).
