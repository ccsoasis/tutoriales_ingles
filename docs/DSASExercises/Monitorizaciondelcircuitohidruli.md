---
tags:
- nacelle internal
- ambient temp
- rotor temp
- multipl temp
- generator temp
- Controller.TempMaxGenerator
- Controller.TempMaxGearBox
- Controller.TempMaxAmbient
- Controller.TempMaxRotorBearing
---

# Observation of the temperature detectors

!!! tip "🎯 Hydraulic circuit monitoring"
    ***Objective:*** Learn to monitor the hydraulic circuit using pressure and state variables to detect deviations.
    ***What to observe:*** System pressures, pump and valve state, as well as possible alarms.
    ***What to note:*** Normal operating values and which variable changes first against an anomaly.
    💡 identify the element that first deviates when an alarm appears.

!!! warning "❓ Guiding questions"
    1. When a stop process is started while in production, is the hydraulic brake used?
    2. What criterion does the controller use to detect a problem in the hydraulic system and which variables does it monitor?

In this practice the objective is to observe the Controller reaction when the temperature sensors of several key components exceed the normal operation limits.

Make sure the wind turbine is in production (see [Set the conditions for the Production entry with low wind to occur](CutinVientoBajo.md)).

Visualize the "SynopticDriveTrain" synoptic (see [How to present a certain synoptic in the foreground](../DSASTutorial/SinpticodelTerminaldeControl.md))

Change the View (first menu option) to "*Nacelle internal*". Put the "Instrumentation view" at "Hidden" (second menu option), and press the third option "Temperatures" so that the temperature indicators are visualized. See the following figure.

![](<lib/DriveTrain-con-gondola-temperaturas.jpg>)

The "**Ambient Temp**", "**Rotor Temp**", "**Multipl Temp**." and "**Generator Temp**" indicators have the red border, which means they are in *'command'* mode. You can modify their value in several ways:

- Moving the bar with the mouse.

- With the "Page Up", "Page Down", "Up arrow" and "Down arrow" keys.

- Typing directly the desired value. If you change the value and the displayed one does not coincide with the previous one, the background turns yellow: you must press "Enter".

The Controller continuously monitors the values in these indicators, comparing them with the "*Controller.TempMaxGenerator*", "*Controller.TempMaxGearBox*", "*Controller.TempMaxAmbient*" and "*Controller.TempMaxRotorBearing*" parameter values.

In this practice you must increase the value in each one of these indicators and observe that, when the temperature exceeds the corresponding parameter value, and during a certain time, the Controller starts a grid disconnection and wind turbine stop process, generating a specific incident.

If you decrease the temperature below the limit once the incident has occurred, you will see that the "Recovered" column of the "Open incidents" table notes the instant that occurs.

Note that the "Ambient Temp" treatment is different from the others: when the maximum allowed ambient temperature is exceeded the corresponding incident is generated, with the wind turbine stop: however, as soon as this temperature drops below its maximum limit, the incident passes automatically to the "Incident history". In the other cases, the operator must "acknowledge" the incident ("Ok" box) before it passes to the "Incident history".
