---
tags:
- gusts
- wind gusts
- pitch
- turbulence
- moment of inertia
- flicker
- DSAS
- RRC
- DFIG
---

# Response to wind gusts

!!! tip "🎯 Learning objectives"
    When completing this experiment you will be able to:

    - Understand the nature of wind gusts and their modeling
    - Identify the challenges that gusts represent for the wind turbine operation
    - Analyze the different response strategies according to the wind turbine technology
    - Evaluate the role of the rotor moment of inertia as energy storage

### Introduction: The wind as a complex phenomenon

!!! info "🌪️ Real wind characteristics"
    The wind is a complex atmospheric phenomenon that is difficult to model with precision. In practice, for the wind turbine design and analysis, three fundamental parameters are considered:

    - **Direction:** Where the wind blows (e.g., North, Southwest, etc.)
    - **Mean speed:** The speed averaged over a time period (typically 10 minutes)
    - **Turbulence:** The rapid and irregular speed and direction variations superimposed on the mean speed
  
    From the perspective of the wind turbine structural and operational sizing, these characteristics are simplified into two main categories:

    - Mean wind: Relatively stable conditions
    - Wind gusts: Abrupt and significant speed changes

### Characterization of wind gusts

Wind gusts are characterized by several parameters:

!!! info "📊 Gust parameters"
    - **Maximum speed:** The speed peak reached during the gust
    - **Minimum speed:** The speed valley (can be lower than the previous mean speed)
    - **Amplitude:** The difference between maximum and minimum speed
    - **Maximum rate of change:** How quickly the wind speed changes (m/s²)
    - **Duration:** The time the gust lasts

#### Standard gust model for comparisons

To compare the behavior of different wind turbines, a standardized gust model is used that allows carrying out reproducible tests:

![Wind gust model for DFIG](<lib/DFIG WindGust Def 120x4.jpg>)

Figure 1: Typical wind gust model used for comparative tests

This model represents an idealized ramp-shaped gust, characterized by:

- An initial stable speed

- A linear speed increase (ascending ramp)

- A sustained maximum speed period

- A linear speed decrease (descending ramp)

- Return to stable conditions

### The challenge of gusts

!!! warning "⚠️ Problems associated with gusts"
    Wind gusts pose two main problems that the wind turbine must solve:
    ##### 1. Power train (Drive Train) stability
    - Abrupt wind speed changes generate **dynamic loads** on the whole mechanical system
    - They can cause **torsional oscillations** in the main shaft
    - They accelerate the **component wear** (bearings, gears)
    - In extreme cases, they can cause **structural damage**
    ##### 2. Quality of the power delivered to the grid
    - The rotor speed variations translate into **power fluctuations**
    - These fluctuations can cause **voltage variations** in the electrical grid
    - "Flicker" problem: perceptible variations in the luminous intensity of the lamps connected to the grid
    - Impact on the **electrical service quality** for other consumers

### General response strategies

!!! info "🛠️ Compensation mechanisms"
    In general, the compensation of wind speed changes is carried out through the adjustment of the blade pitch angle. However, when it comes to gusts:
    !!! warning
    **Fundamental limitation:** The pitch mechanism may **not be fast enough** to compensate the abrupt speed changes characteristic of gusts.
    For this reason, different wind turbine families have developed **additional mechanisms** to manage gusts, especially focused on:

    - Maintaining the power train stability
    - Guaranteeing the quality of the power delivered to the grid

### Response according to the wind turbine family

The following describes how each technology addresses the gust problem:

!!! info "⚙️ First generation wind turbines: Fixed pitch and aerodynamic stall"
*Technology*: Squirrel-cage generator + Fixed Pitch + Passive Stall
    ##### Characteristics:
    - Blades with **fixed** pitch angle (not adjustable)
    - **Squirrel-cage** generator directly connected to the grid
    - Passive control by **aerodynamic stall**
    ##### Gust response mechanism
    The power train stability is achieved through the **blade aerodynamic design**:

    - When the wind speed exceeds the nominal speed, the blades enter **aerodynamic stall**
    - In stall, the air flow detaches from the blade surface
    - This causes an **automatic reduction** of the power captured from the wind
    - Acts as a "natural limiter" of power
  
    📚 See the characteristic curve in: ['Power vs Wind graph in fixed-blade-angle wind turbines'](../DSASTutorial/Productioncurve.md)
    ##### Rotation speed control:
    The power train rpm are controlled by the **squirrel-cage generator** characteristics directly connected to the grid:
    - The rotation speed is kept very close to the generator **synchronous speed**
    - Typical variation: no more than 1% of the synchronous speed
  
    📚 More information: [Introduction to induction machines](../DSASTutorial/IntoductiontotheInductionMachine.md) and 
                [Generator characteristics](../DSASTutorial/DatosTecnicosGenerador.md)
    !!! warning "⚠️ Limitations of this technology"
    - **Variable delivered power:** Above nominal speed, the power **decreases** instead of remaining constant
    - **Tower loads:** The stall phenomenon increases the **horizontal forces** that the tower must withstand
    - **Reduced efficiency:** In high wind conditions, all the energy potential is not used

!!! info "⚙️ Wind turbines with active pitch control"
    *Technology*: Squirrel-cage generator + Active variable Pitch
    ##### Characteristics:
    - Blades with **variable and actively controlled** pitch angle
    - **Squirrel-cage** generator directly connected to the grid
    - Hydraulic or electrical system to adjust the pitch
    ##### Gust response mechanism
    Above the nominal wind speed:

    - The control system **adjusts the blade pitch angle**
    - The blades orient progressively **"to the feathers" (feathering)**
    - This allows the **wind excess to pass through** without being captured
    - Maintains the **power constant** at the nominal value
  
    📚 See the characteristic curve in: ['Power as a function of the Wind in a variable pitch and fixed speed wind turbine'](../DSASTutorial/Productioncurve.md)
    ##### Rotation speed control
    Similar to the previous generation:

    - Squirrel-cage generator directly connected to the grid
    - Rotation speed kept very close to the synchronous speed
    !!! info "✅ Advantages over the previous generation"

    - **Constant power:** Maintains nominal power above nominal wind speed
    - **Lower tower loads:** The feathering reduces horizontal forces compared to stall
    - **Greater efficiency:** Better wind use in the whole operating range
    - **Stop control:** Can stop the rotor in a controlled way by turning the blades 90°

!!! info "⚙️ Wind turbines with rotor resistance control"
    *Technology*: RRC (Rotor Resistance Control) - Wound rotor generator + Variable Pitch
    ##### Characteristics

    - Blades with variable pitch to the feathers (feathering)
    - **Wound rotor generator** (not squirrel cage)
    - Electronic device that allows inserting **variable resistance** in the rotor circuit
    - High rotor and power train moment of inertia
    ##### Gust response mechanism

    This technology introduces an innovative concept: **using the power train as energy storage**:

    1. **During an ascending gust**

        - The pitch system cannot respond fast enough
        - **More power** is captured from the wind than can be delivered to the grid
        - The energy excess is used to **accelerate the rotor**
        - The rotor acts as a **flywheel** storing kinetic energy
        - This requires the generator to be able to operate at **variable speeds**

    2. **During a descending gust**

        - The wind contributes less energy than needed
        - The rotor **decelerates**, releasing stored kinetic energy
        - This helps to **keep the delivered power** more constant

    !!! warning "🔑 Key concept: The power train as a flywheel"

        The power train moment of inertia is high enough for it to act as a **short-term energy storage**.

        The kinetic energy stored in a rotating rotor is:
        E = ½ × I × ω²

        Where:

        - E = Kinetic energy (J)
        - I = Power train moment of inertia (kg·m²)
        - ω = Angular speed (rad/s)

        A change in ω allows absorbing or releasing energy without abrupt changes in the delivered power.

    ##### Technological solution: Wound rotor generator
    For the rotor to be able to change its rotation speed maintaining the grid connection:

    - A **wound rotor generator** is used
    - A squirrel-cage generator cannot be used (almost fixed speed)
    - An **electronic device** is incorporated that allows inserting variable resistance in the rotor circuit
    - This allows controlling the generator **slip**
  
    #####📚 Detailed explanation: ['Basic concepts in rotor resistance controlled wind turbines (Rotor Resistance Controlled Wind Turbines)'](../RRCTutorial/RazonesparaeldesarrollodelosAero.md)
  
    ##### Practical experiments
    To explore the behavior of these wind turbines against gusts:

    - ['Wind gusts during a low wind regime in an RRC'](../RRCTutorial/Rfagasdeviento.md) 
    - ['Wind gusts during a high wind regime in an RRC'](../RRCTutorial/Rfagasdeviento.md)

!!! info "⚙️ Wind turbines with doubly fed generator (DFIG)"
    Technology: DFIG (Doubly Fed Induction Generator) - Variable Pitch + Variable Speed
    ##### Characteristics:
    - Blades with variable pitch to the feathers
    - **Doubly fed induction generator (DFIG)**
    - **Back-to-Back electronic power converters** in the rotor circuit
    - Very wide operating speed range (typically 2 to 1)
    - Sophisticated control system
    ##### Gust response mechanism:
    Similar to RRC, it uses the **rotor acceleration and deceleration** to absorb/release energy and compensate the differences between the power captured from the wind and the power delivered to the grid.
    !!! info "✅ Advantages over RRC:"
    - **Much wider operating range:** Can operate efficiently in a much higher wind speed range
    - **More sophisticated control:** The electronic converters allow precise and fast control
    - **Greater efficiency:** Optimizes the rotation speed for each wind speed
    - **Better power quality:** Independent active and reactive power control
    📚 See detailed behavior: [DFIG WT Behavior](../DFIGTutorial/Implicacionesdelcomportamientode.md)
    📚 About the converters: [Back-to-Back converters](../DFIGTutorial/ConvertidoresBackToBack.md)
    ##### Practical experiments:
    To explore the DFIG behavior against gusts:

    - ['Wind gusts during a low wind regime in a DFIG'](../DFIGTutorial/RfagasdevientoWindgusts.md)
    - ['Wind gusts during a high wind regime in a DFIG'](../DFIGTutorial/RfagasdevientoWindgusts.md) 

### Comparative strategy table

!!! info "📊 Gust response comparison"

| Technology                       | Power Control                        | Speed Control                   | Gust Response                                               |
| ----------------------------------| --------------------------------------| ----------------------------------| -------------------------------------------------------------|
| **Fixed Pitch + Stall**          | Passive aerodynamic stall            | Fixed speed (~1% variation)      | Blade aerodynamic design                                    |
| **Variable Pitch + Fixed Speed** | Active pitch control (feathering)    | Fixed speed (~1% variation)      | Pitch adjustment (limited by actuator speed)                |
| **RRC**                          | Pitch + Rotor resistance             | Limitedly variable speed         | Pitch + Rotor inertia as storage                            |
| **DFIG**                         | Pitch + Converters                   | Widely variable speed            | Pitch + Rotor inertia + Sophisticated electronic control    |

### Proposed experimental activities

!!! tip "🔬 Recommended experiments"
    For each wind turbine family, carry out the following tests:

    1. **Configure standard gust**
   
        - Use the gust model shown in Figure 1
        - Adjust the parameters according to each simulator specifications
    2. **Monitor key variables**
        - Wind speed (input)
        - Rotor rotation speed (rpm)
        - Blade pitch angle
        - Generated power
        - Main shaft torque
    3. **Observe and record**
        - Pitch system response time
        - Rotation speed variation
        - Delivered power fluctuations
        - Mechanical torque peaks
    4. **Tests with gusts in different conditions**
        - Gusts with low mean wind (below nominal speed)
        - Gusts with high mean wind (above nominal speed)

### Comparative analysis

!!! tip "📝 Analysis questions"
    1. **On the power train stability:**
        - Which technology shows the smallest rotation speed variations?
        - Which technology presents the smoothest mechanical torque peaks?
        - How does the rotor moment of inertia affect the response?
    2. **On the power quality:**
        - Which technology keeps the power more constant during a gust?
        - In which cases would flicker problems be observed?
        - How does the DFIG power quality improve with respect to the RRC?
    3. **On the control mechanisms:**
        - Is the pitch sufficient to compensate fast gusts?
        - What role does the variable speed play in the response?
        - Why is the pitch + variable speed combination superior?
    4. **On design compromises:**
        - What advantages justify the greater DFIG complexity?
        - In which scenarios would it be acceptable to use simpler technologies?
        - How does the electrical regulation influence the technology choice?

### Key concepts

!!! info "📌 Summary of fundamental concepts"
    - Wind gusts are abrupt speed changes that challenge the wind turbine control
    - The pitch system alone can be insufficient to compensate fast gusts
    - The **rotor moment of inertia** can be used as short-term energy storage
    - The **variable speed** capacity is key to take advantage of the rotor inertia
    - Each technology represents a compromise between **complexity, cost and performance**
    - The technological evolution seeks to improve both the **mechanical stability** and the **power quality**
