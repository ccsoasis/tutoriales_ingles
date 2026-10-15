---
tags:
- nominal power
- electric generator
- stator
- squirrel cage
- short-circuited rotor
- induction machine
---

# Electric generator: Physical Description

To convert mechanical energy into electrical energy, no device possessing such a physical property is used directly. Instead, an ingenious arrangement based on electromagnetic phenomena is employed. To understand this, it is first useful to examine how magnets can be used in a purely mechanical system, such as the one shown in this video.

The idea is to use two magnets to transfer the mechanical power applied to one shaft to another shaft. This may appear to be a rather trivial application, except when considering that the magnets mounted on each shaft mechanically decouple them, which can be highly advantageous in certain situations.

This example is intended to convey a simple but very important concept: magnetic interaction can be used to transfer mechanical power without direct mechanical contact. However, *this transmission mechanism has a limit*. When the angular displacement between the magnets exceeds 90°, as a result of excessive input torque applied to the driving shaft (the shaft on the right), the magnetic coupling is no longer able to transmit the required power effectively.
Based on these principles, we can build the device shown [in this video](https://youtu.be/3nvRhIbjhbo){:target="_blank"}. Its purpose is to exemplify how to use two  magnetically coupled devices (the two shafts) in such a way that mechanical torque (ie, mechanical energy) applied to one of them can be transmitted to the other. It also shows the artifact's limitations: the angular difference between the two magnetic fluxes cannot exceed 90°; if it does, the artifact changes its characteristics.

Although this arrangement only transfers mechanical power from one shaft to another, it introduces the key concepts needed to understand an electrical generator. 

To understant **how mechanical energy can be transformed in electrical energy** it is necessary to understand the following electromagnetic principles:

1. *A moving electric charge generates a magnetic field* and therefore behaves as a physical magnet. Consequently, permanent magnets and current-carrying coils can be used interchangeably to produce magnetic flux.

2. If a *closed electrically conducting loop* is placed in a region where magnetic flux is present, *a current is induced on it whenever the magnetic flux linking the loop* **changes**. This change in magnetic flux can be produced in several ways: by moving a magnet relative to the loop, by moving the loop relative to a stationary magnet, by replacing the magnet with a coil supplied with alternating current, or by moving a current-carrying coil around the loop.

3. The electrical power carried by the induced current in the is equal to the **mechanical power** required to produce the change in magnetic flux through the loop. Therefore, a generator does not create energy; it simply converts the mechanical power supplied to its shaft into electrical power through electromagnetic interaction.

The operation of an electrical generator is fundamentally based on combining these three principles in a practical and efficient manner.

In the wind turbines contemplated in this Simulator, the generator is a *short-circuited rotor (or squirrel cage) induction machine*, and all the electrical power sent to the grid is obtained through the generator *stator*.

There are various videos in the Internet that give constructive details of this type of generator, like, for example, <iframe width="315" height="576" src="https://www.youtube.com/embed/p7wIT3YEeXc" title="Squirrel Cage Induction Motor Working Principle | 3D Animation" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>, 

or 
<iframe width="315" height="576" src="https://www.youtube.com/embed/08mn52N8YaQ" title="How Squirrel-Cage Motors Really Work?" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

In [Introduction to induction machines](IntoductiontotheInductionMachine.md), presents the operating principles of these machines.

The appendix [Characteristics of the Generator emulated in this Simulator](DatosTecnicosGenerador.md) presents the characteristics of a real model, which this simulator uses.

This type of generator is also used in other installations, such as cogeneration plants. Its main drawback is that the connection to the electrical grid must be carried out in such a way that it neither harms the installation nor disturbs the grid. This is usually achieved by means of a device called [Soft connection (soft connection) to the grid](Softstarter.md).
