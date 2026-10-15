---
tags:
- anemometer
- brake disc
- coupling
- hub
- rotor bearing
- wind turbine
- yawing operation
- blades
- power train
- rotor
- pitch angle
- pitch
- downwind
- upwind
- gearbox
- nacelle
- HAWT
- power electronics
---

# What is a wind turbine?

A wind turbine is an **electrical production plant** capable of transforming the *wind kinetic energy* into *electrical energy*.

It can be described as *two power converters working together*: the first transforms the <u>*linear*</u> kinetic energy of the wind into <u>*rotational*</u> kinetic energy, and another that transforms this rotational energy into electrical energy.

![](<lib/conversion_energia_aerogenerador.svg>)

The first converter is called "***Power Train***" (***DriveTrain*** in English), and is made up of Blades, mounted on a device (***hub***) that only leaves them one degree of freedom (rotation). In this way, the wind energy is transformed into rotational energy of this Power Train.

The second converter consists of an electric generator whose rotor is connected to the Power Train. In most cases this connection is done through a gearbox, because the *optimal working conditions* of the two converters, basically their shaft revolutions, do not coincide.

The electric generator can be of several types. The most common are:

- asynchronous with short-circuited rotor (known as squirrel cage)

- asynchronous with access to the rotor winding,

- synchronous,

- synchronous with permanent magnets.

Depending on the electric generator type, the wind turbines have additional **Power Electronics** equipment for their operation. In the case of the wind turbine with squirrel-cage generator, the object of the simulator associated with this tutorial, there is none.

The electric generator makes the electrical power sent to the grid appear as *mechanical resistance* on its shaft, which opposes the Power Train rotation.

In the case of the wind turbine type corresponding to this simulator, the generator is of the "*squirrel cage*" type, with the *stator* winding directly connected to the grid.

There are several wind turbine types, depending on the position of the axis around which the blades rotate: vertical and horizontal. The ones installed in Wind Farms are, practically all, of horizontal axis. In English they are known by the acronym HAWT (**H**orizontal **A**xis **W**ind **T**urbine). This type of wind turbines has a yaw mechanism through which they keep the blade rotation plane in perpendicular position.

In the following figure a first-generation HAWT wind turbine type is shown: its blades cannot rotate on their longitudinal axis, and are called "*fixed-pitch*".

![](<lib/AeroGenerador pala fija Bonus 600 reducida.jpg>)

Fig 1.

In the following figure an evolution of this design is shown, which has mechanisms in each blade that allow changing its angle with respect to the rotation plane: ***blade angle (pitch).***

![](<lib/Aerogenerador Siemens Pala Variable - textos.png>)

Fig 2.

## Wind turbine types

The wind turbines can be classified according to these two converters. The most common, in industrial use, is the so-called **HAWT** (from *Horizontal Axis Wind Turbine*):

- the blades rotate in a practically vertical plane, on an axis that is kept (almost) horizontal

- the wind strikes perpendicularly on the blade rotation plane. The axis is known as "Power Train", rotates horizontally and is located on an elevated platform, known as "*nacelle*".

The blade rotation plane must be proactively kept in a position perpendicular to the wind, but it can be at the wind turbine "front", or at the rear part. This plane can be the front of the nacelle (the blades are the first thing the incident wind touches) (***upwind*** in English) or the rear one (***downwind*** in English).

The theoretical advantage of the *downwind* method is that the wind itself is in charge of orienting the nacelle; however it has the drawback that the wind slows down when having to cross the nacelle and the tower before reaching the blades. Therefore, the great majority of HAWT wind turbines are oriented facing the wind (*upwind*). This implies that they must have a mechanism to keep them well oriented "facing" the wind.

They generally have **three blades** although there are industrial models with *two blades*.

As for the electrical converters, they all use some type of electric generator and, in some cases, Power Electronics equipment.

The most common electric generator types are:

- *Asynchronous induction generator*.

- *Permanent-magnet induction generator*.

When asynchronous induction generators are used, it is necessary to use a ***gearbox***, since the Power Train normally rotates with speeds in the order of 10 to 40 rpms, while asynchronous induction generators operate in the range between 1000 and 2000 rpms.

In the cases where permanent-magnet induction generators are used, there are some designs that allow working directly at the power train rotation speed, and therefore do not need a gearbox.
