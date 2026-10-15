---
tags:
- dispatching
- allowed power range
- TiempoParaCancelarPropuesta
- production control
- automatic control
---

# Automatic management

In a real wind farm there are other systems that facilitate the Operation and Maintenance tasks, and that take into account aspects related to Planned Maintenance, the logistics of parts, equipment and fungible material, personnel management, etc.

These aspects influence the wind turbine management (start or stop) in relation to the production. Thus, for example, if a wind turbine must be started, and there are several available, one will be preferred over another based on various criteria.

In order to exemplify this influence of additional management aspects, in this simulator it has been chosen to include a management mechanism of the start or stop of a certain wind turbine using a criterion that has to do with:

- the *number of production hours* of each wind turbine (see "*Prod. Hours*" column in [SCADA application view](SCADAview.md))

- *the operator's choice* to allow said wind turbine to participate in said operation (see "Use" column in [SCADA application view](SCADAview.md))

The operation of this "Automatic management" mechanism of the wind turbines can be controlled through the *checkbox* located in the synoptic center and labeled "<mark>Automatic Control</mark>"

The algorithm used monitors the produced power and checks that it is within the limits defined by the ***allowed power range*** (see [Production Indication](Productionindication.md)). If it is above, it calculates the minimum set of wind turbines that makes, if they go to non-production, the total Farm power be the maximum possible within the allowed range, and "proposes" it to the SCADA operator. See the following figure.

![](<lib/Sinoptico SCADA propuesta de desconexion.png>)

The operator has a few seconds (see parameter "*WatingTimeToCancelProposal*" in [Parameters](Parameters.md)) to "Cancel" the proposal: otherwise, the stop of the indicated wind turbines is executed.

Similarly, if the power being produced is below the power range limit, the algorithm calculates the minimum set of wind turbines that makes the generated power rise to a value below the maximum limit.

![](<lib/Sinoptico SCADA propuesta de puesta en marcha.png>)
