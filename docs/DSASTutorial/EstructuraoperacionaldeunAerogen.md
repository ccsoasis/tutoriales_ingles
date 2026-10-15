---
tags:
- pitch
- wind vane
- emergency
- manual brake
---

# Functional scheme of a squirrel-cage wind turbine

## Functional block scheme of a wind turbine with squirrel-cage generator, and with variable blade angle.

![](<lib/Aerog active stall.png>)

In the previous figure, the two most important functions of the Controller of this type of wind turbine are shown: that is, other monitoring and control functions, common to other wind turbine families, such as those related to the nacelle orientation, the temperature monitoring in the different subsystems, etc., are not reflected.

The main functions of the Controller of this wind turbine family correspond to:

- the control of the electric generator **grid connection (and disconnection)**, and

- the **blade angle control:** with it the **power obtained from the wind** is modified (when in *production*) and the **Power Train brake**, when in the *stop* phase.

## Detailed functional scheme

![](<lib/Esquema DSAS.png>)

This figure shows the functional scheme of this type of wind turbine.

Main functions

- <mark>Control of the</mark> <mark>**electric generator connection and disconnection**</mark> <mark>to the Electrical Grid</mark>:

The Controller monitors:

- ○The wind (through the anemometer).

- ○The generator shaft revolutions.

- ○The grid parameters (voltages and currents per phase).

and carries out the control through:

- ○The thyristors.

- ○The Bypass contactors.

- <mark>Control of the</mark> <mark>**power obtained from the wind**</mark>:

The Controller monitors:

- ○The wind (through the anemometer).

and carries out the control of the power obtained from the wind through:

- ○The blade angle (pitch) control mechanism.

- <mark>Control of the</mark> <mark>**two-speed generator connections**</mark>

When the generator has two available ways of connecting its stator (which implies that it can operate at two synchronous speeds), the Controller carries out the change maneuvers between these two speeds automatically. The algorithm used is the following:

- ○If it is in production at the high generator speed:

- It starts the grid disconnection process, modifying the blade angle so that the power obtained from the wind is reduced.

- When the produced electrical power is 0, it disconnects the generator from the grid, opening the Bypass contactors.

- It maintains the blade angle, so that the Power Train keeps losing rotation speed, until it reaches a value slightly below the low synchronous speed.

- It changes the generator winding connection so that it corresponds to the low synchronous speed.

## Auxiliary functions

- <mark>Control of the</mark> <mark>**operation safety**</mark>:

The Controller has wind turbine state supervision algorithms, whose mission is to guarantee the safety of people, and of the equipment itself.

For this it monitors:

- ○The wind speed.

- ○The generator shaft speed range.

- ○The blade rotation speed.

- ○The tower vibration sensor state.

- ○Temperature sensors of several elements: generator stator winding, Power Train shaft bearings, gearbox, environment.

and carries out the grid disconnection operation (if connected), and places the blade angle "*feathered*" (which means with minimum resistance to the incident wind).

- <mark>Control of the</mark> <mark>**nacelle orientation**</mark>.

The Controller uses the **wind vane** signal to know the value of its misorientation with respect to the wind direction.

It uses the motor groups (one for each rotation direction: CW (clockwise) or CCW (counterclockwise)), to correct the possible misorientation.

- <mark>Monitoring and control of the</mark> <mark>**disc brake**</mark>.

The disc brake is used, fundamentally, to prevent the Power Train rotation, when maintenance operations on the blades, etc. must be done. It works like the *hand brake* concept in a car.

The brake mechanism elements (shoe, disc, hydraulic cylinder, valve) are sized for another more demanding function: acting as a Power Train brake in *emergency situations*. When the Controller decides to stop the Power Train it uses the blade angle, specifying a 90º angle. If this procedure does not respond adequately (not fast enough), it uses the disc brake as a last resort. This use is considered a *fault*, since, if the moment of its application is at production rotation speed, all the energy obtained from the wind has to be dissipated in the shoe, producing its deformation.

- <mark>Monitoring of the</mark> <mark>**Tower vibrations**</mark>

The Controller reacts to the activity of the *vibration sensor* located in the Tower, stopping the Power Train, and placing the blade "feathered".

- <mark>Maintenance of the</mark> <mark>**hydraulic system**</mark>.

The hydraulic system is used by the Power Train brake mechanism, but in addition, depending on models, it can be used to fix the nacelle rotation, through shoes placed at its base. In certain models, it has also been used to supply pressure to the blade angle change mechanism.

The Controller receives the signal from a *pressure switch* that allows it to know the pressure level in the hydraulic circuit. Depending on the operations to be carried out, it starts and stops the *hydraulic pump* to maintain said value in an adequate range, or acts on the *discharge valve*, to reduce said pressure.
