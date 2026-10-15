# Practical classes

!!! info "👋 Welcome to the RRC Wind Turbine Virtual Laboratory"
    This laboratory notebook will guide you in the study of the **Rotor Resistance control (RRC) wind turbine**: a squirrel-cage generator with dynamic rotor resistance control through an IGBT and PWM signal.
    You must know the description of this wind turbine type (see [RRC Tutorial](../RRCTutorial/Introduccion.md)) and of the execution environment (see [LdP Help](../LdP_Help/Introduccion.md)).
    With this simulator the DSASWT practices related to yawing, cable unwinding, phase fault, strong winds, moment of inertia and hydraulic circuit can also be carried out.

!!! tip "🎯 Global module objectives"
    - Understand the rotor resistance control mechanism and its effect on the slip and the power.
    - Interpret the "Power vs Slip" synoptic and the operating point on the A-D-C-E sections.
    - Observe how the IGBT DutyCycle (PWM signal) controls the rotor effective resistance.
    - Analyze the wind turbine response against wind gusts with different starting conditions.
    - Understand the Pitch mechanism (slew rate) influence on the system stability.

!!! warning "⚠️ What you should know before starting"
    - Basic principles of the squirrel-cage induction generator and the slip concept.
    - Notions of power electronics: IGBT, PWM and resistance control.
    - Wind energy concepts: wind power, Pitch and operating curves.
    - Basic operation of the LdP environment, the synoptics and the "General" recorder.

!!! info "📚 Competencies you will develop"
    - Interpretation of the "Power vs Slip" synoptic and the A, B, C, D, E operating points.
    - Analysis of the DutyCycle (PWM) as an indicator of the active resistance level in the rotor.
    - Understanding of the differential behavior with low wind (squirrel cage mode) and high wind (active control).
    - Evaluation of the Pitch slew rate influence on the stability against gusts.
    - Diagnosis of the operating point and the power dissipated in the rotor circuit.

!!! example "📝 Recommended work methodology"
    1. **Read the objective** of the practice and identify the main variable (DutyCycle, slip, power, Pitch).
    2. **Note the initial state**: operating point position in "Power vs Slip" and PWM value.
    3. **Cause a single change** each time and record the response in the "General" recorder.
    4. **Look for evidence**: operating point position, PWM value, RPMs and power.
    5. **Conclude**: explain the cause-effect with 2–3 measurable evidences.

!!! tip "✅ Observation checklist"
    - **Operating point:** in which section of the "Power vs Slip" curve is it? A, B, C, D or E?
    - **DutyCycle (PWM):** is it 100% (minimum resistance = squirrel cage) or lower?
    - **Dissipated power (RCCPower):** is it appreciable? Is it proportional to the slip?
    - **Pitch:** does it act? Does it follow the value ordered by the Controller?
    - **RPMs:** do they vary? Does the resistance control stabilize them?

!!! info "📋 How to document your conclusion"
    Use this short format (4 lines):

    - **Situation:** what you were observing.
    - **Event:** what changed (and when).
    - **Evidences:** 2–3 measurable data (PWM, power, RPMs, operating point).
    - **Conclusion:** cause-effect explanation (one clear sentence).

!!! warning "⚠️ Typical errors (to avoid them)"
    - Confusing the 100% DutyCycle with "maximum resistance": it is the opposite (100% = minimum resistance = IGBT always in conduction).
    - Changing several parameters at once without being able to identify the cause of the observed change.
    - Ignoring the "Power vs Slip" synoptic when analyzing the system behavior.
    - Not waiting for the system to stabilize before recording the operating point.
    - Concluding only with an impression, without measurable evidences (PWM, power, RPMs).

These practical classes are designed to show the behavior differences of the rotor resistance control wind turbine from the squirrel-cage wind turbine, whose simulator is the one corresponding to the Two-Speed and Active Stall wind turbine (*DSASWT*).

In particular the objective is to observe the key variable evolutions in normal situations and with **wind gusts**, with different starting conditions.

With this simulator the same practices described in the DSASWT Simulator Tutorial can be carried out, related to:

- Effects of the wind direction change.

    - Manual yawing.

    - Automatic yawing.

    - Power cable unwinding.

- Detailed analysis of the grid connection phases.

- Observation of the reaction to a fault in one of the grid phases.

- Behavior against very strong winds.

- Power Train moment of inertia influence.

- Brake hydraulic circuit monitoring.

    - Normal operation observation.

    - Observation of an excessive circuit pressure loss.

    - Observation of the effect of a pump with incorrect operation.

    - Observation of the effect of a discharge valve that does not work.

- Temperature detector observation.
