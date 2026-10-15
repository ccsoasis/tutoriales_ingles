# IGBTs

IGBTs (Insulated gated bipolar Transistor)

It is a bipolar transistor controlled by an isolated gate. Figure 3, below, shows a transverse cut.

These devices are capable of maintaining high voltages when in open mode (in the order of 1200 V to 3500 V) while conducting high currents in closed mode (thousands of amperes). They are the most stressed converter components and, therefore, the ones that most influence its reliability. This characteristic also conditions how they are delivered, normally in packages together with protection diodes or a set of several units to facilitate the coupling with the heat sinks. See the following table.

| ![](<lib/IGBT simbolo.jpg>) Fig 1 Typical symbol associated with IGBTs | ![](<lib/IGBT internal schematic.jpg>) Fig 2![](<lib/IGBT seccion transversal.jpg>) Fig 3 Equivalent circuit |
|---|---|
| IGBTs are usually sold in independent units, or also packaged in units that facilitate their interconnection and assembly (Wikipedia.com source) |  |
| ![](<lib/IGBT Modulo 1.png>) Up to 1200 Amps and 3300V | ![](<lib/IGBT_Bloque.png>) Up to 30 Amps and 900V |

The power dissipated by an IGBT used as a switching element has two important components: blue and yellow zones.

![](<lib/NewItem1.png>)

The indicated times correspond to:

| **t**<sub>**d(on)**</sub> | response time to a gate-emitter voltage change from non-conduction to conduction |
|---|---|
| **t**<sub>**r**</sub> | time corresponding to the maximum current rise in the IGBT |
| **t**<sub>**d(off)**</sub> | response time to a gate-emitter voltage change from conduction to non-conduction |

- 1.The power dissipated while it *conducts*: this power is determined by the current flowing through it and by the collector-emitter conduction voltage. <mark>Yellow</mark> zone in the previous figure.

- 2.The power dissipated during the *transitions*:  
This power, which can be very important, derives from the fact that, when the cutoff operation starts (for example in a circuit containing inductors, like the Back-to-Back converters) it is not instantaneous and a rapid collector-emitter voltage rise occurs while the collector current has not yet been reduced.  
*This power depends on the IGBT conduction cutoff response time and also on its gate control signal frequency*. <mark>Blue</mark> zone in the previous figure.

The power dissipated by the IGBT must be dissipated so that it remains in acceptable operating conditions. For this, the IGBTs are mounted on a *heat sink* to which they are attached, which decreases the *thermal resistance* between its interior and the exterior (which carries the heat away) and the *heat evacuation type* produced (forced with a fan or with an exchanger based).
