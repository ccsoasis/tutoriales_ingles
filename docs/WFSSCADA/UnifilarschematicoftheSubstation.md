---
tags:
- electrical measurement units
- reactive power
- substation
- unifilar
- wind farm
- point of common connection
- power cables
- unifilar diagram
- three-phase line
- maintenance operations
---

# Unifilar electrical schematic

The **electrical Substation** includes the transformer that raises the wind turbine output voltage, normally in Low Voltage, 690 V, although there are also with Medium Voltage output (between 3KV and 5KV) up to the evacuation line level, which is usually in High Voltage (&gt; 110 KV), although there may be Medium Voltage connection cases (&gt; 30KV).

Generally, depending on the Farm extension, each wind turbine output has a step-up transformer (typically from 690 V to 15KV or 20 KV), in order to reduce the losses in the connection cables with the Substation transformer.

In the Substation are the *cutting devices* (disconnectors and *switches*) that allow connecting the evacuation line transformer, and the operation *'cells'*, which, in turn contain the cutting devices that allow connecting and disconnecting the cables that connect with the wind turbine transformers: this functionality is required to be able to carry out works that require the deactivation of some of these cables.

Additionally, and to comply with the operation regulations, in the Substation there are standard control mechanisms, that monitor: a) the grid frequency; b) that the voltage is within certain limits, c) the temperatures of certain elements, etc.

In the following figure the "**unifilar diagram**" corresponding to the example wind farm Substation is shown. The "unifilar" concept corresponds to a simplified representation in which each line in the drawing corresponds with the three (only the three phases), or four (three phases and the neutral) electrical wires of a three-phase line.

![](<lib/Esquema-unifilar-subestacion.png>)

In the upper part the connection with the Electrical Grid connection line (aerial in this case) is shown: in this case at 220 KV.

The connections with the wind turbines are concentrated in three lines C-1, C-2, and C-3. The wind turbine connection is made in "daisy chain": from one to the next closest. To each one of the wind turbines one of these cables arrives, and internally they have devices for their connection/disconnection.

These lines can be in Medium Voltage (as in this case) with voltage between 15KV and 30KV, although there are also wind farms where the wind turbines are connected to Low Voltage (690V), which is usually the electrical generator output. The Medium Voltage connection makes the installation more expensive (transformers in each wind turbine to raise from 690V to Medium Voltage), but reduces the transmission losses.

Between the High Voltage output and the wind turbine connections are:

- The **Disconnector** "89 L". This device has two fixed positions: a) one in which it connects the lower circuit to the Electrical Grid, and b) another in which this circuit is grounded. Position b) is used to carry out Substation *maintenance operations*. ***This device cannot be operated*** (that is, its position cannot be changed from a) to b) or vice versa) ***if there is current or there can be current through it***. That is, it can only change position if the Switch "52 L" is open.

- The **Switch** "52 L" is the main cutting and connection element of the Substation. ***This device can change state in any situation***: that is, it can open having the Electrical Grid connected (Disconnector "89 L" closed) and the wind turbines connected (C-1, C-2 and C-3 closed) and in production. Likewise it can open in these same circumstances.

- There are **voltage measurement transformers** (220 KV to 110V) connected to the Electrical Grid (when "89 L" is closed) and **current measurement transformers** in each phase.

- The previous transformers feed various **protection elements** ("*relays*") where:

- othe voltage and the current in each phase are monitored with their maximum values,

- othe power circulating through the lines is calculated (entry - consumption -, output - production -), and

- othe Grid frequency is monitored. A list of these relays is found in [Legend of the symbols in the unifilar schematic](Legendofsymbols.md). The output of these protection elements governs the Switch "52 L" control. This Switch can also be commanded from the Farm SCADA.

- A **step-up transformer**, from 20 KV to 220 KV, in delta/star configuration, so that the ***possible phase imbalances*** are isolated.

- **Protection elements** against over-voltages.

- A Disconnector followed by a Switch that connects with the Substation "busbars" to which the wind turbine connections are connected, through Disconnector + Switch sets.  
The objective of these sets is to be able to disconnect a C-x line, without having to disconnect the others.
