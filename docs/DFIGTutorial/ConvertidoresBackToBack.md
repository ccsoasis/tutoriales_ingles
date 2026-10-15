---
tags:
- subsynchronous
- rotor side converter
- RSC
- grid side converter
- GSC
- supersynchronous
- IGBT
- phase locked loop
- PLL
- pulse width modulation
- PWM
---

# Description of the Back-to-Back Converters

As discussed in [Implications for the Electrical Converter](ImplicacionesVeloVariableConvert.md), this structure of electronic power converters fulfills a fundamental and critical mission in a DFIG wind turbine. A brief summary of its properties and functionalities is the following:

- They must guarantee adequate operation in any situation with the grid frequency, within the margins specified by the grid operator. (See [Working area Power vs Frequency of the Grid](RedElectricaExigenciasAreaFuncio.md)).

- They must carry out the grid connection and grid disconnection operations smoothly, without producing transients in the grid.

- They must operate under the conditions imposed by the Power Train control:

- They must have the capacity to withstand brief cuts and overvoltages (Low and High Voltage Ride Through) according to the regulations to be applied in each grid. (See [Grid codes](RedElectricaExigenciasGridCodes.md)).

- They must be very reliable.
