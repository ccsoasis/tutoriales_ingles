# Wind gusts with high winds

!!! tip "🎯 Wind gusts with high winds"
    ***Section objective:*** Study the DFIG behavior against wind gusts when the average wind is high (above the nominal), analyzing how the Controller uses the Pitch to maintain the power and how the Power Train Controller and the B2B interact.
    ***What to observe:*** The transient electrical power drops during descending gusts, the Pitch actuation with winds above the nominal, and the behavior near the "MaxWindForCutin" limit.
    💡 With wind above the nominal, the Pitch plays an active role. What exactly happens to the power during the descending part of a gust?

The experiment in this class is similar to the one described in [Wind gusts with low winds](Rfagasdevientoconvientosbajos.md), to check the great difference in the wind turbine behavior with respect to wind gusts depending on the average wind.

## First series:

Parameter: *NacellePitch.BladeSlewRate*= (5 º/s)/s ; Gust type="*StandardGust120x4*" ; initial wind: first at 7, followed by 8, 9 and 10 m/s.

![](<lib/DFIG WindGust Pitch speed 5 grados 120x4 7 a.jpg>)

### Comments:

- In the "Power" record, the evolutions of the "blue" zones similar to those in the figure:  
![](<lib/Detalle de cambios de viento.jpg>)  
correspond to the (in theory instantaneous) wind changes using the "Page Up" function keys.

- Note that the shape of the Electrical Power evolution is different when the initial wind is above 9 m/s: the reason is that this value corresponds approximately to the value from which the Operational Curve used by the Power Train Controller "exits" the Optimal Power curve (MPPT algorithm). See [Implications for the Power Train](../DFIGTutorial/ImplicacionesparaelTrendePotenci.md).

## Second series:

Parameter: *NacellePitch.BladeSlewRate*= (5 º/s)/s ; Wind Gust="StandardGust120x4" ; initial wind = first at 11, followed by 12, 13, 15 and 16 m/s.

![](<lib/DFIG WindGust Pitch speed 5 grados 120x4 11 a.jpg>)

### Comments:

- When the wind is above the Nominal, the Power Train Controller modifies the Pitch so that it maintains the Wind Power at the adequate level: the Back-to-Back must follow the evolution of this power, helping in the maintenance of the output power and in the Power Train rpms evolution.

- Note that during the transitions, *even when the wind is above the Nominal, there are small Electrical Power drops below the Nominal Power, in the descending part of the wind gust*. This occurs because when the operating point is point D, if there is a wind drop, even if its value remains above the Nominal, a temporary Mechanical Power drop will occur, until the Pitch change allows compensating the wind drop. In that phase, the case may occur (generally) that the power sent to the grid must evolve helping the Power Train Controller so that the stable situation is reached as soon as possible. In practice this is shown with small Electrical Power drops.

## Third series:

Parameter: *NacellePitch.BladeSlewRate*= (5 º/s)/s ; Gust type="StandardGust60x10"; initial wind = first at 7, followed by 8, 9 and 10 m/s.

![](<lib/DFIG WindGust Pitch speed 5 grados 60x10 7 a.jpg>)

### Comment:

The difference between the Third series cases with respect to the First, is related to the wind gust amplitude (10 m/s instead of 4 m/s) which implies that in all the initial wind cases (7 to 11 m/s) there is a time interval in which the wind is above the Nominal, and that forces changing the Pitch.
