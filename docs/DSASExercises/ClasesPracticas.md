# Practical classes

!!! info "👋 Welcome to the ACMSL Wind Turbine Virtual Laboratory"
    With the practices suggested in this document, you will become familiar with the **behavior** of the subsystems and common elements of the wind turbines called **Horizontal Axis**, and also with the specific particularities of the family known as **with Squirrel Cage Generator and Control by Aerodynamic Stall Entry**.
    You must know the description of this family (see [Tutorial](../DSASTutorial/Introduccion.md)) and of the Real Time Simulator execution environment (see [LdP](../LdP_Help/Introduccion.md)).

!!! tip "🎯 Global module objectives"
    - Understand the general operation of a horizontal axis wind turbine.
    - Correctly interpret system states, alarms and transitions.
    - Relate physical variables (wind, speed, power) with the control behavior.
    - Identify protection strategies against anomalous conditions.

!!! warning "⚠️ What you should know before starting"
    - Basic concepts of wind energy and aerodynamics.
    - Elementary notions of three-phase electrical systems.
    - Basic principles of control and state machines.

!!! info "📚 Competencies you will develop"
    - Technical analysis capacity based on evidence.
    - Preliminary fault diagnosis in subsystems.
    - Functional interpretation of state machines.
    - Understanding of the wind turbine dynamic behavior.

!!! example "📝 Recommended work methodology"
    1. **Read the objective** of the practice and locate the main variable (wind, speed, power, pressure, states).
    2. **Observe at rest**: note the initial state and reference values (before causing changes).
    3. **Cause a single change** (one at a time) and record what happens.
    4. **Look for evidence**: states, alarms, transitions, trends and times.
    5. **Conclude**: explain the cause-effect with 2–3 evidences (not only with opinions).

!!! tip "✅ Observation checklist"
    - **States:** in which state is the system? does it change? why?
    - **Alarms:** does any appear? which was the first?
    - **Key variables:** wind, speed, power, direction, pressure (according to the practice).
    - **Transitions:** change instant and the condition that triggers it (threshold, permission, time).
    - **Final state:** does it remain stable? does it remain blocked? does it require reset?

!!! info "📋 How to document your conclusion"
    Use this short format (4 lines):
    - **Situation:** what you were observing.
    - **Event:** what changed (and when).
    - **Evidences:** 2–3 measurable data (variables/states/alarm).
    - **Conclusion:** cause-effect explanation (one clear sentence).

!!! warning "⚠️ Typical errors (to avoid them)"
    - Changing several parameters at once and not being able to identify the cause.
    - Concluding only with an impression, without evidence (variables/states).
    - Confusing **limitation** with **stop** in high wind scenarios.
    - Ignoring the **initial state** (without reference, there is no comparison).

In the following chapters a set of exercises is presented that will allow you to know the wind turbine behavior in different situations.

The list of these practical classes is not exhaustive, since it is possible to develop others where real problems in the wind turbine are proposed that the student solves. Generally these cases imply the development of 'configurations' different from the one used in this simulator, although these differences do not refer to the central core of the configuration, but to sets of parameters, connections between signals, etc. You must consult ACM SL for development guides of these configurations.
