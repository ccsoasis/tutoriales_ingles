---
tags:
- max for start
- max for continuous operation
- max for temporary operation
- absolute max
- Controller.WindAbsolutMax
- ControllerCutin.MaxWindForCutin
- Controller.WindMaxForOperation
---

# Behavior against very strong winds

!!! tip "🎯 Behavior with strong winds"
    ***Objective:*** Relate gusts/high wind with protection and control strategies.
    ***What to observe:*** Wind speed, alarms/protections and state changes.
    ***What to note:*** Gust events, action taken, approximate thresholds and final state.
    💡 Distinguish between limitation (reduction) and stop (cut-out).

In this practice the objective is to experiment the behavior against the wind value, according to the wind description in [Functional wind values](../DSASTutorial/DatosTecnicosValoresVientos.md).

In the [Power cable unwinding](DesenrrolleCables.md) practice the influence of the "*Min for orientation*" and "*Min for start*" wind values is observed. In this practice it is proposed to observe the influence of the "*Max for start*", "*Max for continuous operation*", "*Max for temporary operation*" and "*Absolute max*" wind values, described in [Functional wind values](../DSASTutorial/DatosTecnicosValoresVientos.md).

The concepts to explore are the following:

- When the wind exceeds a certain limit, the wind turbine must disconnect from the grid and place its blades so that the wind effect is minimized. This must occur in any situation: that is, if it is in production it must disconnect, if it is disconnected it will make no connection attempt. This is the "*Absolute max*" concept.  
This value is controlled in this simulator by the "*Controller.WindAbsolutMax*" parameter, with a default value of **30 m/s**.

- When the wind turbine is disconnected from the grid and the wind exceeds a certain value, it is understood that it is not worth starting a connection operation (cutin) because it is estimated that possibly it will have to stop due to high wind shortly. This is the "*Max for start*" concept, which is associated with the "*ControllerCutin.MaxWindForCutin*" parameter. The default value is **18 m/s**.

- When the wind turbine is in production there is a wind limit at which production is maintained, even if it is much higher than the nominal wind. This is the "*Max for continuous operation*" concept, which is associated with the "*Controller.WindMaxForOperation*" parameter, which has a default value of **25 m/s**.  
When the wind exceeds this value, the wind turbine does not immediately start a disconnection operation but waits for a certain time, which depends on the known wind behavior in the place where the wind turbine is located.

- When the wind turbine is in production and the wind has exceeded "*Max for continuous operation*" but has not reached "*Absolute max*", another parameter is used, "Controller.WinMaxForTemporalOperation", which has an associated waiting time shorter than for the "*Max for continuous operation*" case, before starting the disconnection operation.  
The default value of this parameter is **28 m/s**.

The ideas behind these parameters refer to the production maximization when the wind is high, minimizing the risks and the stresses to which the wind turbine is subjected.
