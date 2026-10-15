---
tags:
- nominal wind
- Weibull
- BladesSweptArea
- nominal power
- aerodynamic coefficient
- Cp
- pitch
- wind gusts
- low wind regimes
- maximum expected wind
- air density
- blade swept area
- average wind
---

# Relationship between wind turbines and their location

The basic parameters in the design of a wind turbine are:

1. The maximum power it will deliver to the grid.

2. The wind regime of the site where it will be erected.

The wind regime of a place is described as a statistical function called Weibull. The following figure shows on the ordinate axis the percentage of time (in hours per year) in which the wind is in the range indicated on the abscissa.

![](<lib/Distribucion Weibull castellano.png>)

At the site corresponding to the distribution in the previous figure, the most probable wind speed is between 4 and 5 m/s.

The Weibull distribution has two characteristic parameters: the *average wind* and the *maximum expected wind*. However, from the point of view of electrical production, it is important to take into account that the power generated at a given moment is proportional to the cube of the wind speed at that moment. That is, the formula is:

**WindPower = K \* AirDensity \* BladeSweptArea \* Wind**<sup>**3**</sup>

If we apply the previous formula to the site's wind distribution, we obtain a distribution function of the power obtainable from this site, as shown in the following figure.

![](<lib/Distribucion Potencia Viento.png>)

It is clear that there is a "*favorite*" production speed, around 10 m/s, so this seems to be a good value for the design of a wind turbine for this site. This becomes the "**Nominal Wind**".

The second condition defines the characteristics of the electric generator to be used in the wind turbine, and all the associated Power Electronics circuitry, if any. This value is the "**Nominal Power**".

The length of the blades must be such that at the nominal wind speed we obtain the Nominal Power. This condition has an important consequence: for winds above the nominal wind, the power that can be extracted from the wind is greater than the nominal power of the electric generator.

**Description of the operation of the power train of a wind turbine**

The formula to calculate the power we extract from a wind flow V, mentioned above, can be detailed in the following more explicit form:

**ExtractedWindPower** = 0.5 \* ***AirDensity*** \* ***BladeSweptArea*** \* ***Wind***<sup>3</sup>   \*  ***Cp***(*Wind*, *BladeRotationSpeed*, *BladeAttackAngle*)

From it we see that the ExtractedWindPower is directly proportional to:

- The *air density*.

- The *blade swept area*, i.e. proportional to the square of the blade length. That is, by increasing the blade length by 40% (1.4) the power extracted from the wind will be double (1.4 x 1.4 = approx. 2).

- The cube of the wind. That is, if the wind goes from 5 m/s to 10 m/s the power that we *can extract* from the wind is multiplied by 8. The power that we actually extract depends on another factor, Cp, which also depends on the wind speed.

The fourth component, Cp, known as the **aerodynamic coefficient**, is a complex function that depends on:

a) the wind speed,

b) the speed at which the blades rotate,

c) the angle of attack of the blades on the wind (**Pitch** in English)

A detailed presentation of this function is made in [Description of the Cp function (aerodynamic coefficient)](DescripcindelafuncinCpcoeficient.md).

The maximum value of the Cp function is around 0.49 and depends on the blade design. Using this value we can make a graph like the one shown in the following figure, which gives us the *maximum extractable* power from the wind as a function of the blade length.

![](<lib/CurvasPotenciaVsVientoConRadioComoParametro_1.jpg>)

In the figure, a horizontal line corresponding to a given nominal power (*Target*, in this case 2,000,000 W) has also been drawn.

From this graph the following conclusions can be drawn:

1. The **great influence of wind speeds above the nominal one**.  
That is, if we maintain the conditions (blade rotation speed and attack angle) in such a way that Cp is always the maximum, then a wind 10% above the nominal offers a power of more than 33% over the nominal power. If the wind rises by 50% (up to 15 m/s in the figure) the obtainable power is 337% of the nominal. For example, taking the case of a blade radius of 48 m with a nominal power of 2 MW at 10 m/s, a wind increase to 12 m/s implies that the available power would become almost double (3.8 MW). As a conclusion, it is seen that it is necessary to control the value of Cp for each wind value, so that, for winds above the nominal, the power *actually extracted* from the wind corresponds to the nominal and not the obtainable one. See the following graph.

![](<lib/CurvasPotenciaVsVientoConRadioComoParametro_1.jpg>)

2. Behavior against **wind gusts** (**wind gusts** in English)  
If a gust occurs (understood as a rapid rise in wind (see [Wind gusts (Wind gusts)](RfagasdevientoWindgusts.md)) but the wind never exceeds the Nominal Wind, the power extractable from the wind will not exceed the nominal and, therefore, there will be no danger for the electric generator.  
However, if at some moment the wind exceeds the nominal and grows rapidly, the wind turbine must have a *fast mechanism that allows controlling the Cp* at all times, so that the power actually extracted from the wind does not exceed the nominal, except during predetermined periods of time. This concept is key to understanding how a DFIG wind turbine works. That is, the fastest expected gust conditions the change capacity of the Cp mechanism (basically the angle of attack of the blades).

3. Adaptation of the wind turbine for **low wind regimes**.  
If the wind turbine's location has a low wind regime, the wind turbine must be adapted for it. For this, the only option is to increase the blade radius. In the previous graph it can be seen that to maintain the same nominal power and reduce the nominal wind from 10 m/s (blue curve) to 9 m/s (green curve) we have to increase the blade radius from 48 m to 55 m. That is, to reduce the nominal wind by 10% we have to increase the radius by 14.6%. If we wanted to reduce it to 8 m/s, the radius must increase to 68 m: that is, reducing the nominal wind by 20% implies increasing the radius by 41.7%. This has an important impact not only on the price of the wind turbine but also on the installation and transport conditions.
