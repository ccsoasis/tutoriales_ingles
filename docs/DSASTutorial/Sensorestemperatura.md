---
tags:
- Pt100
- bimetallics
- thyristors
---

# Temperature sensors

The wind turbine has temperature sensors for different elements. The sensor type depends on the monitored element type and the measurement precision need. For example, to sense the Thyristor temperature, or the yaw motors, generally sensors based on bimetals are used, calibrated for the corresponding temperature. These sensors are shown in closed circuit when the temperature is lower than the calibration one and in open circuit if it is higher.

![](<lib/sensor temperatura bimetal.png>)

![](<lib/Sensor temperatura bimetal ejemplo.gif>)

Other elements, for example, the Electric Generator, or the rotor bearing, require a more precise temperature measurement, so that a finer tracking of its evolution can be made.

The more precise measurements that require greater reliability are made through **Pt100** type sensors, widely spread in industry and that present a very well known and stable behavior, and adequate precision level.

The physical effect used is the resistance variation of a conductor as a function of its temperature. These sensors are of Platinum and their nominal value is small, typically 100 ohms, although there are also 1,000 ohms ones.

The resistance relationship with the temperature at which the resistance is, is quite stable in Platinum and follows a reasonably linear rule.

The main problem this sensor type presents consists in its resistance measurement. Being of small value and at a considerable distance from the electronic device that makes the measurement, it is necessary to avoid the problem of the cables that connect the Pt100 sensor and its measurement system, and also to reduce to the maximum the current used in making the measurement, since this current 'heats' the resistance and therefore falsifies the measurement.

The procedure, very well known in industry and in laboratories, is known as the 3 or 4 wire method. See [Pt100 sensor measurement circuits](Sensoresdetemperatura.md).
