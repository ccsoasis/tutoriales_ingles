---
tags:
- air density
- power curve
- power factor
- production
- reactive power
- cutin
- nominal wind
- production curve
---

# Wind turbine power curves

From the production point of view, a wind turbine is characterized by a "**production curve**" that gives the power it produces as a function of the incident wind.

This curve can have several shapes, depending on the technology used in the wind turbine. The first industrial wind turbines had a curve like the one shown in figure 1.

![](<lib/Curva potencia pala fija.png>) Fig 1.

In these wind turbines the *blade attack angle* (**pitch**) is *fixed*. It can be observed that the power generated when the wind increases from a certain wind value (about 16 m/s in the figure 1 example) is reduced instead of increasing. This behavior derives from the *blade aerodynamic response*, which avoids the Power Train *runaway* when the wind rises above a certain value: that is, this wind turbine type includes a runaway safety mechanism "per se".

Later the *variable blade angle* wind turbines were introduced, which differed from the previous ones in having mechanisms that allow regulating the Pitch angle: this capacity is used to control the power, and also to brake the Power Train. The 'Power vs Wind' curve of these wind turbines is shown in the following figure.

![](<lib/CurvaPotenciaPalaVariable.png>) Fig 2

Later the **variable pitch blade** and also **variable Power Train speed** wind turbines were developed. The difference with the previous ones is that the Power Train rotation speed varies as a function of the wind, in order to have the best use of it. This requires that the converter of the Power Train rotational kinetic energy to electrical energy (the Electrical Generator) be more sophisticated. In the previous models, and precisely due to the electrical converter type (typically an asynchronous generator with short-circuited rotor - or *squirrel cage*-), the Power Train is made to work at an almost fixed speed (with variations of the order of 4%), which implies a non-optimal aerodynamic use at low wind speeds.

There are intermediate designs that appeared before the variable speed wind turbines that use two electrical generators (or only one, but with the possibility of two different electrical connections effectively simulating two generators) that have two production operating speeds (two synchronous speeds), with which they present a certain degree of adaptation to low winds. They are known as "*two-speed*".

Taking into account these possible variations, in the following figure a typical curve of a wind turbine with pitch control and two speeds is shown, and the set of wind parameters used in the wind turbine control.

![](<lib/Curva de potencia con vientos.png>) Fig 3.

In this graph the expression "**cutin**" is shown that corresponds to the concept of *'beginning of the wind turbine grid connection process and passage to production*'. Similarly, there is the concept of "**cutout**" that corresponds to the concept of *'cessation of production and grid disconnection*'. The basic parameters are the **Nominal Wind** and the **Nominal Power**: this is the maximum power the wind turbine is capable of producing, which occurs when the wind is equal to or higher than the nominal.

It is important to keep in mind that *the shape* of this curve depends on the air density, which also influences the Nominal Wind value, not so in the Nominal Power, which is limited only by the electrical generator capacity.

In the following table the description of the wind values indicated in the previous graph is presented.

| **V min for orientation** | Below this wind level the Controller does not consider it worth orienting the Nacelle. |
|---|---|
| **V min for cutin** | Below this value, the Controller does not start the grid connection process. |
| **V min change from large to small** | In the case of the two-speed wind turbines, this value corresponds to the minimum value at which the "large" generator is used |
| **V max change from small to large** | In the case of the two-speed wind turbines, this value corresponds to the maximum value at which the "small" generator is used |
| **V max for cutin** | When the wind turbine is stopped and the wind regime is very high, the Controller will not start the cutin process if this wind is higher than this value. |
| **V max continuous production** | This wind value is the maximum at which the Controller keeps the production continuously. |
| **V max with time limit** | When the wind exceeds, during a short time period, the 'V max continuous production' value, the Controller will keep the production. However, if this value is exceeded during a preset period the Controller will start the production exit and grid disconnection process (cutout) |
| **V absolute max** | If the wind reaches this value the Controller will start the cutout process immediately. |
