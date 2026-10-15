---
tags:
- maximum power point tracking
- MPPT
- pitch
- Cp
- per unit
---

# Implications for the Power Train

**Implications for the Power Train**

The Power Train is the converter of wind kinetic energy into rotational energy. This Power Train has mechanisms (basically the angle of attack of the blades on the wind), with which it is possible to control the power effectively extracted from the wind. As described in [Relationship between wind turbines and their location](Relacionentrelosaerogeneradoresy.md) we can distinguish two situations:

- **When the wind is below the nominal**, then it is of interest to obtain the greatest power from the existing wind, i.e. that the aerodynamic coefficient **(Cp) is maximum**, regardless of the existing wind. This criterion is implemented with an algorithm known as [Maximum Power Point Tracking](AlgoritmodeSeguimientodelPuntode.md) ([Maximum Power Point Tracking -MPPT-](AlgoritmodeSeguimientodelPuntode.md)).

- **When the wind is above the nominal**, the value of Cp must be reduced so that the power extracted from the wind is exactly the nominal, so that the electric generator and its power circuitry are always working in design conditions.

The variables available to control Cp are two:

a) the rotation speed of the blades (of the Power Train), and

b) the angle of attack of the blades on the wind.

The solution adopted in the industry for wind turbines is based on the graphs in the following figure.

![](<lib/Curva MPPT con indicador de punto teorico max.jpg>)

Figure 1

In this diagram the abscissa axis represents the angular speed of the Power Train (in revolutions per minute -rpms-), and the ordinate axis represents the mechanical power. The units of measure are shown "normalized" in 'pu's (*per unit*). This representation method replaces the real value by the value relative to a reference one. The reference power chosen is the "nominal" of the wind turbine (in this case 2,000,000 W) and the reference speed is the one corresponding to the synchronous speed of the electric generator used, taking into account the gearbox effect: in this case 15.46 rpms.

We can distinguish three kinds of curves in this diagram:

- Each <mark>green curve</mark> corresponds to the maximum power obtainable from the wind for the indicated wind, as a function of the Power Train rpms. <u>Note</u>: it is important to keep in mind that each of the points on these curves corresponds to a certain value of the attack angle, which is not shown, and which is not necessarily constant.

- The <mark>blue curve</mark> corresponds to the locus of the points that, for each rpms value, gives the maximum wind power. That is, this curve corresponds to the definition of the Maximum Power Point Tracking (MPPT) algorithm.

- The <mark>red curve</mark> corresponds to the curve actually used for the Power Train control of a variable-speed wind turbine (such as the DFIG type).

Documentation about this methodology can be found in several publications: for example in publications of the [National Renewable Energy Laboratory (NREL)](Listadereferencias.md).

A brief explanation of this operating curve is the following:

1. Whenever the wind is below the nominal, the MPPT algorithm must be used. The curve shown, corresponding to this algorithm, derives from the study of the Cp function, whose conclusion is the following: there is a curve, which has the shape of a parabola (i.e. it is proportional to the square of the Power Train rotation speed), which gives for each rotation speed value the maximum power obtainable from the wind.

2. There are practical and operational reasons that determine that, below a certain wind level, it is not economically advisable to keep the wind turbine running. In the previous figure this wind corresponds to *point A*, around 4 m/s.

3. There is another range, between *point A* and around 6 m/s of wind speed, in which, if it is stopped, it is not advisable to start the wind turbine, based on statistical studies of the probable evolution of the wind. That is, if the wind is too low, the possibility that after starting it it will have to be stopped is high and therefore it is not worth starting it.

4. **For winds above the nominal**, **it is desired that the Power Train always works at a fixed speed**. This Power Train speed and the nominal power define *point D*.  
In theory, this *point D* should be on the blue curve, the MPPT one (to extract the greatest possible power from the wind), but that would imply that if a rapid rise in wind occurs from a value below the nominal to another above the nominal, the blade angle control mechanism must react very quickly.  
Instead of this, an area immediately before the rpms of point D (point C) is reserved in order to be in a better position for an evolution of the blade angle in case a gust occurs. This strategy includes a loss of productive capacity (the C-D curve is not on the blue curve, which means that for the existing wind it would be possible to find another operating point -other rpms- that would give more power).

5. The situation described above can be seen more clearly in the following figure, in which the evolution of the blade angle of attack (Pitch) as a function of the wind can be seen. It can be seen that the Pitch remains practically constant up to the nominal wind (close to 0º), i.e. in the MPPT zone. However, it changes very quickly when the wind exceeds the nominal. A large slope can be seen in the area around 14 m/s.

![](<lib/DFIG Curva Pitch vs Viento cerca del nominal.jpg>)

In conclusion, the **Operational Curve** (<mark>red</mark> <mark>curve</mark>) **of a variable-speed wind turbine** has the following operational zones:

1. From point A to point B: zone not usable to start the wind turbine, but tolerated in case it was already in production.

2. From point B to point C: zone that works with the MPPT algorithm.

3. From point C to point D: zone with operation close to the MPPT algorithm, but prepared for a rapid change of wind above the nominal.

4. Point D: This zone, **actually a point**, is the objective for any wind above the nominal.

The zone between points D and E is temporarily used for Power Train evolutions during wind gusts.

A more detailed explanation is given in [Maximum Power Point Tracking algorithm (Maximum Power Point Tracking)](AlgoritmodeSeguimientodelPuntode.md).

The application ["Operational curve of variable-speed wind turbines"](Listadereferencias.md) allows a complete study of the influence of the characteristics of the components of this type of wind turbines (Cp function of the blades, their radius, generator synchronous speed, gearbox ratio), as well as the air density and the chosen design parameters (points A, B, C, D and E) on this curve.

Finally, it is interesting to check the expected evolution of the Power Train rotation speed as a function of the incident wind shown in the following figure. Corroborating the theory explained above, the following figure shows the linear growth zone between points B and C, which is the zone where the MPPT algorithm is truly used. In the zone above point D, in steady state, the rpms are constant.

![](<lib/RPMs vs Viento.jpg>) Figure 2
