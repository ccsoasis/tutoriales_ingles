---
tags:
- SCADA
- striprecorder
- unifilar
- PCC
---

# The Control Room - SCADA

In a Wind Farm there is a Control Center (generally in a building strategically located in the territory where the Farm is deployed), from where the Wind Turbine state is monitored and their start and stop are commanded, the maximum power to generate and the reactive power. A fundamental part of said operations are carried out through a Monitoring and Control System (**SCADA**) (***Supervisory Control And Data Acquisition),*** that has *a communications channel* with each and every one of the Farm Wind Turbines. Its mission, however, is not to maintain the operation of each one of the components of each one of the Wind Turbines: the Wind Turbines can be assimilated to *Independent Production Plants*, capable of *autonomous operation*.

Through the SCADAs the following functions are carried out:

- collection of the Wind Turbine operational data, for their storage and analysis,

- the remote control of the Wind Turbines, understanding this as the capacity to give basic "Start" and "Stop" orders, and depending on the wind turbines, capacity to change certain operating parameters (e.g., maximum active power, reactive power, etc.)

Generally, the wind farm delivers its production according to certain *contractual conditions*. These conditions include, basically, how much active power and how much reactive power they commit to deliver. With the SCADA system the operations that guarantee the acquired commitments can be carried out, taking into account the plant maintenance operations.

To do so, the SCADA also receives data from *external systems* that *predict the wind*. Based on these predictions, the production conditions are determined, generally made by the transmission operating entity in the Electrical Grid (**TSO**: Transmission System Operator).

As a consequence, there is a basic control panel in the SCADA shown in the following fig 1.

![](<lib/Curvas-Control-Parque.png>) Fig 1

In this graph the *wind forecast* (in blue), the *demand forecast* (required production) (in green) are presented, together with the *real wind evolution* up to the current moment (in orange) and the *generated production* up to the current moment (in pink). This is the basic control panel of the Wind Farm.

It can be appreciated that the forecast demand value changes and remains stable in periods of approximately *15 minutes*. This parameter is part of the agreement with the Transmission System.

It can also be appreciated that the *generated production* adjusts with quite a lot of precision, on average, to the forecast demand.

On the other hand, the SCADA system has a synoptic where the state of each one of the farm wind turbines can be appreciated graphically, and quickly. As shown in the following figure.

![](<lib/Diagrama-ejemplo-estado-aerogeneradores.png>) Fig 2.

The power cabling between the wind turbines and the **PCC** (*Common Connection Point* or *Point of Common Connection*, in English) is also usually indicated, where the Electrical Grid connection occurs.

The companies that manage a large number of wind farms have additional Control Centers, also based on SCADA systems, that receive and aggregate the SCADA information in the farms. The following photo shows one of these installations.

![](<lib/Sala-control-parque-eolico.jpg>)
