---
tags:
- unwinding
- cables
- yaw
- cost
- lost production
- wind turbine
---

# Cost of power cable unwinding

!!! tip "🎯 Learning objectives"
    When completing this experiment you will be able to:

    - Understand why the cable unwinding has a significant economic cost
    - Calculate the total time of a complete unwinding operation
    - Estimate the production losses associated with this process
    - Analyze the cost components: lost production vs motor consumption
    - Evaluate strategies to minimize the economic impact of the unwinding

### Introduction: Why is there a cost?

!!! info "💰 The economic problem of unwinding"
    As we saw in the previous experiment, the power cables wind up progressively as the nacelle turns following the wind direction changes. When the winding limit is reached, the wind turbine must execute an unwinding operation.

    This operation has several cost components:

    - **Grid disconnection (cut-out):** During this phase no electricity is generated
    - **Unwinding turn:** The nacelle may have to turn several complete turns, a process that takes time
    - **Grid reconnection (cut-in):** Requires additional time until reaching stable production
    - **Yaw motor consumption:** These motors consume energy during this process
  
    The **objective of this experiment** is to quantify these costs in economic terms.

### Problem statement

!!! warning "📋 Analysis scenario"
    We will consider the following realistic scenario:

    ##### Initial conditions:

    - The wind turbine is in **Production** (generating electricity)
    - The power cables have reached the **winding limit** in one direction
    - Configured limit: **2.5 complete turns** (900 degrees)
    - It is necessary to execute a complete unwinding operation
    ##### System parameters:

    - Wind speed: **Above the nominal speed** (good production conditions)
    - Wind turbine Nominal Power: **1,500 kW**
    - Yaw motor consumption: **5 kW**
    - Electricity sale price: **0.10 €/kWh**
    - Yaw motor speed: **0.5 °/s**

### Experiment methodology

The experiment requires you to determine three critical times and then calculate the associated costs:

!!! example "📝 Task 1: Observe the disconnection time (cut-out)"
    When the wind turbine decides to start the unwinding, it must first disconnect from the electrical grid safely.
    ##### Procedure:

    1. Configure the simulator with the specified conditions
    2. Activate the cut-out (disconnection) process
    3. Use the graphic recorders (StripRecorders) to measure the time
    4. Record the **time from the cut-out start until the generated power reaches 0 kW**
    ##### Data to record:
    
    | Variable                          | Value                   |
    | -----------------------------------| -------------------------|
    | Disconnection time (t\_cutout)    | \_\_\_\_\_\_\_ seconds  |

!!! example "📝 Task 2: Calculate the unwinding time"
    Once disconnected, the nacelle must turn to unwind the cables.
    ##### Theoretical calculation:
    !!! example
    **Total angle to cover:**
    If the limit is 2.5 turns in one direction, we must turn 2.5 turns in the opposite direction
    Angle = 2.5 turns × 360°/turn = 900 degrees
    **Motor speed:** 0.5 °/s
    **Unwinding time:**
    t\_unwinding = Total angle / Speed
    t\_unwinding = 900° / 0.5 °/s = **1,800 seconds** = **30 minutes**
    ##### Experimental verification (optional):

    You can observe this process in the simulator if you modify the yaw speed parameters:

    - Locate the ['NacelleYawing.CWYawingSpeed'](../DSASExercises/DesenrrolleCables.md) 
                    and ['NacelleYawing.CCWYawingSpeed'](../DSASExercises/DesenrrolleCables.md) parameters
    - Set them to 0.5 °/s
    - Observe the real time the complete process takes
    ##### Data to record:

    | Variable                                  | Calculated value  | Observed value (optional) |
    | -------------------------------------------| ------------------| ----------------------------|
    | Unwinding time (t\_unwinding)             | 1,800 s (30 min)  | \_\_\_\_\_\_\_ seconds    |

!!! example "📝 Task 3: Observe the reconnection time (cut-in)"
    After completing the unwinding, the wind turbine must reconnect to the grid and reach stable production.
    ##### Procedure:

    1. Once the unwinding is completed, start the cut-in process
    2. Use the StripRecorders to measure the time
    3. Record the **time from the cut-in start until stable production at Nominal Power is reached**
   
    💡 **Note:** You can take advantage of the ["Comparison of cut-in in different wind turbine families"](ComparisonofcutinindifferentWind.md) experiment data if you already carried out measurements with wind above nominal speed.

    ##### Data to record:
    
    | Variable                        | Value                   |
    | ---------------------------------| -------------------------|
    | Reconnection time (t\_cutin)    | \_\_\_\_\_\_\_ seconds  |

### Cost calculation

!!! warning "💶 Economic analysis"
    Once all the times are obtained, we can calculate the total cost of the unwinding operation.
    ##### Total operation time:

    !!! example
    T\_total = t\_cutout + t\_unwinding + t\_cutin
    T\_total = \_\_\_\_\_ s + 1,800 s + \_\_\_\_\_ s = \_\_\_\_\_ seconds
    T\_total in hours = \_\_\_\_\_ s / 3,600 s/h = \_\_\_\_\_ hours
    ##### Cost components:
    ###### 1. Lost production (unearned income):
    !!! example
    **During cut-out, unwinding and cut-in:**
    Energy that would have been generated = Nominal Power × Total time
    E\_lost = 1,500 kW × \_\_\_\_\_ h = \_\_\_\_\_ kWh
    Lost income = E\_lost × Price
    Cost\_lost\_production = \_\_\_\_\_ kWh × 0.10 €/kWh = **\_\_\_\_\_ €**
    ###### 2. Yaw motor consumption (direct cost):

    !!! example
    **Only during the unwinding:**
    
    Consumed energy = Motor power × Unwinding time
    E\_consumed = 5 kW × (1,800 s / 3,600 s/h) = 5 kW × 0.5 h = 2.5 kWh
    Consumption cost = E\_consumed × Price
    Cost\_motors = 2.5 kWh × 0.10 €/kWh = **0.25 €**
    ###### 3. Total cost:
    !!! example
    Cost\_total = Cost\_lost\_production + Cost\_motors
    Cost\_total = \_\_\_\_\_ € + 0.25 € = **\_\_\_\_\_ €**

### Calculation template

#### 📊 Results summary

| MEASURED DATA                    |                |
| ----------------------------------| ----------------|
| Cut-out time (s)                 | \_\_\_\_\_\_\_ |
| Unwinding time (s)               | 1,800          |
| Cut-in time (s)                  | \_\_\_\_\_\_\_ |
| CALCULATED TIMES                 |                |
| Total operation time (s)         | \_\_\_\_\_\_\_ |
| Total operation time (h)         | \_\_\_\_\_\_\_ |
| COSTS                            |                |
| Lost energy (kWh)                | \_\_\_\_\_\_\_ |
| Lost income (€)                  | \_\_\_\_\_\_\_ |
| Motor consumption (kWh)          | 2.5            |
| Motor consumption cost (€)       | 0.25           |
| TOTAL COST (€)                   | \_\_\_\_\_\_\_ |

### Analysis and reflection

!!! tip "🤔 Questions for analysis"
    1. **Dominant cost component:**
        - Which is the main cost component: the lost production or the motor consumption?
        - In what proportion does each one contribute to the total cost?
    2. **Wind speed impact:**
        - How would the cost change if the unwinding occurred with wind below nominal speed?
        - Would it be more economical to wait for low wind conditions to unwind?
    3. **Unwinding frequency:**
        - If the wind pattern causes an unwinding every week, what would the annual cost be?
        - What percentage of the annual production would it represent?
    4. **Optimization:**
        - What strategies could reduce this cost?
        - Would it be worth increasing the allowed turn limit? What risks would it imply?
        - Would it be beneficial to have faster yaw motors? What considerations would have to be made?
    5. **Comparison between technologies:**
        - Is this cost the same for all wind turbine types (DSAS, RRC, DFIG)?
        - What differences could exist in the cut-out and cut-in times between technologies?

### Practical considerations

!!! info "🔧 Operational aspects in real wind farms"
    - **Intelligent planning:** Modern SCADA systems can plan unwinding operations during low production periods (nighttime low winds, for example)
    - **Weather prediction:** Forecasts are used to avoid unwinding just before optimal wind periods
    - **Continuous monitoring:** Early warning systems when approaching the winding limit
    - **Preventive strategies:** Some controllers try to balance the turns in both directions to minimize accumulation
    - **Adaptive limits:** In some designs, the turn limit can be adjusted according to the operating conditions

### Conclusions

!!! warning "📌 Key points"
    - The cable unwinding has a **significant economic cost**, mainly due to lost production
    - The cost is much higher when it occurs during optimal wind conditions
    - The **unwinding time** component is the longest of the whole process
    - The yaw motor consumption is relatively small compared to the lost production
    - A good **management strategy** can significantly minimize these costs
    - This is an example of how apparently simple operational decisions have **direct economic impact** on a wind farm
