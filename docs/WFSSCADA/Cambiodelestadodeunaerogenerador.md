# 3D view presentation

The [3D view](3DView.md) is controlled from the check-box labeled "***Farm 3D View***".

Make sure it is selected and you will see how the corresponding synoptic appears (described in [3D View](3DView.md)).

While it is visible, this synoptic will present a view centered on the wind turbine that is selected in the [SCADA](SCADAview.md) section.

In the "[Meteorological station](Meteorologicalstation.md)" modify the wind direction by turning the circular button with red mark. Observe that the selected wind turbine changes direction, adapting to the new wind direction.

![](<lib/Sinoptico SCADA estacion meteorologica.png>)

The response time for wind direction changes in a real wind turbine is quite slow, of the order of 0.5 degrees/second. That is it takes 720 seconds (=360 /0.5) to complete a full turn, that is, 12 minutes. In the simulator an immediate response has been chosen to avoid these very long waiting times.
