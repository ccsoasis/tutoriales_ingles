---
tags:
- maximum obtainable power
- fixed speed
---

# By Active Pitch (to-the-feathers)

The Cp function (see [Aerodynamic coefficient](Conceptossobrelapotencia.md)) shows the complexity of the relationship between Cp and *TSR* (which in turn depends on wind speed, blade radius, and blade rotation speed) and blade angle (Pitch). However, if we look for the maximum Cp value for a given TSR across all possible Pitch values, we obtain the curve shown in the following graph. This curve is dependent on the blade shape, logically.

![](<lib/Cp vs TSR con TSRoptimo.png>)

Fig 1.

The interest of this graph is that it shows an absolute maximum: there is a TSR value for which Cp is maximum. It seems clear that when the wind is lower than the nominal, what matters is that the TSR at which we should make the wind turbine operate corresponds to that point (in the figure graph, this optimum TSR is around 7.8), since then we will be obtaining the greatest wind power.

Remembering that the TSR definition is:

TSR = 2 \* π \* BladeRadius \* (BladeRotationSpeed rpms)/60) / WindSpeed

The previous sentence implies that we should make the Power Train operate at a speed that depends on the incident wind:

OptimumBladeRotationSpeed rpms = 60 \* OptimumTSR \* WindSpeed / (2 \* π \* BladeRadius)

An important consequence of rotating the blades at this speed is that the maximum power extracted from the wind is proportional to the square of the Wind Speed (Wind2). The following graph shows the maximum power curves for a given blade type and several radius values, assuming that the TSR and pitch determine the maximum Cp value.

Typical values of this optimum speed, for the blade type corresponding to the previous graph, go from...

![](<lib/Curva velocidad optima rotor vs radio pala es.gif>)

Fig 2.

Another important conclusion from the previous graph is that you can determine a blade's maximum obtainable power from its Cpmax and length, as a function of wind speed. The following graph presents several curves for blades of the same design (i.e., the same Cpmax) and different lengths.

![](<lib/CurvasPotenciaVsVientoConRadioComoParametro_1.jpg>)

Fig 3

In this graph, the desired wind turbine Nominal Power value (target) is also shown; this value corresponds to the Electric Generator specification.

The minimum wind at which we want to obtain the Nominal Power is the Nominal Wind. That is, the nominal wind and power values determine the blade radius.

Below the Nominal Wind, the power obtained from the wind will be lower than the Nominal Power. Above this wind speed, the power may exceed the Nominal Power. Since the wind turbine electrical component is sized to deliver the Nominal Power, the wind turbine must have a mechanism that prevents the power extracted from the wind from exceeding the Nominal Power above the Nominal Wind. See [Control of the power collected from the wind](Coeficienteaerodinmico2.md).

IMPORTANT CONCLUSIONS:  
1- The Power Train, to always obtain the maximum available wind power in winds below the Nominal, requires operating at variable speed. This is an important condition for the electric Generator.  
2- The Power Train must include mechanisms or designs that guarantee that the mechanical power delivered to the electric Generator does not exceed its Nominal Power.
