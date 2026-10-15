---
tags:
- busbars
- bypass contactor
- thyristors
- PCC
- point of common connection
- bypass
- soft connection
- nacelle
- synchronous speed
- large generator
- small generator
- soft starter
- squirrel cage
- medium voltage
---

# Electrical Grid connection

The Electrical Grid connection is where the electrical energy produced by the wind turbine is evacuated. In reality, this connection is made in two sections, one that connects the wind turbine to the electrical Substation of the Wind Farm where the wind turbine is, and another is the Substation connection to the Electrical Grid itself.

Both sections have specific operating voltages. The wind turbine connection to the Substation is usually done through a transformer, located at the wind turbine foot or inside it. Its secondary voltage is in the range called Medium Voltage (more than 1,000 V), typically between 15 kV and 22 kV. The primary is typically 690 V, which is the voltage of the electric generator used.

The electric generator used in the wind turbine on which this simulator is based is of the ones called "**squirrel cage**" or "*short-circuited rotor*" (see [details](Introductiontothephysicalprincip.md)). The generated electrical power comes out through the stator connection.

## Wind turbine generator connection to the transformer

The connection is made through the power cables that go down from the nacelle to the electrical cabinet located in the lower part of the Tower.

![](<lib/Lapp_Wind_Portfolio.jpg>)

## Generator operating regimes

In the model used in this simulator, which allows operating at two speeds, it is achieved using two connection ways of the stator windings. These are designed so that in one stator connection way 4 magnetic poles (2 pole pairs) are generated and with the other 6 poles (3 pole pairs) are generated. This means that the synchronous speed in one case will be 1500 rpms (for a 50 Hz grid) and in another case 1000 rpms.

***Synchronous_speed*** *= (50 Hz * 60 seconds / Pole_pairs)*

Since it is at 1500 rpms when the wind turbine greatest power is achieved, this connection is usually called "*Large Generator*", while the 1000 rpms connection is called "*Small Generator*".

In some old models the same functionality was achieved using two independent generators, connected to a gearbox that has two high "output" shafts, with a different ratio with the low shaft for each of them.

For the case of a 60 Hz grid, the speeds of a similar generator would be 1800 rpms and 1200 rpms, respectively.

## Electrical Panel details

The connection of the cables that go down from the electric generator to the cables that come out of the **Electrical Panel** and that connect the wind turbine to the <mark>Point of Common Connection</mark> of the Wind Farm (known as **PCC**), is done through the Panel busbars, the protection fuses and the wind turbine Main Contactor.

In the Panel *busbars* the phase voltage and phase current measuring instruments are placed: the current per phase measurement is done through <mark>*current measuring transformers*</mark>, inserted in the bars. The output of these *current measuring transformers* is standardized at 1 Amp. or 5 Amps full scale: therefore their primary/secondary ratio must be known (for example, 1000/5), which is a parameter that must be entered in the Controller to make the correct calculations. With these transformers, the measuring instruments of the electrical parameters...

![](<lib/Esquema electrico conexion generador.png>)

The power cable connection passes through a circuit made up of 3 groups of ***thyristors*** in counterphase that have a contactor in parallel, known as ***Bypass***. This component group, together with a control logic that generates the thyristor firing signals (which generates the signals that go to the thyristor gates), are used to achieve a ***soft connection***. This connection mechanism is known as [SoftStarter](Softstarter.md).
