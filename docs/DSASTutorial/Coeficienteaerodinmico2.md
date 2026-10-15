---
tags:
- active pitch
- active stall
---

# Control of the power collected from the wind

There are several methods to control the power taken from the wind: one method consists of controlling the blade angle (Pitch), since varying it modifies the aerodynamic coefficient (Cp) value. See [Aerodynamic coefficient](Conceptossobrelapotencia.md). This solution requires that each blade support to the Hub must have the capacity to rotate each of them on their longitudinal axis. This technique is known in the specialized literature as "***Active Pitch***". In Anglo-Saxon documentation this Pitch control method is called "*to the feathers*", since to lower the Cp the blade is made to "fold to the wind", that is, the blade angle is made to follow the wind, so that it offers the least surface against it.

There is another technique that also uses the Pitch change mechanism but that, instead of being based on "folding to the wind", uses another effect (see [Entry into losses (Stalling)](Stalling.md)). In the 3D graphs of [Cp](Conceptossobrelapotencia.md), this zone corresponds to the "hidden wall" that corresponds to negative Pitch values.

This control method is called "***Active Stall***" and is the one used in the wind turbine on which this Simulator is based.

## Implications for a wind turbine with squirrel-cage Generator.

In the case of a squirrel-cage induction machine used as a Generator (case of this Simulator), its operating speed is above, but very close to, its synchronous speed (see [Introduction to induction machines](IntoductiontotheInductionMachine.md)). This synchronous speed, in the most installed wind turbines, is typically between 1000 rpms and 3000 rpms, depending on the grid frequency and the Generator pole number.

In the particular case of this Simulator electric Generator it has two stator winding connections: one that "creates" 3 magnetic pole pairs in the air gap, and another that creates 2 pole pairs. The synchronous speeds when connected to a 50 Hz grid are, therefore: 1000 rpms (= 50 Hz * 60 / 3) in one case and 1500 rpms (= 50 Hz * 60 / 2) in another.

The speed range at which this type of Generator produces its maximum power is typically below 2% of the synchronous speed (see [Characteristics of the Generator emulated in this Simulator](DatosTecnicosGenerador.md)), so the wind turbines that use this type of Generator are known as "**fixed speed**". Taking into account the first conclusion of the [previous section](Coeficienteaerodinmico.md), this implies that **this wind turbine does not present the best solution to take advantage of winds that are below the Nominal Wind**.

To alleviate this inadequacy, the fixed-pitch wind turbines use the idea of having two Generators that can operate at two different speeds, or a single one but that can operate at two speeds. With this it is possible to use one of them for winds close to or above the Nominal Wind and another that makes the TSR be reached at the optimum for a wind quite below the Nominal Wind.

In the case of this Simulator, in which the Nominal Wind speed is around 11 m/s, and the blade rotation speed, for that power, is 19.4 rpms, using the stator connection for synchronism at 1500 rpms (2 poles). Therefore, when the connection is changed to 3 poles the wind for which the optimum TSR is reached is around 7.3 m/s (= 11 m/s * (1000 rpms / 1500 rpms)).

This technique has proven very efficient in practice, so this wind turbine modality was widely spread before the variable-speed wind turbines.

In the following figure the relationship between wind and Pitch in a wind turbine that uses "*Active Pitch*" (<mark>green curve</mark>) is shown. The relationship between the power obtained as a function of the wind (<mark>gray curve</mark>) is also represented, as a result of applying the corresponding Pitch values for the same wind.

![](<lib/Panel Potencia y Pitch vs Viento espanol.jpg>)

Fig 1.

There is another control method based on the blade design, which uses the "entry into losses" (stalling) concept, which is described in [Entry into losses (Stalling)](Stalling.md).

A third method consists of forcing the entry into losses also by varying the Pitch: this technique is known as "***Active Stall***" and is also described in [Entry into losses (Stalling)](Stalling.md).
