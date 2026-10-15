---
tags:
- generators
- induction
- DFIG
- squirrel cage
- wound rotor
- wind turbines
---

# Differences in the electrical generators used in wind turbines

!!! tip "🎯 Learning objectives"
    When completing this topic you will be able to:

    - Identify the main types of electrical generators used in wind turbines
    - Understand the fundamental differences between squirrel cage, wound rotor and doubly fed generators
    - Relate the generator type with the wind turbine operational capacities
    - Evaluate the advantages and limitations of each generator technology

### Introduction

The electrical generator is the component that transforms the rotor rotational mechanical energy into electrical energy. The choice of the generator type has a fundamental impact on:

- The wind turbine operating speed range

- The power control capacity

- The generated electricity quality

- The system complexity and cost

- The maintenance requirements

!!! info "📖 Fundamental concept: Induction machines"
    All the generators used in the wind turbine technologies we have studied are induction machines, also known as asynchronous machines.

    These machines are characterized by:

    - Not requiring direct electrical contact between rotor and stator (in the squirrel cage case)
    - Operating with a certain **slip** with respect to the synchronous speed
    - Being robust, reliable and relatively economical
    - Being able to work both as motor or as generator

### Historical evolution and main types

Throughout the wind technology evolution, three induction machine configurations have mainly been used:

!!! info "⚙️ Induction generator types in wind turbines"
    1. **Squirrel cage generator (Squirrel Cage Induction Generator - SCIG)**
        - Direct grid connection
        - Practically fixed speed
        - Simplest and most economical technology
        - Used in first and second generation wind turbines
    2. **Wound rotor generator with resistance control (Wound Rotor with Rotor Resistance Control)**
        - Allows limitedly variable speed
        - Uses variable resistances in the rotor circuit
        - Intermediate technology in complexity and cost
        - Used in RRC wind turbines
    3. **Doubly fed induction generator (Doubly Fed Induction Generator - DFIG)**
        - Allows a wide variable speed range
        - Uses electronic power converters (back-to-back)
        - Most complex and sophisticated technology
        - Used in modern high efficiency wind turbines

### Deepening in each technology

!!! warning "📚 Main study resource"
    For a complete and detailed understanding of the differences between these electrical generator types, as well as their operation, operating principles, and application in wind turbines, consult the specialized tutorial 
    [📖 'Electric Induction Machines'](../DFIGTutorial/Vistasconstructivasdemaquinaselc.md)
    
    This tutorial covers in depth:

    - Fundamental principles of induction machines
    - Constructive differences between squirrel cage and wound rotor
    - DFIG operation and the back-to-back converters
    - Characteristic curves of each generator type
    - Relationship between the generator type and the wind turbine performance
    - Advantages and limitations of each technology

### Key aspects to understand

!!! tip "🎓 Fundamental topics for your study"
    When studying the induction machines tutorial, pay special attention to:
    ##### 1. Basic induction machine concepts:
    - What is the synchronous speed?
    - What is the slip?
    - How is the rotating magnetic field generated?
    - What is the difference between motor and generator operation?
    ##### 2. Squirrel cage generator:
    - Why is it called "squirrel cage"?
    - Why is the speed practically fixed?
    - What advantages does it offer in terms of reliability and cost?
    - What are its main limitations for wind applications?
    ##### 3. Wound rotor generator:
    - How does it differ constructively from the squirrel cage one?
    - How does resistance control allow varying the speed?
    - What role do the slip rings play?
    - What is the achievable speed variation range?
    ##### 4. Doubly fed generator (DFIG):
    - Why is it called "doubly fed"?
    - What function do the back-to-back converters fulfill?
    - How is the wide variable speed range achieved?
    - What advantages does it offer in terms of active and reactive power control?
    - Why can the converters be of lower power than the generator?

### Relationship with the wind turbine performance

!!! info "🔗 Generator - global performance connection"
    The generator type used directly determines the following characteristics

| Wind turbine characteristic         | Generator dependence                                                                                    |
| -------------------------------------| ---------------------------------------------------------------------------------------------------------|
| **Operating speed range**           | SCIG: very limited (~1%) Wound rotor: limited (~10%) DFIG: wide (~30-40%)                               |
| **Partial load efficiency**         | Variable speed (DFIG) allows optimizing the blade tip speed for each wind speed                          |
| **Gust response**                   | Variable speed allows using the rotor inertia as energy storage                                          |
| **Power quality**                   | DFIG offers decoupled active and reactive power control                                                  |
| **System complexity**               | SCIG: minimal Wound rotor: medium DFIG: high                                                             |
| **Cost**                            | SCIG: low Wound rotor: medium DFIG: high (but compensated by higher production)                          |

### Current trends

!!! warning "🔮 Technology evolution"
    Currently, the majority of new wind turbines use DFIG technology or total conversion systems (full converter), which offer:

    - Maximum operational flexibility
    - Optimal efficiency in a wide wind range
    - Excellent power quality
    - Electrical grid support capacity
  
    However, squirrel cage and wound rotor generators remain relevant in:

    - Small and medium wind turbines
    - Applications where simplicity and low cost are priorities
    - Existing wind farms that continue operating

### Suggested study activities

!!! tip "📝 To consolidate the learning"
    1. **Main tutorial reading:**
        - Read carefully the ['Electric Induction Machines'](../DFIGTutorial/Vistasconstructivasdemaquinaselc.md) tutorial
        - Take notes on the key concepts
        - Draw schematics of each generator type
    2. **Comparative analysis:**
        - Create a table comparing the three generator types
        - Include: construction, operating principle, advantages, limitations, applications
    3. **Relationship with previous experiments:**
        - Review the previous experiments on wind turbine comparison
        - Identify how the generator type influences each observed behavior
    4. **Complementary research:**
        - Research synchronous and permanent magnet generators in wind turbines
        - Compare with the studied induction machines

### Conclusion

!!! info "📌 Key points to remember"
    - The electrical generator is a fundamental component that determines many wind turbine operational characteristics
    - There are three main induction machine types used in wind turbines: squirrel cage, wound rotor and doubly fed
    - The technological evolution has gone from fixed speed toward variable speed to improve efficiency and power quality
    - Each technology represents a compromise between complexity, cost and performance
    - The understanding of the generators is essential to understand the wind turbine global operation

!!! warning "📚 Additional resources"
    In addition to the main induction machines tutorial, it is recommended to consult:
    
    - Specific tutorials of each wind turbine family (DSAS, RRC, DFIG)
    - Documentation on power converters and power electronics
    - Real wind turbine case studies
    - Technical regulations on energy quality in wind farms
