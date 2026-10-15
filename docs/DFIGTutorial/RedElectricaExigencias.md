---
tags:
- TSO
- transmission system operator
- electric grid
---

# Grid fault tolerance capabilities (Voltage-Fault-drive-through)

### General description of an Electrical Grid in a wide area

The distribution of electrical energy in a wide area, for example a State, from its generation points to the consumption ones, is carried out through a system generically known as the Electrical Grid. Its structure takes into account, among others, the following concepts:

- The minimization of Transmission costs.

- The ease of adaptation to customer requirements.

- The total controllability of the system.

![](<lib/Red Electrica.png>)

The Transmission part has the mission of minimizing the transmission costs and of having elements that allow the controllability of the supply. It is made up of a power transmission network, with voltages typically of 135 kV and higher, generally AC, although there may be very high voltage DC sections (> 400 kV) to cover large distances (several thousands of kilometers). This network is meshed (that is, there are several connection possibilities between one point and another of the network), so that there is the possibility of solving contingencies in a controlled way, for example isolating certain zones when there are problems without cutting the supply to other neighboring ones or those that receive energy through them.

The Transmission network begins in substations connected to the generation points of a certain power (generally above 20 MW) and ends in substations close to the consumption points (for example those that exist near cities). It contains transformation stations with the necessary switching and transformation elements (busbars, disconnectors, switches, transformers, etc.) to carry out the desired supply routing at each moment. The operation of this network is the responsibility of high-level organisms, frequently belonging to the State, and they are known by the acronym TSO (Transmission System Operator).

The electrical energy is distributed to the different consumers from substations connected to the Transmission network, through transformation centers (substations) that operate at voltages between 10 kV and 60 kV (typically between 15 kV and 36 kV) and where the connections to the different customers depart from. These connections work at a voltage that depends on the type of customer: Low Voltage (up to 1,000 V) for residential customers and up to small industries, or Medium Voltage (between 3,000 V and 20 kV for large-consumption industrial installations). This part is called the Distribution network and is managed, generally, in the liberalized markets, by companies independent of the TSO.

As shown in the previous figure, Wind Farms are electrical production centers that are connected (generally) to the Transmission network. As Wind Farms are installed in a given territory, their importance for the controllability of the Transmission network compromises its stability. The first Wind Farms (until the 2000s) were built with wind turbines built with squirrel-cage generators, with no or very little possibility of controlling the energy they could contribute to the grid. In addition, they imposed additional conditions on said grid, such as the need to supply reactive power during their start-up, to create the initial magnetic flux in the generator air gap. This need introduced an additional effort on the wind farm connection lines with the grid and made it less controllable.

Currently, when the participation of wind energy in the energy mix reaches 25% in some countries, with supply peaks that reach more than 50% (for example in Spain), the grid is stable thanks to the new capabilities of the Wind Farms and, in particular, to the characteristics of the DFIG wind turbines, which already constitute the bulk of the installed wind turbines.

One of the capabilities that have greatly contributed to this change in the qualification of Wind Energy as a reliable source, has been the ability to sustain production after the grid suffers important voltage drops (up to 100% in some countries - see [Grid codes](RedElectricaExigenciasGridCodes.md) -) during brief periods of time (less than a second). These situations are relatively common since they obey events such as a short circuit in the grid due to a tree falling on it, or some operation fault in an electrical substation.

This capability can be described in the following sentences:

- When these micro-cuts occur, the wind turbine must not disconnect from the grid, which means that it must be able to remain connected when the voltage is 0.

- When the grid voltage recovers, the wind turbine is obliged to supply, without delay, the same power level it was delivering to the grid just before the micro-cut.

The following graphs show the evolution of the rotor voltages, and the rotor and stator currents and powers, in a DFIG, when the grid voltage drops by 37.5%.

![](<lib/GE voltage sag 37 porciento.jpg>)
