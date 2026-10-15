---
tags:
- DriveTrain
- NacellePitch.BladeSlewRate
- Nacelle.DriveTrain.PitchNacelleOut
- Controller.Control.PitchOut
---

# Pitch mechanism change capacity influence

!!! tip "🎯 Pitch mechanism change capacity influence"
    ***Objective:*** Observe how a Pitch mechanism slew rate reduction (from 5 to 2 degrees/s) affects the wind turbine stability against gusts, and understand the rotor resistance control compensating role when the Pitch is not fast enough.
    ***What to observe:*** The difference between the Controller ordered Pitch and the real Pitch when the slew rate is slow, the RRC control (PWM) actuation to compensate, and the power peak that occurs when neither of the two mechanisms is sufficient.
    💡 With slew rate reduced to 2°/s and fast gust, can the RRC control compensate the Pitch slowness?

!!! warning "❓ Guiding questions"
    1. With 2°/s slew rate and slow gust (StandardGust120x4) with 15 m/s base wind: can the RRC control compensate the Pitch slowness to keep the power constant?
    2. With 2°/s slew rate and fast gust (StandardGust60x10): what happens to the generated power? Does it exceed the nominal power? Why is the RRC control also not enough?
    3. Why with low base wind (6 m/s) the reduced slew rate does not cause problems? What difference is there in the required Pitch changes with respect to the high wind case?

In this practice the objective is to observe the Pitch mechanism influence on the wind turbine stability.

Repeat the examples of the [Gusts with wind below the nominal](Rfagasconvientoinferioralnominal.md) and [Wind gusts with starting wind above the nominal](Rfagasdevientoconvientodepartida.md) practices but having previously changed the Pitch mechanism "Slew rate" value from 5 degrees/second to 2 degrees/second. To do so, open the "Parameters" synoptic and change the value in the "*NacellePitch.BladeSlewRate*" row.

You must obtain graphs in the "General" type recorder like the following:

## With 15 m/s base wind

![](<lib/Evolucion con rafagas lenta y rapida a 15 ms.jpg>)

#### Comments:

It is seen during the *slow* gust, the Pitch mechanism (*NacelleDriveTrain.PitchNacelleOut* in the first panel, in black) is not capable of following the Pitch ordered by the Controller (*Controller.Control.PitchOut* in red). However this deficiency is corrected by the rotor resistance control mechanism (NacelleDriveTrain.PWMOut in the second panel), which forces shaft speed changes.

However with the fast gust, the changes ordered by the Controller are not followed by the Pitch mechanism and the rotor resistance control mechanism cannot compensate it: due to this, a generated power peak occurs, which greatly exceeds the nominal, and also in the shaft speed.

Another interesting aspect to note is that in the fast gust descent, despite the wind being at all times above the nominal, the generated power drops below the nominal. This is because, when the wind drops, the Pitch must also drop, but the Pitch mechanism is not capable of following it, not even with the rotor resistance control mechanism at minimum resistance (PWM at 100%).

## With 6 m/s base wind.

![](<lib/Evolucion con rafagas lenta y rapida a 6  ms.jpg>)

## Comments:

In this case the Pitch mechanism follows the Controller ordered value quite well, despite being slower than normal. This is because, with low winds, the steady state Pitch is very close to 0 degrees, so the requested changes do not represent a problem.
