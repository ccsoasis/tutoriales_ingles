# Wind speed change tracking

As reflected in the **[production tracking graph](../WFSSCADA/Productioncontrol.md)**, the wind speed is a parameter whose evolution over time is known previously, with a certain degree of precision.

In this exercise it is proposed that you make **[wind speed modifications](../WFSSCADA/Meteorologicalstation.md)**, maintaining the production demand (**[SetPoint](../WFSSCADA/Externaldemandsetpoint.md)**), and start or stop wind turbines manually, so that the "[**Total Power**](../WFSSCADA/Productionindication.md)" indicator always has a green background, which indicates that the power being produced is in accordance with the demanded one (SetPoint).

Previously you must create a [**Recorder**](../WFSSCADA/Grficosdeevolucindeseales.md) with the "Predefined panel" with title "Basic + Power per WT Group".

Repeat the same operation but this time letting the [**SCADA Automatic Control**](../WFSSCADA/AutomaticDispatching.md) decide/suggest which wind turbines must be started or stopped.

Remember that the SCADA Automatic Control algorithm takes into account the indications to take into account, or not, each one of the wind turbines, according to the "**Use**" column content of the SCADA grid.

Compare the power evolutions and the start-ups and/or stops in both cases.
