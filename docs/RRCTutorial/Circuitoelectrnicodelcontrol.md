---
tags:
- IGBT
- slip
---

# Control electronic circuit

In the following figure the *simplified circuit* used to change the rotor resistance is shown, corresponding to *one grid phase*.

![](<lib/RRC circuit de control.jpg>)

Fig 1

The idea is to use an [IGBT](IGBTs.md) (*Insulated Gate Bipolar Transistor*) as a switch that can commute at high speed between short circuit and open circuit.

In the figure 1 circuit, the external resistance is made up of a resistance *Rext* in parallel with a circuit consisting of a rectifier bridge at whose output the IGBT is connected.

When the IGBT gate-cathode voltage exceeds a certain value, between the IGBT anode and cathode there is a very small resistance (milliohms), which we will call *IGBT*<sub>*On*</sub>. When this gate-cathode voltage is below that value, the resistance between anode and cathode is very high, which we will call *IGBT*<sub>*Off*</sub>.

The voltage at the rotor terminals has a frequency that is

***RotorFreq = StatorFreq \* Slip / MagneticPoleNumber***

Where *StatorFreq* is the grid frequency to which the stator is connected. For example, in an induction machine of 2 magnetic pole pairs fed at 50 Hz, when the slip is 4%, the rotor AC signal is 1 Hz (= 50 * 0.04 / 2).

If we make the signal applied to the IGBT base commute between On and Off at a speed much greater than this rotor frequency, the rotor will only notice the averaged value of the IGBT<sub>On</sub> and IGBT<sub>Off</sub> resistances depending on the time the IGBT is conducting. IGBTs can be used with switching frequencies of several kHz.

Ignoring the rectifier bridge influence, the equivalent resistance of the circuit to the right of the rotor is:

![](<lib/Formula Requiv IGBT.jpg>)

Where *DutyCycle* is the proportion of time it is On with respect to the signal total period.

In figure 2 the two extreme values have been labeled corresponding to the maximum DutyCycle value (100%) which corresponds to the IGBTOn case, and the other extreme where DutyCycle is 0%.

In [Power vs Rotor Slip](PotenciavsDeslizamientodelRotor.md) the various cases are described in more detail.

![](<lib/RRC Power vs Slip rotulos IGBT.jpg>) Fig 2
