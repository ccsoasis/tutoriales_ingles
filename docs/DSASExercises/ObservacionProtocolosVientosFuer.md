---
tags:
- wind
- max for start
- messages
- incident history
---

# Observation of the behavior with very strong winds: several cases

!!! tip "🎯 Strong wind protocols"
    ***Objective:*** Understand the automatic protocols that are activated against strong winds.
    ***What to observe:*** Wind speed, state changes, power limitation or stop.
    ***What to note:*** Protection sequence and final system state.
    💡 differentiate between progressive power reduction and complete stop.

In this practice you must observe the protocols used by the Controller in relation to high winds.

- 1.Make sure the wind turbine is disconnected from the grid. Press "STOP" if necessary. Make sure there is no pending incident, except "Manual STOP".

- 2.Set a high wind, but below "*Max for start*" (18 m/s). Check that the wind turbine carries out the grid connection operation (cutin) normally.

- 3.Disconnect the wind turbine from the grid: press "STOP".

- 4.Set a wind above 18 m/s and check that the wind turbine carries out the operation of orienting to the wind, but does not complete the grid connection. You can observe that the Controller is continuously monitoring the wind value: press the "*Messages*" tab of the "Control Terminal" synoptic.

- 5.Reduce the wind to a little below 18 m/s, for example 17.9 m/s. Check that immediately the grid connection process (cutin) begins.

## Very high wind protocols.

- 1.Put the wind turbine in grid connection.

- 2.Keep slowly raising the wind with the arrows or paging keys up to 25 m/s. ("*Max for continuous operation*" value.) Check that the wind turbine remains in production indefinitely.

- 3.Increase the wind above 25 m/s. You will observe that after a certain time has elapsed the Controller disconnects the generator from the grid (cutout) and generates an incident with the message "*Wind &gt; WinMaxForOperation for more than 100 s*".

- 4.If now you slowly decrease the wind, check that nothing happens until the wind has a value below 18 m/s.

- 5.Observe that when the wind drops below 18 m/s, the incident passes automatically to the "*Incident history*", and the Controller automatically starts the grid connection process.

- 6.Keep slowly raising the wind with the arrows or paging keys up to a value somewhat above 28 m/s, for example 28.1 m/s. ("*Max for temporary operation*" value.) You will check that the Controller will start the grid disconnection (cutout) after a time that is notably lower than in point 3.  
Two incidents will appear with the descriptions: "Wind &gt; WindMasForOperation for more than 100 s" and "Wind &gt; WindMaxForTemporalOperation for more than 5 s". Note that the second has a slightly earlier "Start".

- 7.If now you slowly decrease the wind, check that nothing happens until the wind has a value below 18 m/s.

- 8.Observe that when the wind drops below 18 m/s, the incidents pass automatically to the "*Incident history*", and the Controller automatically starts the grid connection process.

- 9.Now increase the wind until reaching 30 m/s ("*Absolute max*" value). You will check that an incident with the description "Wind &gt; WindAbsolutMax for more than 1 s" will be generated in a very short time, followed by two others similar to those in point 6.
