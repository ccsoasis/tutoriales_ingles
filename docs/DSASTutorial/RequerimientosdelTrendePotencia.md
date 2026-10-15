---
tags:
- Weibull
- hours per year
- nominal wind
---

# About the wind

## Wind definition

The wind regime of a place is described as a statistical function called "**Weibull**". The following figure shows on the ordinate axis the time percentage (in *hours per year*) in which the wind is in the range indicated on the abscissas.

![](<lib/Distribucion Weibull castellano.png>)

At the location corresponding to the distribution of the previous figure, the most probable wind speed is between 4 and 6 m/s.

The **Weibull** distribution has two characteristic parameters: the "*average wind*" and the "*maximum expected wind*".

However, since our interest is the power we can extract from the wind, it is more interesting to consider the distribution of the power associated with the wind, for which we must apply the formula described in [Concepts about the extractable wind power](Porqugiranlaspalas.md).

**WindPower = K \* AirDensity \* BladeSweptArea \* Wind**<sup>**3**</sup>

Where *K* is a constant. If we apply this formula to the previous graph, to obtain the power distribution as a function of the wind, we obtain the following figure. The abscissas still refer to the wind speed (m/s) and the ordinates to the power.

![](<lib/Distribucion Potencia Viento.png>)

We can see that, in this particular case, despite the fact that the wind speed that has more hours per year is between 4 and 6 m/s, there is a <u>*higher production speed*</u>, around 10 m/s, so this value becomes the "**Nominal Wind**" ("Nominal Wind" in English).

The second condition defines the characteristics of the electric generator to be used in the wind turbine, and all the associated Power Electronics (if any). This value is the "Nominal Power" ("Nominal Power" in English).

The blade length must be such that at the nominal wind speed we have the Nominal Power. This condition has an important consequence: for winds above the nominal wind, the power that can be extracted from the wind is greater than the electric generator nominal power. This very important aspect is presented in the following paragraph: [Power Train requirements](RequirementsimposedbytheDriveTra.md).
