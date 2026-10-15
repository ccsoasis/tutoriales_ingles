---
tags:
- main switch
- internal view
- power factor
- capacitor bank
- UPS
---

# Electrical panel

This panel mimics the Electrical Panel of a Rotor Resistance control type wind turbine.

![](<lib/Panel electrico - exterior.jpg>)Fig

Exterior the "**Main switch**" is seen.

With the boxes marked "1", "2" and "3" Electrical Grid phase faults can be simulated: they can be understood as mimics of the per-phase fuses.

By activating the "**Internal view**" box the synoptic changes as shown in the following figure.

![](<lib/Panel electrico - interior.jpg>)

The left panel includes the power cable entry to the electrical grid (lower part), which are connected to the "*Main switch*". The other contacts of this switch connect to the power cables that go up to the nacelle and [connect to the electric generator](Esquemaelctrico.md).

In the right panel the wired logic part is found (relay panels), the Controller (made with an industrial PC or with a PLC (Programmable Logic Controller)), and the *UPS* (Uninterruptable Power Supply) that feeds it in case of grid fault or disconnection.

In the lower right part a **capacitor bank** used to compensate the *Power Factor* is shown.
