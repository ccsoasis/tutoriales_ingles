---
tags:
- total power
- allowed power range
---

# Manual production control

- 1.Make sure the "[Automatic control](AutomaticDispatching.md)" checkbox is not selected.

- 2.In the "[Meteorological station](Meteorologicalstation.md)" increase the wind.

- 3.In the [SCADA](SCADAview.md) observe that:

- 1.The wind in each wind turbine, on average, also increases.

- 2.The wind in each wind turbine is slightly different in each one of them. This is due to the random nature of the wind and the farm orographic profile.

- 3.The *Total Power* increases.

- 4.Check that the background color of the *Total Power* indicator changes to red when the wind increase makes this value exceed the [allowed power range](Productionindication.md).

- 4.You must get the Total Production to return to a value such that the background is green. To do so go to the SCADA view and select a wind turbine that is in "Production"; press with the mouse (left button) on the "Start/Stop" column, so that the wind turbine passes to "Stop". Observe that the Total Production decreases.  
Repeat this operation with other wind turbines that are in "Production" until the Total Power background passes to green.

- 5.Repeat the cycle 2 to 4, but this time decreasing the wind speed.
