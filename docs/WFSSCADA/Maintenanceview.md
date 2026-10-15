---
tags:
- operational status
---

# Wind turbine state management

In a real SCADA there are several procedures to indicate that a wind turbine "is not available" for production. In this simulator the interface indicated by the figure is available to pass a certain wind turbine to this "Not available" state.

To do so it is necessary to previously select the wind turbine in the grid ([SCADA application view](SCADAview.md)).

When a wind turbine is selected, it appears in the box, as shown in the following figure.

![](<lib/Sinoptico SCADA - control disponible - a fuer.png>)

In this situation, if the "Put it 'Out of Service'" button is pressed the application asks for confirmation and if it is given, it passes the indicated wind turbine state to "Not availabe" (Not available).

If the selected wind turbine were out of service, the functionality of this button will change, as the following figure indicates.

![](<lib/Sinoptico SCADA control disponible - pasar a.png>)

At any moment it is possible to change the "Efficiency" value of the selected wind turbine, by typing a value between 0 and 1 in the corresponding box. This value is used in the real production calculations.
