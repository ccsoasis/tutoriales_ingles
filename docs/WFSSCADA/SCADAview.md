---
tags:
- supervisory control and data acquisition
- SCADA
- communications
- 3D view
- production hours
---

# SCADA application view

The central part of the synoptic presents an interface similar to the one found in the synoptic center. See figure 1.

![](<lib/Sinoptico SCADA - panel de visualizacion y co.png>) Fig 1.

Doing *click* with the left mouse button on any "*row*" of this grid selects a certain wind turbine, and said row changes color to pink. If the "*3D View*" synoptic is visible and a "*double click*" is done on a row, the "*3D View*" moves to this generator.

The description of each one of these columns, functionalities and meanings is the following:

- Column "**ID**": internal indicator of a certain wind turbine.

- Column "**State**"

| <mark>Not available</mark> | For some cause, the wind turbine cannot/should not be started. |
|---|---|
| <mark>Stop</mark> | The wind turbine is available, but at this moment it is not in production. |
| <mark>Production</mark> | The wind turbine is in production |

- Column "**Name**": Identifying name of the wind turbine.

- Column "**Model**": wind turbine type.

- Column "**Use**": if the check-box is not marked, this wind turbine will not be taken into account in the wind turbine start/stop algorithm. See [Automatic management](AutomaticDispatching.md).

- Column "**Start/Stop**": this box allows starting or stopping the wind turbine

| **Icon** | **State** | **Possible action** |
|---|---|---|
| (Without icon) | The wind turbine is not available | None, until the wind turbine becomes available and stopped. See [Maintenance operations view](Maintenanceview.md) |
| ![](<lib/Parada.ico>) | In "<mark>Production</mark>" | With double click the wind turbine goes to production |
| ![](<lib/Arranca.ico>) | Stopped, "<mark>Stop</mark>" | With double click the wind turbine goes to "Stop", available but without production. |

- Column "**Est. Comm**": indicates the communications state between the SCADA and the wind turbine.

| ![](<lib/Led-amarillo.ico>) | At that instant, the SCADA is asking the wind turbine to send it its state. |
|---|---|
| ![](<lib/Led-verde.ico>) | The SCADA has received satisfactorily the state data requested from the wind turbine. |
| ![](<lib/Led-rojo.ico>) | The SCADA did not correctly receive a response to its state request. |

- Column "**Nom. Power**": the wind turbine nominal power. In KW.

- Column "**Real Power**": the power the wind turbine is producing at that moment. In KW.

- Column "**Wind**": the wind measured by the wind turbine anemometer, at that moment. In m/s.

- Column "**Orientation**": indicates the Nacelle orientation at that moment. In degrees, between 0 and 360.

- Column "**Prod. Hours**": indicates the number of wind turbine production hours. This value is used to decide which are the wind turbines that must be started or stopped in an [automatic farm management](AutomaticDispatching.md).
