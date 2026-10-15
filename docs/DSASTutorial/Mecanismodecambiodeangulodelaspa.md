---
tags:
- feathered
- aerodynamic coefficient
- maintenance
- aerodynamic brake
- fault
---

# Power Train Brake System

The Power Train, which includes the blades, has a brake mechanism that is NOT used (normally) to reduce the blade rotation speed, but as a position fixing mechanism, once it is stopped (or rotating at very low speed). To reduce the blade rotation speed, the value of its pitch angle is used: from a certain value, the *blades push the air*, *transferring kinetic energy from the Power Train to the air*.

The following figure shows a typical example, located on the *high shaft* (the generator shaft).

![](<lib/Freno-disco.jpg>)

## Brake concepts in a wind turbine

The *Power Train* of a wind turbine can be in the following situations:

- **In Production**  
In this state, the blade angle makes an energy be collected from the wind in the form of mechanical torque that moves the electric generator shaft, which transforms it into electrical energy.

- **Inactive** (*Idle* in English)  
In this state, the blade angle is in a position such that it does not collect any energy from the wind, so that the Power Train does not rotate. This angle is 90 degrees and this position is called "*feathered*".  
In this position the blade [Aerodynamic coefficient](Conceptossobrelapotencia.md) is *negative*: that is, any rotation that the Power Train may give is braked by the blades. In other words, any rotational energy that the Power Train has is used to "move the air", and therefore, it is energy that is transferred to the air and therefore decreases.  
In this state the Power Train can rotate, although for a short time.

- **Braking**  
This state is used to carry out work inside the wind turbine, and to guarantee the safety of people. This state is guaranteed by a **disc brake system**: see [Some industrial examples](SistemadeFrenos.md).

## Brake system functions

The brake system in a wind turbine has the following functions:

- **Prevent the Power Train from moving while it is in the "parking" position**, typically during maintenance operations.

- **Prevent the Power Train overspeed**.  
The Controller continuously monitors the Power Train rotation speed, and starts a safety protocol so that it does not exceed a maximum value.  
For this it uses two devices:

- ○The blades, setting an angle such that the wind mechanical torque is negative, that is, that it brakes the Power Train, which corresponds to an *aerodynamic brake*.

- ○If the aerodynamic brake is not capable of reducing the Power Train rotation speed in a certain time, then the Controller will use the disc brake system.

Stopping the Power Train implies the dissipation of the kinetic energy stored in it. Therefore, if the disc brake system is used, it can result in an important deformation of the disc, or of the brake pads, which constitutes an **important fault** of the wind turbine.

The brake disc can be located on the gearbox high shaft (that is, on the Generator shaft) or on the low shaft (that is, on the rotor shaft, which is directly connected to the blade Hub). The most common position is on the high shaft, since, although there is usually more space on the low one, that position requires a greater friction torque.
