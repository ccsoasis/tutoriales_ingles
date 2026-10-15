---
tags:
- angular encoder
- rotary encoder
- PLL
- phase locked loop
---

# Grid requirements

### The need for synchronization of the B2B signals with the grid.

The grid frequency is not fixed, but can take a value between two extremes (see [Working area Power vs Frequency of the Grid](RedElectricaExigenciasAreaFuncio.md)). For example, in Spain the limits are between 47 Hz and 52 Hz. The frequency variations come from a set of circumstances that alter, during short time intervals, the power distribution balance along the grid. When there are sudden load incorporations, short circuits in the lines, power losses in one of the generators connected to the grid, etc., a change in the grid stability situation occurs that implies a variation of the generator shaft speeds and these variations imply a variation of the frequency of the powers delivered to the grid.

Additionally, the B2B converters of DFIG wind turbines allow controlling both the active and reactive power (something that other classic generators - from thermal, hydraulic, nuclear plants - cannot do) and because of this they must know precisely the relative phases with respect to the grid signal.

To be able to do an adequate tracking, the B2B controller receives the signal from an angular encoder connected to the Generator shaft and monitors the grid signal using a PLL circuit (Phase-Locked-Loop) to be able to track the frequency evolution. The output signal of this circuit, whose frequency derives from the grid, is used as a "master clock" to elaborate the other IGBT control signals.

The *angular encoder* (also known as *rotary encoder*) used is of the "absolute" type, and serves to measure the angle of the Generator rotor shaft with respect to a reference position. This reference position needs to be calibrated for a correct operation of the B2B converters.

Using both signals (angular encoder and PLL) it is possible to know the angle of the magnetic fluxes in the Generator air gap, which constitutes the mechanical-to-electrical power conversion point.
