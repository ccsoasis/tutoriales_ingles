---
tags:
- dispatching
- maintenance
---

# Simulation of putting a Wind Turbine "Not available"

- 1.Review the concepts of the possible wind turbine states (See [Wind turbine state management](Maintenanceview.md).)

- 2.Select a wind turbine in the SCADA view that is in "<mark>Production</mark>" or "<mark>Stop</mark>".

- 3.Use the button labeled "Put it 'Out of service'" so that its state passes to "<mark>Not available</mark>".

- 4.The wind turbine will remain as "the selected one", so that the button will change to the label "Put 'Active'". Pressing this button now the wind turbine will pass to "<mark>Stop</mark>". If you want it to pass to production you must press in the SCADA section, in its "***Start/Stop***" column.

That is, a wind turbine can pass to the "Not available" state both if it is in production and if it is not in production, for example due to
