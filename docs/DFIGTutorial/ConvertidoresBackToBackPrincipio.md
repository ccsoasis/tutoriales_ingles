---
tags:
- IGBTs
---

# Operating principles

**Basic principles of the converters used in the B2B.**

The general scheme of the B2B configuration is presented in the following figure.

![](<lib/B2B esquema en colores.jpg>)

Power conversions are made towards the DC Link (the capacitor in the center) from the two possible sources: the grid or the rotor winding, and also from the DC Link towards the grid or towards the rotor winding.

These power conversions are carried out exclusively by opening or closing direct connections between these three points (Rotor, DC Link and grid). The switches that make these connections are **IGBTs** (*Insulated Gate Bipolar Transistor*): electronic devices that are made to operate as electrical switches that commute between the "conducting" and "open" states, with very low response times, in the order of microseconds. When they are conducting, the ohmic resistance is very low, in the order of milliohms, while when they are open the leakage current is very low (high impedance). When they are open there is a maximum value of the voltage they can withstand without entering a catastrophic failure. There are several families, and the current limit of this voltage is between 1,000 V and 3,300 V.

They have a limit in their dissipation capacity, which depends on the heat sink to which they are attached, on the thermal resistance of that junction and on the type of heat evacuation produced (forced with a fan or with an exchanger based on it). The power dissipated in these IGBTs depends on the current flowing through them when they are conducting and on the number of times per second they are in the intermediate phases of transition to conduction and transition to cutoff: this makes said dissipated power depend on the frequency at which they are operated.

As can be seen in the scheme, these switches commute between voltage sources and their ohmic resistance is very low: this situation (connection of two voltage sources, in principle with different voltages) cannot be sustained for long because the current through the device would be very large. The solution to this problem consists of placing an inductor in series with the switch, since in these circumstances, <u>this inductor limits the rate of change of the current flowing through the circuit</u>.

To illustrate this concept, we will analyze a circuit that uses this principle, used in most portable device chargers, known as "Booster". The basic scheme is shown in the following figure.

| ![](<lib/Boost converter 1.jpg>) | Booster-type voltage converter. |
|---|---|

The objective of this circuit consists of feeding a load (R<sub>L</sub>) at a certain voltage (V<sub>O</sub>) from a source (V<sub>I</sub>), whose value is different from V<sub>O</sub>. This version of the circuit is used when we want the load voltage to be higher than the available source (V<sub>O</sub> &gt; V<sub>I</sub>).

The "trick" of this circuit consists of using the property that inductors have to "store" electrical energy (during brief periods of time). Let us remember that a capacitor is also an electrical energy store: if we "charge" it (inject current) until we have a certain voltage across its terminals, and then we disconnect it, the capacitor will "maintain" that voltage for an indefinite time (if the capacitor has no losses). If the capacitor has losses and/or is connected to any electrical circuit, its voltage will decrease until it reaches 0, dissipating its energy in the load represented by the external circuit or its own internal losses.

One way of seeing this capacitor behavior consists of considering that, when it is charged, *it opposes any change in its voltage*, and the way of reacting is by "releasing" current, all the more so the greater our effort to make a rapid voltage change.

Inductors behave in an analogous way, but exchanging voltage for current. That is, if we want a certain current (I<sub>L</sub>) to flow through an inductor we have to apply a change of the voltage across its terminals with a certain rate of change. Once this I<sub>L</sub> flows through the inductor, if we try to make a change in that value, the inductor will react by varying the voltage across its terminals, opposing that change. A common case is the electrical circuit that feeds the spark plugs of a gasoline combustion engine. That circuit consists of a coil that is periodically connected to and disconnected from the battery. During the phase in which it is connected to the battery, the current through it grows; when it is disconnected, the reaction is to raise (extraordinarily) the voltage across its terminals, so that it is much higher than the battery voltage, in an attempt to maintain the previous current flow. This voltage rise lasts a very short time. In this way we can generate, with a very simple circuit, high voltages (> 15,000 V) from a 12 V battery.

The relationship between the voltage across the terminals and the current change per unit of time in an inductor is given by the following formula:

| V = L \* (Δ I) / (Δ t) | Where: V = voltage across the terminals. L = inductance value. (Δ I) / (Δ t) = rate of change of the current. |
|---|---|

In the previous circuit, the control mechanism to go from V<sub>O</sub> to V<sub>I</sub> consists of **controlling how long and when** **we must keep the switches open or closed**. The control algorithm is divided into two stages: a) inductor charging, b) transfer of the energy charged in the inductor to the load.

We will use an equivalent theoretical circuit of the previous one to make it more understandable.

A) Charging of the inductor L.

![](<lib/Boost converter 2.jpg>)

During a certain time we will put the IGBT into conduction. In this situation the diode will isolate the load from the inductor, since the voltage at its cathode (capacitor voltage) will be higher than the voltage at the right terminal of the inductor (which is set to 0 by the IGBT).

In this situation there will be a progressive increase of the current flowing through the inductor, in the direction indicated in the figure.

B) Transfer of the inductor energy to the load.

![](<lib/Boost converter 3.jpg>)

A certain time later, we open the IGBT and what will happen is that there will be a current flow (ID) in the direction indicated in the figure because the voltage of the right terminal of the inductor will grow due to its opposition to the change, so that a certain time later that voltage will be higher than the voltage across the capacitor: when that happens the diode will behave as a short circuit and therefore will allow the inductor current (which moments before flowed through the IGBT) from that moment on to flow through the diode to the capacitor and the load. The part of the current that flows through the capacitor will increase the voltage across its terminals.

That is, in this phase we have a transfer of the electrical energy stored in the inductor L to the circuit formed by the load R<sub>L</sub> and the capacitor C. The energy that passes to the load is dissipated, while the one that passes to the capacitor remains stored in it. This latter energy is the one that "feeds" the load during phase A, when it is disconnected from the inductor.

The value of the "average" voltage across the capacitor (V<sub>O</sub>) with respect to the voltage of the energy source (V<sub>L</sub>) will depend on the value of L, C, R<sub>L</sub> and on the relative times of phases A and B.

*In other words: if we have a circuit with a fixed installation (L and C), by managing the time relationship of phases A and B we can vary the voltage across the load; or also, we can adapt to variable loads (RL) by also changing the time relationship of both phases.*

An important conclusion of this approach is the change of paradigm of control of physical magnitudes from hardware to software.

### Obtaining alternating voltages

If in the previous circuit we remove the output capacitor and the diode, it is possible to vary the voltage across the load terminals. For this it is only necessary that the frequency of the signal governing the IGBTs be much higher than the desired frequency in the load (according to the Nyquist criterion, at least twice the frequency of the desired voltage in the load). The following figure shows the simplest example, where the time relationship of phases A and B is 1 (equal). The voltage across the load terminals corresponds to the black line. The gray line (the desired one) is obtained by introducing filters. The effect of these filters is to pass the voltage in the areas marked in green to the areas marked in blue.

![](<lib/Aproximacion 1.jpg>)

### Waveforms and "levels"

The previous waveform can be improved by using two power sources connected in series instead of one, and connecting the load to the common point between them. In this way, what is known as "three levels" is obtained. See the following figure.

![](<lib/Aproximacion 2.jpg>)

The following circuit implements this idea by creating the two sources from a single one and using two capacitors of identical value (C1 and C2) in series.

![](<lib/Convertidor esquema tres niveles.png>)

In this case, there are two circuits per phase (two sources and two IGBTs) that have their own control signal generators. The harmonic content of the resulting signal is lower than in the previous case, which implies that the output filters (the ones that connect to the load) are smaller.

Using special techniques, for example, pulse width modulation (PWM) for the control signals, it is possible to reduce the harmonic content even more. See the following figure.

![](<lib/Sinusoide PWM modulation.jpg>)

Similarly, there are circuits that add "levels" in order to minimize the harmonic content: see the following figure.

![](<lib/Aproximacion 3.jpg>)

This approach requires the generation of increasingly complex waveforms to excite the IGBT control gates. See the following figure.

![](<lib/DFIGB2Bv2 - B2B senal una fase.jpg>)

### Other specific requirements

The previous concepts apply to many types of converters, for example those used to supply variable-frequency power to squirrel-cage motors in order to control their rotation speed without having to lose power. Likewise, they are used in DC/AC converters, for example in uninterruptible power supplies.

In the case of the converters used in the B2B there are other important constraints:

#### Change of operating mode

When the wind turbine Power Train controller decides that its operating speed corresponds to a generator speed that is subsynchronous:

- The GSC must feed the DC Link and therefore must work as a controlled rectifier.

- The RSC must generate voltages and currents with two important conditions: a) that their frequency be the one corresponding to the desired Power Train speed and b) that their relative phase angles be such that the flux created by the rotor winding is adequately ahead of the one created by the stator winding.

For the particular case that the speed corresponds to the synchronous speed, the frequency of the rotor signals is 0, that is, direct current (on average), but presenting an impedance whose angle is a determined one, which depends on the power transferred by the Generator.

In the supersynchronous situation:

- Part of the electrical power comes out through the rotor winding and therefore the RSC acts as a controlled rectifier that feeds the DC Link; but in addition, for this to happen, the RSC must be "seen" from the rotor winding with a certain impedance (modulus and phase), which is also dependent on the power.

- The GSC must work as a DC (DC Link) to AC converter.
