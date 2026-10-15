---
tags:
- recorders
- StripRecorders
---

# Practical classes

!!! info "👋 Welcome to the DFIG Wind Turbine Virtual Laboratory"
    This laboratory notebook will guide you in studying the **behavior** of wind turbines with **Doubly-Fed Induction Generator (DFIG)** and **Back-to-Back (B2B)** converters.
    You must know the description of this type of wind turbine (see [DFIG Tutorial](../DFIGTutorial/Introduccion.md)) and of the execution environment (see [LdP Help](../LdP_Help/Introduccion.md)).

!!! tip "🎯 Global module objectives"
    - Understand the operation of a DFIG and its control through Back-to-Back converters.
    - Interpret the operational curve of the wind turbine and the MPPT algorithm.
    - Relate the electrical variables of the generator (fluxes, currents, powers) to the wind and the RPMs.
    - Identify the system behavior against wind gusts, stops, and voltage drops.
    - Understand the DFIG's capacity to control reactive power.

!!! Warning: "⚠️ What you should know before starting"
    - Basic principles of induction electrical machines.
    - Wind energy concepts: wind power, Cp, TSR, and the MPPT algorithm.
    - Notions of power electronics: AC/DC and DC/AC converters.
    - Basic operation of the LdP environment and the simulator synoptics.

!!! info "📚 Competencies you will develop"
    - Functional interpretation of the operational curve (MPPT, points C and D).
    - Analysis of magnetic fluxes in the generator (sub and supersynchronous mode).
    - Diagnosis of the B2B behavior (RSC and GSC) in different conditions.
    - Understanding of the influence of the moment of inertia and the air density.
    - Evaluation of the system response against grid faults and wind gusts.

!!! example "📝 Recommended work methodology"
    1. **Read the objective** of the practice and identify the main variable or phenomenon to observe.
    2. **Note the initial state**: reference values before causing changes.
    3. **Cause a single change** each time and record the system response.
    4. **Look for evidence**: states, alarms, transitions, trends in the recorder.
    5. **Conclude**: explain the cause-effect with 2–3 measurable evidences.

!!! tip "✅ Observation checklist"
    - **Operational curve:** at what point is the system? On MPPT, point C or point D?
    - **RPMs:** subsynchronous or supersynchronous? How does it affect the rotor flux?
    - **Powers:** active and reactive in stator, rotor and GSC.
    - **Pitch:** does it change? When and why?
    - **Final state:** does the system stabilize? Does it require reset?

!!! info "📋 How to document your conclusion"
    Use this short format (4 lines):
    - **Situation:** what you were observing.
    - **Event:** what changed (and when).
    - **Evidences:** 2–3 measurable data (variables/states/alarm).
    - **Conclusion:** cause-effect explanation (one clear sentence).

!!! warning "⚠️ Typical errors (to avoid them)"
    - Changing several parameters at once and not being able to identify the cause.
    - Concluding only with an impression, without measurable evidences.
    - Confusing subsynchronous mode with supersynchronous when interpreting the sign of the rotor power.
    - Ignoring the initial system state before launching an operation.
    - Not waiting for the system to stabilize before causing the next change.

## Introduction

This section describes a set of experiments that will help you understand the complex behavior of this type of wind turbine.

Other experiments allow you to observe the evolution of certain signals under fault conditions.

## Prerequisites

To carry out the experiments described in this section, it is essential to become familiar with the description of the components of this Simulator (see [Description of the DFIG Wind Turbine Simulator](../DFIGTutorial/DescripcindelSimuladordelAerogen.md)) and of the common functionalities of the LdP framework ([LdP Tutorial](../LdP_Help/Introduccion.md)).

It is also convenient to know the description of the different [Predefined panels](../DFIGTutorial/PanelespredefinidosparalosRegist.md) for this simulator.

You also need to know the *StripRecorders* (*Recorders*) defined in this Simulator. To do so, go to the execution control form ("*Executing ..*")

![](<lib/Formulario control ejecucion.jpg>)

and press the "*Synoptics*" menu option, and you will get the list of synoptics presented in the following figure:

![](<lib/Listado registradores.jpg>)

Click "StripRecorders" to see a form labeled "Registradores_X".

![](<lib/Registradores_X.jpg>)

Clicking "Predefined panels" shows a list of predefined configurations for this simulator.

![](<lib/Listado paneles espanol.png>)

Choose the first one, "*Cutin + Cutout + Production: Panel to monitor cutin and cutout operations*" and you will see that this form changes to the one shown in the following figure:

![](<lib/SR pitch potencias frenos rpms viento 0.png>)

The first recorder shows the evolution of the two signals related to the blade attack angle (pitch): the command value (Controller.Control.PitchOut, in red) and the real value (Nacelle.DriveTrain.PitchNacelleOut, in green). The differences may be due to the pitch mechanism's actuation in the nacelle (characterized by the maximum response speed: see Parameters-> Analog -> NacellePitch:BladeSlewRate) and its state; it may be stuck or disconnected.

The second recorder shows the electrical power sent to the grid (Nacelle.DFIGB2B.GridActivePower in green) and the mechanical power extracted from the wind (Nacelle.DriveTrain.ActualWindPowerOut in black).

The third shows the evolution of the hydraulic brake release mechanism.

The fourth shows the evolution of the Generator shaft rotation speed.

The fifth shows the evolution of the real wind (SynopticWindNacelle.WindSpeedOut in black) and the effective wind, accounting for possible nacelle misorientation (*Controller.Control.EffectiveWind* in blue).
