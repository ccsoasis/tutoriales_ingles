---
tags:
- low speed
- large generator
- small generator
- power factor
- nominal power
- TSRoptimo
- gearbox
---

# Detailed analysis of the speed change mechanism (change Small Generator to/from Large)

!!! tip "🎯 Generator changes analysis"
    ***Objective:*** Understand why the system changes mode/generator and its effect on power and stability.
    ***What to observe:*** Modes/states, power setpoint, rotor speed and change criterion.
    ***What to note:*** When the change occurs, which threshold triggers it and how it stabilizes afterwards.
    💡 Look for whether the change occurs by fixed threshold, hysteresis or safety condition.

!!! warning "❓ Guiding questions"
    1. How much time elapses in the electrical generator connection change operation from low wind (below 6.2 m/s) to high wind (above 7 m/s)?
    2. The same question, but going from high wind to low wind.

In this practice the objective is to study the concepts around the generator connection type change (between 4 and 6 magnetic poles).

The base reason is to have a better use of the wind. As presented in Fig 1 of [By Active Pitch (to-the-feathers)](../DSASTutorial/Coeficienteaerodinmico.md), for a certain blade, there is an optimal value between the wind speed and the blade turning speed (*TSRoptimo*).

Observe that the relationship between the generator shaft turning speed and the blades one is fixed (the multiplier relationship). And that, on the other hand, when in production the generator is kept very close to the synchronous speed. Check that with a high wind (17 m/s) the power is the nominal (1,300 kW) and the generator speed is 1,509.7 rpms: that is, the slip for maximum power is barely 0.65% (= (1509.7 / 1500) -1). The result of these two observations is that the blades are forced to work at *constant speed*.

In order to obtain a better use of the wind, the blade design of this wind turbine type is special, so that the zone corresponding to the *TSRoptimo* is not a point but has a wide range. In any case, this range does not cover a relationship between the nominal wind (around 14 m/s in the real wind turbine) and a *'low'* wind, for example 6 m/s, which are usual.

The solution adopted in this wind turbine, common in several models of various manufacturers, consists of having a ***'gearbox'*** mechanism. In some models (not the one used for the simulator) there are two electrical generators, connected to the blade shaft through a multiplier with two outputs. In the case of the simulated wind turbine, the gearbox mechanism is based on having a generator whose stator winding is 'split', so that by changing the connection of these 'pieces' it is possible to have 2 pole pairs (*Large generator*) or 3 pole pairs (*Small generator*). These two cases correspond to synchronous speeds of 1500 rpms for 2 pairs, or 1000 rpms for 3 pairs.

*SynchronousSpeed = 50 Hz * 60 seconds / PolePairs*

There is another *'electrical'* reason, which has to do with the *'power factor'* characteristics of induction generators. In the [characteristics tables](../DSASTutorial/DatosTecnicosGenerador.md) you can check that for the same active power, the power factor is better the closer the active power is to the **nominal power**. In the case of the 2 pole pair connection the nominal power is 1300 kW, while at 3 pole pairs, it drops to 350 kW. If we look at the 3 pole pair connection power factor for a 250 kW active power we see it is 0.867, while generating these 250 kW with the 2 pole pair connection implies a 0.614 power factor.

The generator connection change *protocol* implements a hysteresis mechanism to avoid oscillations (frequent changes) when the wind value is close to the one at which it is decided to make these changes. See the following figure.

![](<lib/HisteresisVientos.png>)

Check these concepts with the practices [Being in production, wind modification to change the Generator connection from Small to Large](Cambiode1000a1500.md) and [Being in production, wind modification to change the Generator connection from Large to Small](Cambiode1500a1000.md).
