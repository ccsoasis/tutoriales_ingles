---
tags:
- stop
- cutout
- idle
- cutin
- TSR
- brake released
- hydraulic brake circuit
- fail-safe
---

# Brake control algorithm and signals

The control algorithm used in the brake system obeys the following ideas:

- 1.**"Fail/Safe" design principle**: this principle establishes that a device that controls an important part of a system must be designed so that, if it fails, it leaves the system in a "safe" position.

- 2.**Allow a rapid Power Train stop**. This need comes from the secondary use of the brake mechanism as a "safety alternative", in case the Power Train cannot be braked by aerodynamic means.

- 3.**Minimization of the number of sensors and actuators**.

<mark>This power train brake mechanism is NOT the mechanism used for</mark> <mark>*stop*</mark> <mark>(</mark><mark>*cutout*</mark>) operations: these operations are carried out using aerodynamic methods, that is, using the blades, changing their attack angle, or, in some old models that did not have a pitch change mechanism, through a change in the shape. See the following figure.

However, in exceptional conditions, for example, when the pitch mechanism fails, or certain power train rpms have been exceeded, or a very rapid stop is needed, the Controller also uses the hydraulic brake.

In the chosen design the "*idle*" position is with the shoe pressed against the brake disc by the cylinder spring. This follows the 'Fail/Safe' operating principle (if something goes wrong, the mechanism remains in a *safe* position), in this case the safe position is power train stop.

When the wind turbine is in production, the shoe is away from the disc, so it does not interfere with the power train movement. For this to occur it is necessary to counteract the spring pressure in the cylinder that forces the shoe. This is achieved by increasing the hydraulic pressure applied to the spring base. The increase of this pressure is achieved: by putting the valve in the 'closed' position and the pump running.

![](<lib/Zapata-separada-bomba-valvula-cerrada.jpg>)

When braking is desired (shoe against the disc) it is enough to reduce the hydraulic pressure at the spring base. This is achieved by opening the valve. There is usually more than one valve, with different flow rates, so that the pressure drop speed, and therefore the braking, can be graded (up to a certain point).

Finally, in the design of this circuit, a minimum of elements are used: a pump, a liquid reservoir, the valve(s), the pressure switch (not indicated) and the shoe separation sensor (not indicated).

The brake shoe *state* is not measured by any sensor, but is *deduced* by the Controller during the start-up (*cutin*) phase. The procedure consists of applying an important mechanical torque to the power train, while keeping the hydraulic brake active (shoe against the disc). This mechanical torque is achieved by yawing the nacelle to the wind and setting a pitch value that guarantees the maximum wind exploitation with low rotation values (that is, with *TSR* practically 0). In those circumstances the power train rotation speed is monitored: if it is not 0 (stopped) it is due to some problem related to the shoe, or the cylinder spring; in these circumstances the cutin operation is aborted.

The pump is used to maintain the pressure at the spring base at a value that guarantees that, in production, the shoe does not rub the brake disc. For this, this pressure is not measured, but a more robust device is used, a pressure switch, calibrated around the desired pressure. In this way the Controller only receives a digital signal (the pressure switch output) and has to control two also digital signals: the pump control and the valve(s) control. There is also a limit switch that is activated when the shoe is already separated from the brake disc. This signal corresponds to the signal associated with the 'Brake released' button. The pressure value at which, typically, this signal is activated corresponds to the **'yellow'** <mark>**mark**</mark> in the hydraulic circuit pressure circular indicator.

The evolution of the signals related to this hydraulic circuit can be observed using one of the "Predefined recorder Panels" (pressing in the execution control synoptic: *'Synoptics'* --> *'Recorders'* a recorder form is presented, and in *'Defined panels'* select *'Hydraulic brake circuit'*). You can observe the variation of various hydraulic circuit signals during different operating and stop situations.

The basic control concepts are based on the pressure switch hysteresis, whose output is used by the Controller to start the pump when its value is 'Off', that is, the pressure is below the pressure switch lower calibration limit. And stop the pump when the pressure exceeds the pressure switch upper limit. The valves are assumed to be closed. The following figure exemplifies this control method.

![](<lib/CicloControlBombaconHisteresis.png>)
