---
tags:
- grid codes
---

# Grid codes

The problems that can occur in an electrical grid are very varied and can become very complex. One of these types of problems was brought to light with the growth of Wind Farms built with wind turbines with squirrel-cage generators (the first models, which were massively installed until the first part of the 2000s decade). The description of this problem derives from the following points:

- Squirrel-cage wind turbines demand an important current peak at the moment of connection with the grid (this derives from the fact that the generation of the magnetic flux in the air gap, so that the conversion of mechanical energy into electrical energy occurs, must be done with the only available winding: the stator).

- That current peak is also reactive. The importance of this fact derives from the fact that a reactive current peak at the end of the connection line with the Wind Farm produces a voltage drop at the generator terminals.

- The controllers of these wind turbines were designed to "protect the wind turbine" and not for the best of the grid that evacuates the produced energy. A result of this characteristic is that when a voltage drop occurs in the Wind Farm, the controller starts the cutout operation and withdraws the generator from the grid. When the grid restores the voltage back to "normal" values, the controller takes an important time (some minutes) to reconnect the generator to the grid. Unfortunately there are common phenomena that produce important voltage drops in the grid, although they last little: for example, a tree falling on the line. We can qualify this characteristic as an asymmetric response in time with respect to grid voltage variations.

The result of this behavior was an important conceptual limitation when deciding what percentage of electrical energy could come from Wind Farms. To solve this limitation, the TSOs (grid operators) defined the behavior required from the wind turbines that could be connected to their grids. This mandatory behavior is briefly explained in the graphs below, and can be summarized in the concept of "while the -short- change in the grid voltage is kept within certain limits, the wind turbine will continue the same production it had before starting said change". Example, in Spain if our wind turbine was supplying 1.5 MW before the voltage dropped 75% of its nominal value, if the voltage recovers in less than 500 ms, the wind turbine is obliged to continue delivering the 1.5 MWs when the grid voltage recovers.

This regulation is different in the different electrical grids (see below) and can also include specifications regarding the amount of reactive current that the wind turbine must supply or consume during the time the voltage is below or above the nominal one.

In English this regulation is known as "Grid Codes" and the capacity of a wind turbine to withstand it is called "Low-Voltage-Ride-Through capabilities".

The next two figures show the common concepts in all cases:

| ![](<lib/LVFRT voltios 2 casos.jpg>) | Interpretation: If the evolution of the grid voltage is within the gray zone (above the thick black line), the wind turbine is not authorized to disconnect from the grid. (Case of the thin red line). |
|---|---|
| ![](<lib/LFRT Reactive requirements.png>) | In some Grid Codes the obligation to support consumption or supply of current during short voltage drops and also rises is also specified. |

In the following graph the specification of the possible voltage evolution in the Grid Code of several countries is shown.

![](<lib/Gridcodes varios paises.png>)
