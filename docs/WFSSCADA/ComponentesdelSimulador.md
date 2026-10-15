---
tags:
- continue
- stop
- run
- synoptics
- signals and connections
- present
- hide
- execution control
---

# Execution control and option access

Once the simulator program has been launched (that is, LdP execution with the "WFSSCADAr12.conf" configuration), the synoptics indicated in [Simulator Components.](Description.md) appear.

For the **simulation to start running** properly it is necessary to press the "***Run***" button of the ***Execution Control*** synoptic options menu.

![](<lib/Sinoptico control SCADA.png>)

At that moment this button changes functionality to "***Stop***". See the following figure.

![](<lib/Sinoptico control SCADA - Parar.png>)

If "Stop" is pressed, the simulation will stop and all the variables will remain "frozen", and its functionality will change to "***Continue***". See the following figure.

![](<lib/Sinoptico control SCADA - Continuar.png>)

When pressing "Continue", the simulation will continue with the same variable values as when "Stop" was pressed.

When pressing "***Synoptics***" the following drop-down menu will appear:

![](<lib/Sinoptico control SCADA - desplegable Sinopti.png>)

If you select "***Signals and Connections***" you will be able to access the internal definition of the connections between the different sub-systems of this simulator. For a description of this functionality consult the "[*Introduction to LdP*](../LdP_Help/Introduccion.md)" tutorial (*"Tutorials" -&gt; "Introduction to LdP"*).

The "[Parameters](Parameters.md)" option will allow you to access the visualization and editing of the parameters used in this simulator processes.

The "[Recorders](PowerpergroupTotalproducedPowera.md)" option will allow you to access various predefined recorders where the evolutions of several signal sets are presented.

The last option, marked with a tick, allows ***presenting*** or ***hiding*** the main synoptic of this simulator.
