---
tags:
- Cp
- moment of inertia
---

# Reasons for the development of Wind Turbines with Rotor Resistance control

This type of wind turbine constitutes an evolution of the wind turbines that use asynchronous squirrel-cage generators, which constituted the greatest percentage of those installed at the end of the 1990s decade.

The main reason for the development of this type of wind turbines was due to the need to have a design that allowed withstanding wind gusts without increasing the tower and pitch change mechanism sizing, and maintaining the use of induction generators for their low cost, reliability, and availability of multiple suppliers.

To explain this solution we will make the following considerations:

#### Consideration 1: the electric generator must be protected.

The electric generator must be sized for the desired nominal power. That power must be the one applied, at most, to its shaft.

If the generator is induction with short-circuited rotor, like the one used in previous wind turbines (see DSAS Simulator), its shaft speed, in production, must remain above the synchronism one, but with a very small slip (typically below 1%) (see [Induction generators with variable Rotor Resistance](GeneradoresdeinduccinconResisten.md)); that is, it must be practically constant.

#### Consideration 2: wind gust impact.

The wind gust effect derives from the *great influence* of the wind speed on the power incident on the blades, governed by the following formula:

**ExtractableWindPower** = 0.5 \* *AirDensity* \* *BladeSweptArea* \* ***Wind***<sup>3</sup>   \* ***Cp***(*Wind*, *BladeSpeed*, *PitchAngle*)

Where [Cp](Coeficienteaerodinmicodelaspalas.md) is the blade aerodynamic coefficient, which depends on the blade attack angle (Pitch).

The following figure graphically illustrates these considerations. In it the maximum extractable wind power is presented (that is, assuming that the blade pitch angle always has the adequate value to maximize said power), with several blade length values. Using for example the 48 m radius case, we see that the 'desired' power (horizontal line at 2 MW) corresponds to a 10 m/s wind. We can see that, if the wind rises to 13 m/s, the obtainable wind power rises to 3.5 MW, approx 1.75 times the nominal power.

![](<lib/CurvasPotenciaVsVientoConRadioComoParametro_1.jpg>)

To avoid the mechanical rotation power in the Power Train exceeding the electric generator nominal, the Controller modifies the Pitch angle, so that the Cp() is reduced.

Let us now consider: a) *the wind speed rate of change* and b) the *Pitch angle change mechanism* characteristics.

If we can change the Pitch faster than the wind changes, the Controller can use a power tracking algorithm so that it never exceeds the nominal power. There are additional considerations related to the moment of inertia of the blades themselves around their rotation axis, and that are also fixed to the hub, which in turn rotates on the Power Train rotor, which has maximum values that should not be exceeded.

However, if we cannot change the Pitch fast enough, we will have that a rapid wind rise (gust) will generate a mechanical power peak applied to the generator shaft, which can very quickly exceed its nominal power.

**Consideration 3: possible power peaks can be absorbed by accelerating the Power Train**

The idea is to consider that, normally, the Power Train has a large **moment of inertia**, which can be used to **absorb the power peaks due to gusts** that the pitch mechanism cannot counteract, letting this extra power accelerate its rotation speed.

This proposition has the drawback that it cannot be done if the generator is induction with short-circuited rotor (squirrel cage): the solution adopted in the wind turbine type like the one of this Simulator, is to keep using an induction generator, but with an electronic device that allows varying the rotor resistance. This characteristic allows the generator to operate with much greater slips (up to 15% or 20%). See the explanation in [Induction generators with variable Rotor Resistance](GeneradoresdeinduccinconResisten.md).
