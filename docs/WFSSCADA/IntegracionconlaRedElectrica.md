---
tags:
- production setpoint
---

# Delivered Active Power control

There are farms that have wind turbines that allow *controlling the power delivered to the Grid*, independently of the existing wind speed (that is, they have control elements such that the delivered power is lower than the one they could give at that moment). With this wind turbine type, the total power delivered to the Grid can be controlled by making a production distribution among the different wind turbines, for each **production setpoint** change. This is the case of the DFIG type wind turbines and those controlled by Rotor Resistance.

Other wind turbine types, such as the fixed blade speed ones or those that work through "Active Stall" control (blade stall entry), do not have that capacity: in this case the tracking of the power setpoint to deliver to the Grid is carried out by disconnecting some of the wind turbines.

The farm can implement various criteria to adapt to the power setpoint change. In the following figures some are shown:

- By *upper limit*.

![](<lib/LimitacionPotenciaParquePorMaximo.jpg>)

- By *gradient limitation*: the setpoint change is followed, but without abrupt transitions.

![](<lib/LimitacionPotenciaParquePorGradiente.jpg>)

- With *continuous tracking*, but with a reserve margin:

![](<lib/LimitacionPotenciaParqueConReserva.jpg>)

It may also be that the farm is obliged to participate in the Grid frequency maintenance, an important part of its stability: in this case the delivered power control system is more sophisticated and has to obey the Grid parameters, governed by a curve similar to the following:

![](<lib/LimitacionPotenciaParqueConParticipacionEnCon.jpg>)
