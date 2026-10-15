---
tags:
- cut-in
- start-up
- wind turbines
- DSAS
- RRC
- DFIG
- comparison
---

# Comparison of the start-up (cut-in) in different wind turbine families

!!! tip "🎯 Learning objectives"
    When completing this experiment you will be able to:

    - Understand the start-up (cut-in) process in a wind turbine
    - Identify the differences in the start-up behavior between the three main wind turbine families
    - Analyze the key variable evolution during the transition from stopped to production
    - Create and analyze comparative graphs of the start-up time as a function of the wind speed

### What is the cut-in or start-up?

!!! info "📖 Concept: Cut-in (Start-up)"

    The **cut-in** is the process through which a wind turbine carries out the transition from a **stopped** state (power train stopped and generator disconnected from the grid) toward the **production** state (generating electricity and feeding the electrical grid).

    This process involves multiple wind turbine subsystems and varies significantly according to the technology used.

### Importance of the comparative study

Each wind turbine family uses different strategies and technologies to carry out the start-up. Understanding these differences will allow you to:

- Evaluate the advantages and limitations of each technology
- Understand the impact on energy production
- Analyze the maintenance and wear requirements
- Optimize the wind turbine selection according to the site conditions

### Experiment methodology

!!! warning "🔬 Experimental objective"
    Create a data table for each wind turbine type that relates the **wind speed** with the **time needed to complete the start-up**.

#### 📊 Data table structure

For each wind turbine you will create a table with two columns:

- **Wind speed (m/s):** From 6 m/s to 17 m/s in 1 m/s increments
- **Start-up time (s):** Time measured from the start to stable production

!!! info "🛠️ Measurement tool: StripRecorders"
    You will use the StripRecorders (graphic recorders) functionality of the simulators to:

    - Visualize the temporal evolution of the variables
    - Measure time distances between events
    - Create active copies of the measurements

    📚 Consult the "[Active StripRecorder hardcopies](../LdP_Help/DefinicindeRegistradores.md)" tutorial to learn how to use this tool.

### Experimental procedure

!!! example "📝 Experiment 1: DSAS wind turbine"
    ##### Type: Squirrel-cage generator directly connected to the grid with active aerodynamic stall control.

    **Preparation:**

    1. Carry out the Practical Class: "[Set the conditions for the Production entry with low wind to occur](../DSASExercises/CutinVientoBajo.md)"
    2. Become familiar with the DSAS simulator controls
    3. Identify the key variables to monitor

    **Execution:**

    1. Start the DSAS simulator with 6 m/s wind speed
    2. Activate the StripRecorders for the main variables:

        - Rotor rotation speed (rpm)
        - Generated power (kW)
        - Generator state (connected/disconnected)

    3. Start the start-up process
    4. Observe and record the time from the start until stable production is reached
    5. Repeat the experiment increasing the wind speed in 1 m/s steps up to 17 m/s
    6. Record all the times in your data table

!!! example "📝 Experiment 2: RRC wind turbine"
    ##### Type: Induction generator and power train with wound rotor resistance control and blade pitch angle

    **Preparation:**

    1. Open the RRC simulator
    2. Carry out the Practical Class "[Grid connection sequence with wind below the nominal](../RRCExercises/SecuenciadeconexinalaRedcutincon.md)"

    **Execution:**

    1. Repeat the same procedure as in experiment 1
    2. Pay special attention:

        - To the rotor resistance control behavior
        - To the pitch system movement
        - To the rotation speed evolution

    3. Complete your data table for the RRC.

!!! example "📝 Experiment 3: DFIG wind turbine"
    ##### Type: Doubly fed induction generator and power train with pitch angle control

    **Preparation:**

    1. Open the DFIG simulator (50Hz) or DFIG (60Hz) according to your region
    2. Carry out the Practical Class "['Wind Turbine start-up (cutin) with wind below the nominal'](../DFIGExercises/Clasesprcticas.md)"

    **Execution:**

    1. Repeat the procedure of the previous experiments
    2. Observe especially:

        - The back-to-back converters behavior
        - The variable speed control strategy
        - The operating speed range

    3. Complete your data table for the DFIG

### Results analysis

!!! tip "📊 Analysis activities"

    1. **Create comparative graphs:**

        - Represent in the same graph the three "Start-up time vs Wind speed" curves
        - Use different colors for each technology

    2. **Analyze trends:**

        - How does the start-up time vary with the wind speed?
        - Which technology starts up more quickly?
        - Are there critical speeds where the behavior changes?

    3. **Compare technologies:**

        - Which wind turbine has the smoothest start-up?
        - Which one generates greater mechanical stresses during the start-up?
        - What impact does this have on maintenance?

    4. **Reflect on applications:**

        - In a site with variable winds, which technology would be more efficient?
        - How does the start-up time affect the annual energy production?

!!! warning "⚡ Key points for your report"
    When finishing the experiment, make sure you can answer:

    - What are the main differences in the start-up process of each technology?
    - What advantages and disadvantages does each start-up method present?
    - How do the control systems (pitch, rotor resistance, converters) influence the start-up?
    - What relationship exists between the technological complexity and the start-up performance?

### Complementary resources

!!! info "📚 To delve deeper"
    It is recommended to consult the following tutorials to understand each technology in detail:

    - **DSAS:** Foundations of the aerodynamic stall control
    - **RRC:** Wound rotor resistance control
    - **DFIG:** Doubly fed generators and back-to-back converters
