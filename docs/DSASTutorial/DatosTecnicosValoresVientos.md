---
tags:
- abs max
- maximum temporary wind
- wind speed
---

# Functional wind values

![](<lib/Curva de potencia con vientos.png>)

| **Min for yawing** | Wind below which the Controller will not start the protocol to track the wind direction. |
|---|---|
| **Min for start-up** | Wind below which the Controller will not start the grid connection (cutin) operation. |
| **Min for Large Gen** | If the wind turbine is in production, with the Large Generator connected and the wind drops below this level, it will start the Large to Small Generator change operation. |
| **Max for Small Gen** | If the wind turbine is in production, with the Small Generator connected and the wind exceeds this level, the Controller will start the Small to Large Generator change operation. |
| **Max for start-up** | If the wind turbine is disconnected from the grid, and the wind is above this limit (normally quite above the Nominal Wind: for example 18 m/s) and the Controller receives the order to start the connection (cutin), it will not do it, unless the wind drops below this level. This limit has no influence if the wind turbine is in production and the wind exceeds this limit. The reason for this limit is statistical, so it has to be adjusted for each wind farm. It is about not starting the wind turbine if it is suspected that the wind is so strong that shortly it will exceed the maximum continuous operation wind and therefore it will have to disconnect. |
| **Max for continuous operation** | Upper limit at which the wind turbine can remain in production. If the wind remains at this level or slightly above for a certain period of time, the Controller proceeds to the disconnection. |
| **Max for temporary operation** | Similar to "Max for continuous operation", it is a higher value than it, but the time the Controller waits to proceed to the disconnection is shorter, if the wind remains equal to or above it. |
| **Absolute max** | If the wind reaches this value the Controller proceeds to disconnection immediately. |
