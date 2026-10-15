---
tags:
- subsynchronous
- synchronous speed
---

# Operating modes

The B2B operating mode is determined by the Generator needs, which depends on the conditions imposed by the Power Train.

When the Generator is operating below its synchronous speed (subsynchronous) it requires its rotor winding to receive power with certain frequency, voltage and current values per phase, both in magnitude and phase. To see details you can go to the [Practical classes](../DFIGExercises/Clasesprcticas.md). In everything that follows, the phase reference is the phase 1 voltage.

In the previous situation the RSC works as a three-phase generator that receives power from the DC Link and injects it into the rotor.

When it is at a speed higher than the synchronous one, part of the generated electrical power "comes out" through the rotor winding. For this to happen, the RSC must behave as a certain impedance (which depends on the instantaneous power and the instantaneous rpms). In this situation, the RSC also becomes a controlled three-phase rectifier that converts the (AC) power that comes out of the rotor into DC in the DC Link.

The voltage in the DC Link (the capacitor located in the middle) is variable and its value depends on the instantaneous rpms and on the powers the generator is delivering. Its maximum value is usually in the range of 1,500 to 2,500 V DC.

The connection of the GSC with the grid is sometimes done through a transformer that reduces the maximum operating voltage requirements on its electronic components.
