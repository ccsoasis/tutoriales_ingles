---
tags:
- aerodynamics
- pitch
- power
---

# Power and Pitch vs Wind

## Power and Pitch as a function of the Wind

In this panel two variables are presented on the ordinate axis: Wind Power and blade Pitch as a function of the Wind.

The ordinates are drawn in "pu's". The corresponding reference unit values for each of the variables are indicated on the graph (1,500,000 W for the Power and 26.29º for the Pitch).

The gray curve corresponds to the Power and the green curve corresponds to the Pitch, and they represent the values of both magnitudes in a stable situation (steady state): that is, the value they will tend to when a reasonable time is expected after changing the wind. Therefore this panel is very useful to observe how the instantaneous values evolve during the transition phases to the responses to wind changes, for example, during wind gusts.

The instantaneous values are indicated by two icons: ![](<lib/Icono aspa potencia.jpg>) for the Power and ![](<lib/Icono circulo verde pitch.jpg>) for the Pitch.

The buttons labeled "in pu's" allow changing the representation mode of the corresponding value between "pu's" and "kWs" in one case, and "degrees" in the other.

![](<lib/Panel Potencia y Pitch vs Viento espanol.jpg>)

In a stable situation, the icons corresponding to the instantaneous Power and Pitch are on their corresponding curve.

The graphs in this panel reflect the evolution described in [Implications for the Power Train](ImplicacionesparaelTrendePotenci.md).

The Pitch curve has several zones. While the (stable) wind is in the zone between point B and point D, its value is very close to 0º, which for the TSR values corresponding to this wind margin corresponds to maximum Cp. This corresponds to winds between 5 m/s and the nominal (around 11 m/s) and it is the zone in which (for the most part) the Controller uses the MPPT algorithm (see [Maximum Power Point Tracking algorithm (Maximum Power Point Tracking)](AlgoritmodeSeguimientodelPuntode.md)).

As it becomes necessary to limit the power extracted from the wind, the Pitch begins to grow. The evolution of this curve for winds above the Nominal has two sections: an initial one in which the curve slope is low, between 11 m/s and 13.5 m/s. This translates into the capacity of the mechanism that controls the Pitch to make the changes requested by the Controller being small compared to the capacity required in the next zone, between 13.5 m/s and 14 m/s. This latter slope is the one that determines the mechanical power required from the Pitch mechanism. This slope depends on several factors, among them the blade radius and the gearbox ratio. See our "*Operational Curve for Variable Speed Wind Turbines*" application ([Reference list](Listadereferencias.md)).
