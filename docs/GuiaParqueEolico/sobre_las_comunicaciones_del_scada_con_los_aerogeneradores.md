# About the SCADA communications with the wind turbines

The SCADA communications with the wind turbine Controllers use a protocol known as **"[polling](https://en.wikipedia.org/wiki/Polling_(computer_science))":** each time *the SCADA wants to obtain data* from a wind turbine, or wants to *send it a command*, it emits a "question" to the Controller of said wind turbine. This responds with the requested data.

The **standard cadence of these questions is 10 minutes**. In most recent SCADAs, this cadence is much faster (1 per minute at least).

In the Simulator, the communications between the SCADA and the wind turbines are presented in the "**Est.Comm**" column ("*Communications state*") of the SCADA grid: when the indicator is yellow, it simulates that the SCADA is sending the request to that wind turbine, and waiting for its response. This operation is carried out sequentially for all the wind turbines, at a cadence determined by the value selected in the "**Communications Speed**" widget, located in the lower right part of the Synoptic. The default value is 2 seconds to facilitate the visualization during the simulation.
