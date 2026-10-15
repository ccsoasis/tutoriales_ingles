---
tags:
- wind turbine
- WT
- kinetic energy
- HAWT
- horizontal axis wind turbine
- DFIG
- doubly fed induction generator
- basic wind turbine simulator
- plant
- nacelle
- upwind
- downwind
- gearbox
- synchronous speed
- rotor resistance
- power train
- permanent magnets
- asynchronous
- synchronous
- DC link
- full converter
- back-to-back
---

# Basic concepts of wind turbines

This document assumes that the reader is familiar with the basic terminology, functionalities and capacity of a wind turbine. We recommend reading the "Basic Wind Turbine Simulator" tutorial.

In any case, here is a brief presentation of these concepts, as a reminder.

An **industrial** **wind turbine** is an **electric power production plant**, with a capacity starting at 100 kW. Currently there are commercial models in the 6 MW range.

At a high level, a wind turbine can be described as two power converters working together: one that transforms the kinetic wind energy that strikes it into rotational energy, and another that transforms this rotational energy into electrical energy.

Wind turbines can be classified according to these two converters. The most common in industrial use is the so-called **HAWT** (Horizontal Axis Wind Turbine), in which the wind strikes perpendicularly on the plane of rotation of the blades, which are attached to a "power train". This "power train" rotates horizontally and is located on an elevated platform, known as the "**nacelle**".

The plane of rotation of the blades must be kept perpendicular to the wind, and for this there are two methods depending on whether the blades should be the first thing the incoming wind touches (*upwind*) or the last (*downwind*). The theoretical advantage of the downwind method is that the wind itself is responsible for orienting the nacelle (the same principle as common wind vanes); however, it has the drawback that the wind has to flow through the nacelle and the tower before it reaches the blades, resulting in an associated energy loss. Therefore, the great majority of HAWT wind turbines are oriented facing the wind. This implies that they must have a mechanism to keep them well oriented "facing" the wind.

They generally have three blades, although there are industrial models with two blades.

As for the electrical converters, they all use some type of electric generator and, in some cases, power electronics equipment.

The most common types of electric generators are:

- Asynchronous induction generator.

- Permanent-magnet induction generator.

When asynchronous induction generators are used, it is necessary to use a **gearbox** since the **power train**, i.e. the mechanical subsystem connected to the blades, normally rotates at speeds in the order of 15 to 40 rpms, while asynchronous induction generators operate in the range between 1000 and 2000 rpms.

In cases where permanent-magnet induction generators are used, there are some designs that allow working directly at the rotation speed of the power train, and therefore they do not need a gearbox.

Another important aspect refers to how the electric generator is connected to the grid. In the simplest form, this connection is direct, i.e. the generator stator is directly connected to the grid. This solution forces the power train (including the blades) to rotate at a practically fixed speed, since induction generators have a very narrow operating range, typically less than 1%, in the area immediately above their "synchronous speed". This solution is common in the first generations of wind turbines, up to powers in the order of 700 kW to 800 kW.

Forcing the power train to work at a fixed speed is not the most efficient procedure from the point of view of "exploiting" the wind energy, when it varies over a wide margin: each wind speed requires a specific speed for optimal transfer: see [Reasons for the use of Variable Speed Wind Turbines](PorqueAerogenVeloVariable.md). To resolve the mismatch between the requirements of the induction generator and the wind mechanism, several solutions have been adopted: the first was to divide into two the wind range where operation is desired, and use two electric generators, one for each range. A variant of this solution is to use a single generator but changing the way its windings are connected, so that its magnetic poles can be changed, typically between 6 and 4 poles, and therefore its synchronous speed.

A second solution was to use the torque-speed characteristic of induction generators, which is very sensitive to changes in the rotor winding resistance. The great advantage of this approach is that the power electronics needed to change the rotor resistance must handle a power that is a very small fraction of the Nominal Power of the whole. In the case of the controller called "Rotor Resistance", by controlling the external resistance seen by the rotor it is possible to increase the dynamic margin of the generator at nominal power up to 10% above its synchronous speed.

A third solution that can be found in some wind turbines, although very minority, consists of not connecting the induction generator directly to the grid, but rather feeding a Power Electronic Converter through a controlled rectifier: this converter is the one actually connected to the grid. In this solution the generator supplies power to a DC circuit (**DC Link**), which in turn feeds the Power Electronic Converter: this modality is usually referred to in the sector as "**full Converter solution**", to emphasize that the Electronic Converter must withstand all the power transferred in the wind turbine, which is why this Converter is an important part of the construction cost and also of the maintenance cost of the wind turbine.

A fourth solution uses the ideas of the two latter solutions, and is known as DFIG (from Doubly Fed Induction Generator), or doubly-fed generator. This solution uses a wound-rotor induction generator which is connected to a structure of electronic power converters known as "**Back-to-Back**". This solution allows extending the generator's operating speed range between 15% below and 15% above the synchronous speed. Apart from this extended operating range, this solution has the advantage that the electronic power converters only have to "withstand" a percentage (between 25% and 30%) of the total power of the wind turbine.
