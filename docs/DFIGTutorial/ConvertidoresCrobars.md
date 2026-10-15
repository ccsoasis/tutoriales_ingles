---
tags:
- crowbar
- low-voltage-fault-ride-through capability
- power train
---

# Auxiliary circuits for the control of the response to Grid Codes: Crowbars

The capacity to withstand the behavior specified in the [Grid Codes](RedElectricaExigenciasGridCodes.md) determines the characteristics of the Back-to-Back converters and also the Power Train control algorithms. The latter occurs because when a very rapid voltage drop occurs, the electrical power "follows" the voltage (that is, it drops). However, the mechanical power received by the Power Train remains constant, since it depends on the existing wind (which we can assume does not change) and on the blade Pitch (which does not change either because the control mechanism has a very slow response time compared to the duration of these voltage drops). The result is that the balance that existed

*(Input Mechanical Power = Electrical Power delivered to the grid + Various losses*)

is broken and an "available" mechanical power appears whose effect is the acceleration of the Power Train.

This acceleration must be controlled since the Power Train rpms have an upper limit (point E in [Implications for the Power Train](ImplicacionesparaelTrendePotenci.md)), not far from the operating point in production (point D in the same figure). If the Power Train rpms exceed point E, the Controller launches a high-priority stop process (that is, using the hydraulic brake) which is considered a fault in itself.

On the other hand, if we need the production conditions to "return" immediately after the grid voltage is recovered, we need the Power Train rpms to remain at their initial value during the transient.

A common mechanism in DFIGs consists of using a resistive load that is connected to dissipate this mechanical power during the transient. It is known as "**CrowBar**" in English and is usually placed in the Rotor circuit, as shown in the following figure.

![](<lib/GraficoDFIG.jpg>)

This CrowBar is connected to the Rotor with a fast switch: there are versions in which this switch is made with Thyristors (more economical) and in others with IGBTs. The different switches in the figure change during the momentary voltage drop, to adapt to the requirements imposed by the Grid Code.

The basic concepts for the analysis of this type of configuration are the following:

- During a significant grid voltage drop, the Power Train rotation speed cannot change much, due to its significant inertia. This characteristic is important to achieve that the same situation is maintained when the voltage is restored.

- During the voltage drop, the stator current increases (since its voltage has dropped), which induces a proportional increase in the rotor current. We can distinguish two cases depending on the rotor revolutions:

In the [Electrical cabinet](DFIGArmarioElectrico.md) synoptic the relative size of a Crowbar can be seen. In the following figure several schemes for its implementation can be seen. The most common are the rotor ones.

![](<lib/Crowbars espaol.png>)

In case a) the disconnection is difficult, which complicates the control algorithm and limits the applicability cases. In case b) it is possible to connect the Crowbar resistors at any time of the cycle, which expands the degree of controllability of this unit.

Case c) is similar to a) but placing the dissipation resistors in the stator connection: in this case there is a continuous loss during normal production situations, in which the thyristors remain in conduction, so that the resistors remain "short-circuited"; when dissipation in the resistors needs to be activated, the thyristors are de-energized. This solution is very rarely used.
