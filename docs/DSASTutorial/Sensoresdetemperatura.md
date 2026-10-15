# Pt100 sensor measurement circuits

Pt100 type temperature sensors are devices that contain a platinum resistance, which is put in contact with the element whose temperature is to be measured. It is a very reliable sensor type with very widespread use in industry due to the stability of the resistance-temperature relationship. The resistance curve as a function of the temperature is also quite linear in the use range.

There are several values: the Pt100 type presents a resistance of 100 ohms at 0ºC, and has a proportionality coefficient of 0.385 Ohms/ºC. That is, the resistance value when the sensor is placed on an object at 100ºC is 138.5 Ohms (= 100 ohms + 100ºC * 0.385).

The measurement of this resistance has two problems: one derived from the low value of the temperature variations combined with the influence of the wire resistances that connect the sensor with the measuring device. The solution consists of using a measurement circuit like the one shown in fig 1: R1, R2 and R3 correspond to the wire resistances that join the R<sub>PT</sub> sensor with the measuring device (located at terminals L1, L2 and L3).

.![](<lib/Sensor_Pt100.png>)

![](<lib/Circuito Pt100 3 hilos.jpg>) Fig 1

By construction the R1, R2 and R3 values are very similar. If the resistances between terminals L3 and L2 are measured, and then between terminals L2 and L1, the R<sub>PT</sub> resistance is the difference between the two.

A similar concept is used with the 4-wire method.

![](<lib/Circuito Pt100 4 hilos.jpg>)

The idea is based on the fact that any voltage measuring instrument has a large impedance (above 1 M ohms) and therefore, if a known current is injected between terminals L1 and L4, only a negligible part will flow through L3 and L2, so that the voltage measured in the voltmeter (DVM) will be the same as the one at the R<sub>PT</sub> terminals.

The other problem derives from the fact that injecting current into the R<sub>PT</sub> to make the measurement, heats the R<sub>PT</sub>, so the measurement is distorted. This error depends not only on the current, but on the R<sub>PT</sub> thermal characteristics and the point where the measurement is made.

To solve this problem, some systems use a short current pulse mechanism, in which they make the measurement.
