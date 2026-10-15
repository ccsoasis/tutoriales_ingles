---
tags:
- yaw
- orientation
- gondola
- nacelle
- wind turbine
- wind
- control
---

# Observation of the nacelle orientation operations

!!! tip "🎯 Learning objectives"
    When completing this experiment you will be able to:

    - Understand the function and importance of the orientation (yaw) system in wind turbines
    - Identify the factors that the control system monitors to decide when to orient the nacelle
    - Know the different methods of measuring the misalignment with respect to the wind
    - Analyze the orientation process and its operational limitations
    - Understand the problem of power cable winding

### Introduction: Why is orientation necessary?

!!! info "📖 Fundamental concept: 'Upwind' orientation"
    In "upwind" wind turbines (with the rotor located in front of the tower, windward), the nacelle must remain oriented **facing the wind** to maximize the wind energy capture.

    If the nacelle is not correctly oriented:

    - The power captured from the wind is reduced
    - The lateral loads on the rotor and the tower increase
    - The mechanical component wear increases
    - The wind turbine global efficiency decreases

### The orientation system (Yaw System)

To keep the nacelle oriented toward the wind, wind turbines incorporate a 
            [yaw subsystem](../DSASTutorial/Yawingsubsystem.md).

!!! info "⚙️ Typical Yaw system components"
    The system normally includes **two sets of motors with gearboxes**, one for each turn direction:

    - **Orientation motors:** Provide the force to turn the nacelle
    - **Gearboxes:** Reduce the speed and increase the driving torque
    - **Toothed crown:** Mounted on the tower top
    - **Attack pinions:** Mesh with the crown to transmit the movement
    - **Orientation brakes:** Keep the nacelle fixed when there is no yaw operation
    - **Measurement systems:** Sensors that determine the orientation and wind direction

### Factors monitored by the orientation process

The wind turbine controller constantly monitors several factors before deciding whether the nacelle must be reoriented. 

#### 1. Nacelle misalignment with respect to the wind direction

!!! info "📐 Misalignment measurement methods"
    This value can be obtained in two different ways:

    ##### Method A: By means of a wind vane (Wind Vane)
    Uses a [wind vane](../DSASTutorial/MedicindeladireccionDireccionVie.md) mounted on the nacelle:

    - The wind vane reference axis must be aligned with the nacelle vertical symmetry plane
    - Measures **directly** the misalignment angle
    - **Advantage:** Direct and simple measurement of the orientation error
    - **Disadvantage:** Can be affected by turbulences created by the rotor itself
    ##### Method B: By means of advanced anemometer + Absolute orientation measurement
    Uses absolute measurements with respect to geographic North:

    - An **advanced anemometer** provides the wind direction (with respect to North)
    - A measurement system provides the **nacelle orientation** (with respect to North)
    - The controller calculates the difference between both measurements
    - **Advantage:** Greater precision, less affected by local turbulences
    - **Disadvantage:** Requires that both the orientation measurement mechanism and the anemometer be correctly **calibrated to North**

!!! warning "⚠️ Importance of the orientation sensor calibration"
    For Method B it is absolutely critical that both the nacelle orientation measurement system and the anemometer be **properly calibrated and oriented to geographic North**.

    Any calibration error will translate into a systematic error in the wind turbine orientation.

#### 2. Current wind speed

The orientation system only operates when the wind speed is within an appropriate range, defined by two limits:

!!! info "🌬️ Wind speed limits for orientation operations"
    - **'Minimum for orientation' (Min for orientation):**
  
        - If the wind is below this value, the system does not execute orientations
            - Reason: With very low winds, the operation would consume more energy than would be gained
            - In addition, with low winds the direction is usually very variable and unstable
    - **'Maximum for start' (Max for cutin):**
        - If the wind exceeds this value, the wind turbine may be in an emergency stop process
            - The orientation operations are suspended for safety reasons
  
    📚 For more details, consult this [wind limits tutorial](../DSASTutorial/DatosTecnicosValoresVientos.md).

#### 3. Number of accumulated turns in the power cables

!!! info "🔌 Cable winding problem"
    The power cables transport the generated electricity from the electrical generator (located in the nacelle, which is rotating) to the grid connection point (located in the tower base, which is fixed).

    As the nacelle turns following the wind direction changes:

    - The cables are **winding over themselves**
    - **Mechanical tension** accumulates in the cables
    - There is risk of **damage due to excessive torsion** if a limit is exceeded
  
    For this reason, the controller keeps a **counter of the number of accumulated turns** (positive in one direction, negative in the other). When a predefined limit is reached, the system must execute an unwinding operation.

    📚 For more information on this process, consult the [nacelle orientation tutorial](../DSASTutorial/Yawingofthenacelle.md).

#### 4. Wind turbine state

The orientation system behavior depends on the wind turbine operating state:

!!! info "🔄 Orientation strategy according to the state"
    - **In Production state:**
  
        - The wind turbine is generating electricity
        - The orientation is a priority to maximize energy capture
        - The misalignment thresholds are usually stricter
    - **In Stopped state:**
        - The wind turbine is not generating
        - The orientation is less critical
        - Greater misalignment can be tolerated
        - It is the ideal moment to carry out cable unwinding operations

### Recommended practical technical session

!!! tip "🎓 Guided experiment"
    To observe in detail the complete orientation process under changing wind conditions, it is strongly recommended to follow the technical session 
    📚 [**"Changing the wind direction"**](../DSASTutorial/Cambiodelavelocidaddelviento.md)

    In this practical session you will be able to:

    - Observe how the system responds to gradual wind direction changes
    - Analyze the controller actuation thresholds
    - Study the behavior during the turn accumulation in the cables
    - Understand the interaction between all the monitored factors
    - Experiment with different parameter configurations

### Important operational considerations

!!! warning "⚡ Key operation aspects"
    - **Orientation speed:** Typically between 0.3 and 0.5 degrees per second (very slow compared to the rotor rotation)
    - **Energy consumption:** The yaw motors consume electrical energy; unnecessary orientations reduce the net production
    - **Mechanical wear:** Each yaw operation generates wear on gears, bearings and components
    - **Design balance:** The controller must optimize between:

        - Maintaining good orientation (maximum energy capture)
        - Minimizing yaw operations (reducing wear and consumption)
        - Avoiding reaching the cable winding limits

### Analysis activities

!!! tip "📝 Proposed exercises"
    1. **Threshold analysis:**
        - Why do you think there is a minimum misalignment threshold before activating the yaw system?
        - What would happen if the system tried to maintain perfect orientation (0° error) constantly?
    2. **Measurement method comparison:**
        - List the advantages and disadvantages of each misalignment measurement method
        - In which situations would each method be preferable?
    3. **Unwinding strategies:**
        - Is it better to unwind the cables during production or during stop?
        - What factors influence this decision?
    4. **Parameter optimization:**
        - If a site has very changing winds in direction, how would you adjust the parameters?
        - If the wind is very stable in direction, what modifications would you make?

### Key concepts to remember

!!! info "📌 Summary"
    - The correct nacelle orientation is essential to maximize energy capture
    - The yaw system is a compromise between energy performance, mechanical wear and consumption
    - Multiple factors (misalignment, wind speed, cable winding, wind turbine state) must be considered before deciding to orient
    - There are two main misalignment measurement methods, each with advantages and disadvantages
    - The cable winding imposes important operational limits that require unwinding operations
    - The correct calibration of the measurement systems is absolutely critical
    - The wind turbine operating state significantly affects the orientation strategy
