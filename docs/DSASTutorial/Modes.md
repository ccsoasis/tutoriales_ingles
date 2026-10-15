---
tags:
- cable turns
- yawing operation
---

# Modes

The Controller allows *two operating modes* in relation to the **nacelle yawing** functionalities:

a) Manual.

b) Automatic.

In "Manual" mode, the operator can use the "Control Terminal" buttons associated with "Manual turn". See the following figure.

![](<lib/ControlTerminal-espanol-en-produccion.jpg>)

Fig 1

In production these two buttons are "*not active*", as shown in Fig 1, above.

For them to become "*active*" it is necessary to disconnect the wind turbine from the grid, "STOP" Button.

![](<lib/ControlTerminal-espanol-parado.jpg>)

Fig 2

In "Manual" yawing mode, the Controller prevents the turn buttons from being active if there is any problem with the electrical system.

Even in Manual mode, the Controller keeps monitoring the power cable turns number value, and does not allow the maximum to be exceeded, in either of the two directions.

In "Automatic" mode the Controller makes decisions about cable unwinding, with several criteria.

In Automatic mode the behavior of the yawing system takes into consideration the state of the WindTurbine. The main target is to keep the WindTurbine in production as long as possible and also to reduce the consumption of power (the yawing motors consume power that is borrowed from the produced power - if in production - or taken from the Grid if the generator is disconnected).

If the wind speed is below a limit ("*Minimum for yawing*"), then it is not wise to spend energy putting the WindTurbine facing the wind. A typical value for this limit is 2.3 m/s. Above this limit, the criteria is: it makes sense first orient the Nacelle as, most probably, the wind will grow enough for trying a cutin process in short time.

If the decision is for "orienting" the Nacelle then the next criteria relates to the cables' turns. If at the beginning of the orienting process these turns are bigger than a certain limit (another parameter), then, before starting orientation, makes sense untwist the cables, foreseeing that perhaps the wind will change its direction in the sense of reaching that limit. Once untwisted the orientation process continues. A typical value for this limit is related to the maximum number of turns the cables support. If this number is, say, 3.5 turns, then a good limit for untwist before orienting, and before trying to cutin, is around half, say, 2 or 2.5 turns.

Of course the Controller, in Automatic mode, monitors continuously the maximum limit of turns for the cables but does not act unless the limit switch is activated. If that happens the WindTurbine will stop immediately, registering an "incidence" that generates a STOP Sequence of level 5. This level of STOP is the softest, meaning that the Controller will change the Pitch to get a negative value of power (therefore the DriveTrain will start slowing down), till the Generator speed will reach the synchronous value, moment at which the Bypass contactor will be opened with minimum stress (i.e., zero or minimum current passing through it, minimizing the arcs inside it), and the DriveTrain will continue slowing down, till its speed reaches an idle value. At that moment, if wind speed is valid for cutin, the automatic untwisting of the cables will take place as explained above.

![](<lib/Nuevo tem 11.png>)

![](<lib/Nuevo tem10.png>)

![](<lib/Nuevo tem 9.png>)

![](<lib/Nuevo tem 8.png>)

![](<lib/Nuevo tem 1.png>)

![](<lib/Nuevo tem.png>)
