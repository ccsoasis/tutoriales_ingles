---
tags:
- stop
- start
- cutin
- cutout
---

# With winds in the upper part of the range

!!! tip "🎯 Gusts with winds near the operation limit"
    ***Objective:*** Observe the wind turbine reaction to large-amplitude gusts when it operates near the maximum allowed wind (MaxWindForCutin ~18 m/s), and understand the automatic cutout/cutin protocol.
    ***What to observe:*** The cutout activation when the wind exceeds 25 m/s (WindMaxForOperation), the automatic cutin retry when the wind drops, and the difference between a gust that causes cutout and one that does not.
    💡 The system remembers the last order (START or STOP). What does that imply for the behavior against gusts?

!!! warning "❓ Guiding questions"
    1. In Case 1 (gust "Standard60x10"), how much time passes between the automatic cutout and the new cutin? What does the Controller check before trying to reconnect?
    2. Why in Case 2 (gust "StandardGust60x4") no cutout occurs although the wind rises significantly?
    3. What operational meaning does the fact that the system "remembers" the last received order (START/STOP) have?

This experiment shows the wind turbine reaction when it is operating with wind speeds close to "*MaxWindForCutin*" (see [About specific wind values](../DFIGTutorial/Sobrevaloresespecficosdevientos.md)) and receives a large-amplitude wind gust.

This value of "*maximum tolerable wind before starting the grid connection operation*" is set through the parameter "*ControllerCutin.MaxWindForCutin*" and literally prevents the wind turbine from starting the start-up operation (*cutin*) if the wind is above said value, even if the user presses the START button. Typically this value is around 18 m/s.

There is another parameter "*Controller.WindMaxForOperation*" that is used by the Controller to stop production (cutout) if the wind exceeds said value and persists beyond a certain "confirmation" time. In our case this value is 25 m/s and the time approximately 1 minute.

There is another wind value "*Controller.WindMaxForTemporalOperation*" (in our case 28 m/s) whose meaning is the same as "*Controller.WindMaxForOperation*", but tolerating a much shorter confirmation time (a few seconds).

*The cutout operation in these cases is also the one that is started when the user presses the STOP button while in production, but the Controller state is not exactly the same*. The idea is that the wind turbine tries to reconnect immediately after the gust disappears.

## Case 1

In this experiment we will start with the wind turbine in STOP, and with a wind just below "*MaxWindForCutin*" (that is, 17.7 m/s), we will press START and wait for it to enter production.

When it stabilizes in production we will apply a "Standard60x10" type gust and we will obtain a record similar to the one shown in the following graph.

![](<lib/DFIG 17-9 m-s con windgust 60x10.jpg>)

In this case, the wind remains above 25 m/s for enough time to launch the *cutout* operation. This operation effectively stops the Power Train; however, immediately after, the Controller checks that there is enough wind to do cutin and below the maximum to try cutin, so that, after a check time, it launches the cutin operation, which leaves the wind turbine in production again, as before the gust. This occurs because the Controller "remembers" that the last received order was "START".

This example shows that the real meaning of pressing "**START**" can be summarized with the sentence:  
"**Try to get into production and stay in production until you receive the "STOP" order**".  
On the other hand, the meaning of pressing "**STOP**" can be summarized as:  
"**If in production, disconnect and stop the Power Train, and stay in that state until you receive the "START" order**".

## Case 2

In this case we will repeat the previous experiment (wind at 17.7 m/s) but we will apply a lower-amplitude gust "StandardGust60x4". In this case we will obtain a graph similar to the following.

![](<lib/DFIG 17-9 m-s con windgust 120x40.jpg>)

In this case, since the wind never exceeds the "*Controller.WindMaxForOperation*" value (25 m/s), no *cutout* operation occurs.
