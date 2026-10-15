---
tags:
- pitch
- algorithms
- Controller.Control.PitchOut
- Nacelle.DriveTrain.PitchIn
- Nacelle.DriveTrain.PitchNacelleOut
- Controller.Control.PitchNacelleIn
- pitch angle
- feathered
---

# Blade Pitch angle control algorithm

The blade pitch angle can be common (the three with the same angle) or they can have different values. Its control is done through hydraulic cylinders or electric motors.

In the case of the wind turbine emulated in this simulator, **the pitch of the three blades is common** and is modified through hydraulic cylinders.

The Controller emits a signal (*Controller.Control.****PitchOut***) that reaches the control input terminal of the servo-control circuit that exists in the nacelle that governs the hydraulic cylinders (*Nacelle.DriveTrain.****PitchIn***).

The control algorithm used by the Controller takes into account the real value at each moment of the pitch angle (*Nacelle.DriveTrain.****PitchNacelleOut***) through its input (*Controller.Control.PitchNacelleIn*), to implement a feedback control loop. This algorithm takes into account other factors, such as the wind speed, to set the pitch angle value at all times.

The concepts taken into account derive from what is explained in [Concepts about the extractable wind power](Porqugiranlaspalas.md).

The pitch value goes to -90º ("feathered" position) when it is disconnected from the grid and without production, so that the mechanical stresses on blades, nacelle and Tower are minimized.
