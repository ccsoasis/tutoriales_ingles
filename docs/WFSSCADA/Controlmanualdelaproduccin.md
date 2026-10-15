---
tags:
- allowed power range
- total production
---

# Automatic production control

- 1.Make sure the "[Automatic control](AutomaticDispatching.md)" checkbox is selected.

- 2.In the "[Meteorological station](Meteorologicalstation.md)" increase the wind.

- 3.In the [SCADA](SCADAview.md) observe that:

- 1.The wind in each wind turbine, on average, also increases.

- 2.The wind in each wind turbine is slightly different in each one of them. This is due to the random nature of the wind and the farm orographic profile.

- 3.The *Total Power* increases.

- 4.Check that the background color of the *Total Power* indicator changes to <mark>red</mark> when the wind increase makes this value exceed the [allowed power range](Productionindication.md).

- 4.Observe that a message appears such as the one shown in the following figure.  
![](<lib/Sinoptico SCADA propuesta de desconexion.png>)  
  
This is the "operation proposal" suggested with the control algorithm so that the Total Production becomes within the [allowed power range](Productionindication.md).  
You have "*Time to cancel*" seconds to "***Cancel***" this proposal. After this time the simulator assumes the answer is affirmative.  
You can also press the "***Accept***" button so that it executes immediately.

- 5.Repeat from 2 to 4 but this time decreasing the wind.  
Observe that when the wind decrease is sufficient, the background color of the Total Production indicator will change to <mark>yellow</mark>, at which moment a message like the one in the following figure will appear.  
![](<lib/Sinoptico SCADA propuesta de puesta en marcha.png>)  
  
This is the "operation proposal" suggested with the control algorithm so that the Total Production becomes within the [allowed power range](Productionindication.md).  
You have "*Time to cancel*" seconds to "***Cancel***" this proposal. After this time the simulator assumes the answer is affirmative.  
You can also press the "***Accept***" button so that it executes immediately.
