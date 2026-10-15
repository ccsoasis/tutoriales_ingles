---
tags:
- soft brake
---

# Observation of the effect of a discharge valve that does not work

!!! tip "🎯 Valve with fault observation"
    ***Objective:*** Identify how a defective valve affects the circuit behavior.
    ***What to observe:*** Pressure changes, actuator response and possible associated alarms.
    ***What to note:*** Which variable stops responding correctly and at which moment the fault is detected.
    💡 observe whether the fault is permanent or intermittent.

!!! warning "❓ Guiding questions"
    1. When a stop process is started while in production, is the hydraulic brake used?
    2. What criterion does the controller use to detect a problem in the hydraulic system and which variables does it monitor?

In this practice the objective is to observe the protocol used by the Controller when a brake circuit valve fault occurs.

In this case we will use one of the characteristic functionalities of the graphic indicators of the LdP framework in which this simulator is developed. We will simulate a manual control directly of one of the brake valves.

![](<lib/SynopticDriveTrain espaol.png>)

To do so we will put the wind turbine in production (see for example the [Set the conditions for the Production entry with low wind to occur](CutinVientoBajo.md) practice).

Next we will 'select' the *'Soft brake'* indicator in the "*SynopticDriveTrain*" synoptic, clicking on it. (Nothing should happen, since this indicator mode, by default, is *'presentation only'*: its border is green).

We press the 'F6' key, so its border will change to red, indicating that now it behaves like a button with which we can control the associated signal, which is the 'Normal brake' valve control.

Now we click with the mouse on this button, so the associated signal will become active and it will be indicated on the button, which will change the background color to yellow. The power train will stop immediately, and the Controller will create an incident with description "*Bypass or Thyristors on and brake not released*". This incident indicates that, during the braking evolution (absolutely unforeseen), there has been a time interval (some milliseconds) in which the Thyristor Bypass Contactors were connected and the brake was activated. A dangerous situation for the electrical elements.
