---
tags:
- orientation operation
- min for orientation
---

# Automatic orientation

!!! tip "🎯 Automatic orientation (Yaw)"
    ***Objective:*** Analyze how the system automatically adjusts the orientation to align with the wind.
    ***What to observe:*** Wind direction, alignment error and yaw actuation.
    ***What to note:*** Minimum correction threshold and time needed to reach alignment.
    💡 identify whether the correction is continuous or in discrete steps.

This practice allows observing the "*Min for orientation*" and "*Min for start* (cutin)" wind values described in [Functional wind values](../DSASTutorial/DatosTecnicosValoresVientos.md).

The Controller has a parameter, "Min for start", which is the minimum wind at which it is worth putting the wind turbine in production.

There is another parameter, "Min for orientation", to implement the concept of "the wind is low to enter production but may rise: let's place the Nacelle facing the wind to minimize the start-up time".

- 1.Make sure there are no open incidents and that the wind turbine is disconnected from the grid (press STOP to make sure).

- 2.Reduce the wind to 1 m/s using the "Page Up" and/or "Down arrow" keys.

- 3.Fill in the "Ok" column of the "Manual STOP" incident and press "START".

- 4.Change the wind direction, so that the Nacelle is very misaligned.

- 5.Keep slowly raising the wind value, with the "Up arrow" key. Check that the Controller does not give the orientation order until the wind reaches 1.5 m/s.

- 6.Check that with this 1.5 m/s wind the Nacelle manages to orient itself, but the grid connection operation (cutin) does not start.

- 7.Keep slowly raising the wind value, with "Up arrow" up to approximately 3.6 m/s when the grid connection process (cutin) begins.
