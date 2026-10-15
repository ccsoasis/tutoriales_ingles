---
tags:
- production
- wind speed
- active power
- datalogging
- datalogger
- energy
- DFIG
- full converter
- Rotor Resistance Controlled
- automatic control
- 'use' column
- Automatic Dispatching
- manual mode
- automated control mechanism
- setpoint
- demand
- wind forecast
---

# Production Control

According to what is described in [Integration of a Wind Farm in the Electrical Grid](IntegrationofaWindFarmintheGrid.md) and in [The Control Room - SCADA](TheControlRoom.md), the basic Farm functionality is to deliver at all times the demanded power, which arrives as a setpoint, which depends basically on the wind forecast and atmospheric conditions. And this must be done respecting the needs imposed by the maintenance of the wind turbines and other farm equipment in their optimal state.

The farm operator must ensure that this condition is fulfilled. To do so they have the control of the start or stop of each one of the wind turbines.

Therefore in the control room of a Wind Farm there is a graphic representation like the one shown in the following figure:

![](<lib/Curvas-Control-Parque.png>)

*Legend*:

- (m/s) wind speed in meters per second.

- **Wind Forecast** (m/s): evolution of the wind speed forecast.

- **MeanWind** (m/s): average speed of the wind that has existed.

- **ExternalSetPoint** (MW): value of the power setpoint to generate, in megawatts.

- **PowertOutput** (MW): real value of the produced power, in megawatts.

The previous figure shows the graph with the mean wind evolution and the generated power at 15:57:00, together with the wind forecast and the expected generation at 16:02:00.

The control of the power generated at each moment is carried out from the SCADA with a procedure that depends on the wind turbine type in the Farm: if they are squirrel-cage generators directly connected to the grid, the only power control method is to stop or start wind turbines. It is the case of the previous figure. As a result, the average generated power follows the setpoint evolution with quite a lot of resolution, but with divergences. These divergences must be within the setpoint tolerance. If the generators allow an active power setpoint, as is the case of the wind turbines with rotor resistance control, or the doubly fed ones, this power control has much better resolution (follows the setpoint more faithfully).

The start or stop of the wind turbines, and/or the change of the setpoints to each wind turbine (depending on the case) can be done in "manual mode" or through an "automated control mechanism" (see [Automatic management](AutomaticDispatching.md))

In manual mode, the user can "stop" and "start" each wind turbine, from the SCADA, using a functionality similar to the one described in "[Possible action](SCADAview.md)".

The criteria for the Automatic management take into account considerations relative to the wind turbine aging, blade state, gearbox, generator, planned maintenance, etc. In general, the operator also has easy-to-use procedures to avoid the application of these criteria to certain wind turbines, in certain situations: this functionality is shown in the "Use" column in [SCADA application view](SCADAview.md).
