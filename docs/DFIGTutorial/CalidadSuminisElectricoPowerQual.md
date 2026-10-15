---
tags:
- power quality
- flicker
---

# Power Quality

**Power Quality** is a broad concept that has emerged in recent years, coinciding with the deployment of Renewable Energies, although it also has a lot to do with the change in the type of non-linear loads (for example, certain electronic devices) and the need to have a more controllable Electrical Grid, among other things to avoid "supply 0s" (loss of supply in wide areas of the grid).

In relation to wind turbines there are two aspects that affect the quality of the produced energy.

The first has to do with the harmonic content: in the chapter [Implications for the Electrical Converter](ImplicacionesVeloVariableConvert.md) it is shown that DFIG wind turbines need the Back-to-Back converters, with a power that can reach 25% or 30% of the total nominal power of the wind turbine, and in [Operating principles](ConvertidoresBackToBackPrincipio.md) of these converters it is shown that the waveforms generally have a lot of harmonic content (i.e. little sinusoidal). To improve the supply quality in this aspect, the Back-to-Back converters have designs that minimize this harmonic content and also incorporate low-pass filters that eliminate those harmonics.

An important aspect of the supply quality has to do with the "**flicker**" that is produced by slow variations of the voltage level in incandescent lamps. It happens that in HAWT wind turbines (with the Power Train on a horizontal axis) the passage of the blades in front of the tower generates a frequency that falls within those that influence the flicker level. For example, a three-blade wind turbine rotating in production at around 20 rpms, the influence of the passage in front of the tower is 1 Hz (20 rpms * 3 / 60 s).

This is one of the reasons why in modern designs the pitch angle of each blade is varied as it passes in front of the tower, so that the power variation due to this effect is minimized.
