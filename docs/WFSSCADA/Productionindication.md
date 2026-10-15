---
tags:
- active power
- production
- total power
- total available power
- allowed power range
---

# Production Indication

In the lower right part are the indications of the "**Total Power**" that the farm is delivering, and of the total power it could give ("**Total available power**"), if all the wind turbines could be put in production for the current environmental conditions.

![](<lib/Sinoptico SCADA produccion total y disponible.png>)

The Total Power indicator has a background color that serves to indicate the relationship of the indicated value with the [Demand](Externaldemandsetpoint.md) requested from the farm.

If it is <mark>Green</mark> color, it means the production is within the **allowed power range** whose center is the current Demand value and its lower and upper limits are defined by the "***SetPointTolerance***" parameter (see [Parameters.](Parameters.md)).

If it is <mark>Red</mark>, it indicates the current production is above the upper limit of the *allowed power range*. This situation can give rise to economic penalties, for not attending the supply contract conditions.

If it is <mark>Yellow</mark>, it indicates the current production is below the allowed power range limit, and therefore, it is possible to start more wind turbines to increase it, if they are available.
