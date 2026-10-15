---
tags:
- meteorological station
- datalogger
- datalogging
- wind turbine
- wind speed
- wind gust
- wind direction
- striprecorder
- signal
- anemometer
- temperature
- measured wind
---

# Meteorological instruments

Each wind turbine has its own instruments for measuring the wind intensity, direction, ambient temperature, etc., so that they can work without receiving information from any sensor external to the wind turbine.

However, the Wind Farm has similar sensors, located in a significant place within the Farm, where these parameters are also measured, in a **meteorological station**.

![](<lib/Torre meteorologica espaol.png>) Fig 1

Generally wind measurements are made at two heights, in order to be able to know the turbulence existing at each moment. The meteorological station sensors are connected with the SCADA.

It is interesting to remark that the wind speed measurements of the meteorological station can differ from those existing in each one of the Farm wind turbines. This is because these are in different locations, which can be very separated from each other, and also to the measurement method used in the wind turbines. In these, the anemometers are usually located in the Nacelle rear part (see [What is a Wind Turbine?](WhatisaWindTurbine.md)). Due to this, the wind measurement corresponds to the wind that passes through the blade turning plane, and therefore corresponds to the incident wind minus the one used to move them. This can be appreciated in real measurements in a wind turbine in production, as shown in the following figure.

![](<lib/Datalogger-Efecto-cambio-pitch.png>) Fig 2.

It can be appreciated that the significant changes of the blade angle (Pitch), at the instants 20:26:40 and 20:27:20, influence the *'measured wind',* which has an evolution that does not correspond with the real wind evolution (much more stable). That is, the wind measured a few seconds after the angle goes to -5º, and the wind turbine is not connected and does not generate power, corresponds with the 'real wind' incident on the blades; in the graph it is appreciated that this value is approximately 2 m/s additional over the value measured when it is in production.
