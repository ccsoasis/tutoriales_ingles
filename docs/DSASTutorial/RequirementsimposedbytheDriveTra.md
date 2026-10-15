---
tags:
- wind gusts
- turbulence
---

# Power Train requirements

The maximum extractable power from a given wind depends on the blade swept area. This means that said power is proportional to the square of the blade radius used.

The following figure shows the relationship of the maximum extractable power for a certain blade type, as a function of its radius. The abscissas are wind values (m/s) and the ordinates powers (watts).

![](<lib/CurvasPotenciaVsVientoConRadioComoParametro_1.jpg>)

*Fig.: Maximum obtainable power as a function of the Wind, for several blade radius values.*

The horizontal line at 2,000,000 watts indicates the power value we want to obtain: this value sets the characteristics of the electric generator we must use, and of all its associated Power Electronics. It therefore corresponds to an upper limit that must not be exceeded, and is known as **Nominal Power**.

In the figure we see that this nominal power is reached with different wind values, depending on the blade radius: the wind with which we reach the nominal power is known as **Nominal Wind**.

That is, to determine the blade radius we start from the desired nominal power, and from the wind we have at our location.

Another very important conclusion of the previous figure refers to the Power Train control. It can be seen that when the wind exceeds the Nominal Wind, the *obtainable* power is much greater than the nominal. However, the electric generator has been sized for the nominal power. This means that we must have a mechanism that allows reducing the power that is de facto extracted from the wind, so that it does not exceed the nominal power. This mechanism is the blade angle control (pitch).

In addition, the wind presents other characteristics, besides the 'stable' Weibull distribution, such as gusts and turbulences, which take into account *the wind speed rate of change*. The pitch control mechanism must be sized to withstand the maximum expected wind gusts at the wind turbine location, above all taking into account that the blades are quite heavy elements, and that the pitch changes occur while the blades rotate, so there are gyroscopic effects that must be additionally overcome.
