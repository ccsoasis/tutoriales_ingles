# About the unavailable wind turbines

Each wind turbine has power cables that connect it with the electrical Substation. These cables come out of the transformer associated with the wind turbine, which raises the generator voltage (typically 690 between phases) to a Medium Voltage level (typically between 15kV and 30kV). In this way the thickness of these cables can be smaller, since the current corresponding to the same power is inversely proportional to the transport voltage.

Generally the structure of these cable connections with the Substation is **not** "radial", which would imply one Substation entry per wind turbine. See "[**Territorial deployment**](../WFSSCADA/Landlayout.md)**.**" There is only a (small) set of entries in the Substation, each one connected to a set of wind turbines.

Each one of these entries must have a Medium Voltage switch (see in "**[Unifilar electrical schematic](../WFSSCADA/UnifilarschematicoftheSubstation.md)**" the switches marked "P1", "P2", "P3" in the lower part of the schematic, associated with the lines "C-1", "C-2" and "C-3"). It is important to take this structure into account because it has implications for the Farm Maintenance, since if it were necessary to carry out a maintenance operation on the Transformer part of some wind turbine, it would be necessary to cut the switch (C-1, C-2 or C-3) to which it is connected, which will cause all the wind turbines that share said switch to become disconnected. See in "**[Wind turbine connections](../WFSSCADA/IconicviewoftheWTsPCCandpowercab.md)**" the power cable layout and the "**Point of Common Connection**" (the Substation).

Additionally, the **Controller** of each wind turbine is connected with the SCADA through a **communications cable**, which is usually fiber optic, and which usually goes along the power cables. Through this cable, the SCADA *requests data* from, and *sends commands* to, the **Controller** of each wind turbine.

With these considerations, the causes for which a wind turbine may **not be available** are:

1. Problems with its transformer.

2. Problems with its transformer cables.

3. Problems with the communications cables between its Controller and the SCADA.

4. Problems with the Controller communications unit.

5. Problems with the SCADA communications unit corresponding to said wind turbine.

6. Operating problems of the wind turbine Controller.

7. Problems with some wind turbine component or subsystem, reported through the Controller.
