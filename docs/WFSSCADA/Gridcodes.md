---
tags:
- blade
- grid code
- pitch
- wind
- wind farm
- wind gust
- wind turbine
- grid
- TSO
- stability
- grid codes
- grid codes
- extensive territory
- Low Voltage Ride Through capability
---

# "Grid codes"

Due to the fact that, in many countries, the Wind Farm contribution to the total electrical production is considerable, it has been necessary to consider their influence on the Grid "**stability**". The electrical supply grids must be maintained in operating conditions that guarantee that a generalized supply cut will not occur in an *extensive territory*. To do so they are designed attending the expected evolution of the consumptions in each node. Initially, the guarantee of this operation resided in the generator type (basically large synchronous generators), with a great inertia. When the wind penetration increased, two variations on the previous situation were introduced: a) the wind is an uncontrolled energy source; b) the wind turbine inertia was considerably lower than that of the generators associated with the thermal, hydraulic, nuclear plants, etc.

The first problem has been addressed through an anticipated knowledge of the wind evolution, together with a precise modeling of the consumption evolution in each grid node.

However, the response to very fast changes (of the order of 1 s or less), that occur in the normal operation of Distribution Grids (for example, the fall of a tree on the electrical wiring) generates dynamics that can be well tolerated by the large synchronous generators, but that could not be supported by the initial industrial wind turbines (those installed until the end of the 90s). The design of these wind turbine models was based on "protecting the wind turbine": the form of this protection consisted of detecting anomalous situations (for example, a phase fault) and disconnecting the wind turbine from the Grid immediately.

This reaction against Grid faults of those initial wind turbines had a perverse effect on the Grid stability. To understand this effect let us think about the following sequence: let us suppose that we have a 25 MW Wind Farm and that a momentary supply cut occurs. This can happen due to a short circuit in a phase, for example, that triggers a protection procedure (typically momentary line disconnection, since it is known that this operation can, by itself, resolve the problem). If the momentarily disconnected line is in the connection circuit with the Wind Farm, and assuming that the wind turbines of this Farm only have the self-protection mechanism, a cascade reaction will occur so that, in a very short time, the whole Farm will be disconnected from the Grid. That is, a "minor" problem (a tree branch on the electrical wiring) ends with the production loss of a complete plant, that is, a "major" problem for the Grid stability.

Due to this behavior, the entities in charge of the general Electrical System stability control modified the conditions that any electrical production Plant had to assume, especially the Wind Turbines, so that they did not disconnect from the Grid when the Grid itself produced, at the Connection Point, brief supply cuts (typically less than 1 second). These regulations are known as "**Grid Codes**" or "**Códigos de Red**", and vary from one country to another, due to the different capacities of their corresponding electrical Grids.

The specification is complex and is shown in the following graphs:

![](<lib/GridCode1.png>) Fig 1.

The zone marked in red is the Grid voltage evolution zone in which the Wind Turbine cannot disconnect. That is, if a Grid voltage drop occurs, but it is kept within the red zone, the Wind Turbine *must continue generating*.

In the following figure two voltage evolutions are shown. The green one is always within the red zone, and therefore the Wind Turbine cannot disconnect without breaching the regulation. However, if the evolution is the blue one, which leaves the red zone at the instant 0.15 seconds after the incident start, it can do so without breaching the regulation.

![](<lib/GridCode2.png>) Fig 2.

The wind turbine capacity to support "Grid Codes" is called "**Low Voltage Ride Through capability**" in English.
