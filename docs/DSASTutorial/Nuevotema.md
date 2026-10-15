---
tags:
- thyristor
- anti-parallel
- soft starter
---

# Thyristors

## Description of a Thyristor

A Thyristor is a solid-state semiconductor device that works like a diode, that is, the current conduction is unidirectional, from the Anode to the Cathode, provided that the Anode-Cathode voltage is positive, but, in addition, only if the Gate-Cathode voltage has exceeded a certain value.

Its characteristic curve and its layer structure is shown in the following figure.

![](<lib/Semikron_Thyristor.jpg>)

![](<lib/power-thyristor.jpg>)

## Typical circuit

![](<lib/tiristor_circuito1.gif>)

In the previous figure an electrical circuit is presented that can be used to control the light emitted by a bulb using a thyristor.

When the switch S<sub>1</sub> is closed, the circuit formed by the resistor R<sub>t</sub> and the capacitor C reproduces the V<sub>AC</sub> signal at the C terminals, but <u>*delayed in time*</u>. When this C voltage exceeds the <u>conduction value of the diode D</u><sub><u>1</u></sub> (approx 0.6 V) plus the voltage necessary to <u>excite the SCR thyristor gate</u> (a value below "*Forward break over*"), then the thyristor starts conducting. This is shown in the graph at the top right ("*Conduction*").

The more the excitation moment of the thyristor gate is delayed, the less the time in which it will be conducting, and therefore the <u>average of the current flowing through it in one cycle</u> will be less. The light emitted by the "*Lamp*" bulb is greater the greater this average current. That delay is proportional to the R<sub>t</sub> and C values, that is, the greater R<sub>t</sub> the entry into conduction moment will be more delayed, and therefore the conduction time will be smaller. That is, **greater R**<sub>**t**</sub> **⇒** **less light**.

This is the same principle used in the [Soft starter](Softstarter.md), only that in each Electrical Grid phase two thyristors are placed in "**anti-parallel**", that is, joining the cathode of one with the anode of the other, so that the circuit works in both half-cycles.
