---
tags:
- controlled rectifier
---

# Basic structure of the Back-to-Back Converters

To understand the structure of the Back-to-Back (B2B) converters it is important to be aware of their purpose:

- They must have an important power capacity: the converter connected to the grid (GSC) must be able to supply between 25% and 30% of the wind turbine Nominal Power. That is, approximately 600 kW for a 2 MW wind turbine. That is also the power that "comes out" through the rotor when it is in supersynchronous operation and therefore, the capacity of the RSC as a controlled rectifier.

- The two converters (GSC and RSC) must also be able to act as controlled rectifiers. The RSC must also have control mechanisms that allow "presenting" a certain type of load to the Generator rotor, controllable in frequency, as well as in voltage, current and phase, for each rotor winding.

- The DC Link must be able to store enough energy to support all possible operations, both subsynchronous and supersynchronous.

A general scheme of these converters is shown in the following figure.

![](<lib/B2B esquema en colores.jpg>)

The green part (left) corresponds to the RSC, the right part to the GSC and the central part corresponds to the DC Link.

It can be seen that the outputs (both of the RSC and of the GSC) have inductors: these are the elements that allow *controlling* the currents that at each moment flow from/towards the outside of both converters. In [Operating principles](ConvertidoresBackToBackPrincipio.md) some basic electronic circuits on which these converters are based are presented.

Conceptually we can summarize the behavior of this set of converters with the following ideas:

- Each of them is capable of operating as an "alternating current generator" and also as a "*controlled rectifier*".

- When one of them generates AC the other rectifies.

- All the power transfer is done through a store, which is a capacitor, called DC Link.

That is, these circuits transfer electrical energy from an AC source to a DC one and vice versa. The way of making this transfer is by using electronic components that operate only in digital mode: that is, the only way of control is by deciding when they are conducting and when open. When they are conducting they behave as "short circuits" (or very close) and therefore the circuit needs a component that limits the current: that component is an inductor. See a more detailed description in [Operating principles](ConvertidoresBackToBackPrincipio.md).

![](<lib/Esquema basico del B2B.jpg>)
