---
tags:
- wind vane
- nacelle orientation
- misorientation
- direction
- yaw mechanism
- yawing
- cutin
- cutout
- aspect ratio
- duty cycle
---

# Wind specification and top view of the nacelle

## Wind and top views of the nacelle

![](<lib/WindNacelle a 1 5 grados.jpg>)

In this synoptic there are four panels:

In the bottom-left one the following are shown: a) the wind direction and its intensity (dark blue arrow); b) the nacelle orientation.

In the bottom-right one the blade angle (Pitch) is shown together with the vectors corresponding to the winds incident on it.

In the top-left one the following are shown:

- The state of the nacelle yawing motors.

- An oscilloscope view of the wind vane signal (see [Measurement of the wind direction - description of a wind vane](MedicindeladireccionDireccionVie.md)).

The top-right panel contains:

- The fields where the wind intensity and its direction can be varied.

- Indicators of:

The details of these indicators are explained below.

| ![](<lib/Indicadores de Viento espanol.jpg>) | The way of changing the wind or its direction can be modified in two ways: By directly typing the desired value. When the value is changed, the background changes to <mark>yellow</mark> to indicate that the indicated value does not correspond to the (internal) value that is actually being used at that moment in the simulator. When the "Enter" key is pressed, the "proposed" value is validated and, eventually, replaces the existing value: when this happens the background turns white. Before pressing "Enter" it is possible to abort the change with the "Esc" key. Using the Page Up (+1 m/s), Page Down (-1 m/s); Up Arrow (+0.1 m/s) and Down Arrow (-0.1 m/s) keys. In the case of the Direction (degrees) Page Up (+10), Page Down (-10); Up Arrow (+1) and Down Arrow (-1). |
|---|---|
| ![](<lib/Indicador vueltas cables espanol.jpg>) | The power cables hang from the nacelle down to the base of the tower. When the wind turns, the Controller acts on the nacelle yawing mechanism (*yawing*) and these cables wind on themselves. It may happen that the wind direction changes in the same direction for long enough for the number of winding turns to exceed a certain value that compromises the electrical safety of the installation. To avoid reaching that point, the wind turbine contains a limit switch whose body is attached to the inside of the tower, which does not rotate, and the detector is attached to a cable, whose other end is attached to the head of the power cables. There is a spring that always keeps this cable in tension; in this way, when the number of winding turns of the power cables reaches a certain value, this limit switch is activated. The tension and length of the limit switch cable is adjusted so that the activation occurs at a certain preset value. In the simulator this value is specified through "*Parameter.NacelleYawing.MaxCableTwist*", which is connected to the input "*Nacelle.Yawing.MaxCableTwistIn*". A typical value of this parameter is 3.5 turns. The output of this limit switch ("*Nacelle.Yawing.MaxCablesTurnsReached*") reaches the Controller ("*Controller.Control.CableMaxTwistReachedIn*") and its activation implies that the two software protection levels of the Controller have been skipped (see below) and a first-level incident occurs, equivalent to a major fault. An operation is started in which the wind turbine disconnects from the grid and remains stopped, deactivating even the yawing operations. There is another Controller parameter related to the monitoring of the cable winding: this parameter enters through the signal "*Controller.Control.MaxCableTwistIn*", connected to "*Parameter.ControllerYawing.MaxCableTwist*". When the number of winding turns of the cables exceeds this level (typically 2.5 turns), an incident is generated that triggers taking the wind turbine out of production (*cutout*), followed by a cable unwinding operation. When the number of cable turns is less than 0.5 turns (in absolute value), the wind turbine connection operation (*cutin*) is automatically started, so that the wind turbine finally continues production. A third parameter ("*Parameter.ControllerYawing.MaxCableTwistBeforeCutin*") that is connected to the Controller ("*Controller.Control.MaxCableTwistBeforeCutin*") has the mission of launching the cable unwinding operation when its value is exceeded (typically 1.5 turns), before launching a grid connection operation. That is, if the wind turbine is out of production and all the necessary conditions are met (wind, etc.) and the START order is given, first it is checked whether the cable winding turns exceed the value of this parameter: if they are more, then the cable unwinding operation is launched. The purpose of this strategy is to minimize the probability of having to stop to unwind cables when production is reached. |
| ![](<lib/Indicador orientacion gondola espanol.jpg>) | This indicator shows the angle turned by the cables, i.e. the indicated value can be higher than 360 or lower than -360: each cable winding turn adds or subtracts 360 degrees. |
| ![](<lib/Senal veleta espanol.jpg>) | The wind vane signal is a digital signal (see [Measurement of the wind direction - description of a wind vane](MedicindeladireccionDireccionVie.md)) that can take the following values: Continuously On. Continuously Off. In oscillation. In the first two cases the nacelle is misoriented from the wind by an angle higher than the wind vane oscillation. In the latter case its duty cycle (statistical value) is proportional to the existing misorientation between the wind and the nacelle. |
| ![](<lib/Giros izq y derecha espanol.jpg>) | These two buttons indicate the yawing signals that are emitted by the Controller to control the corresponding motors: one group of motors for each of the two rotation directions. They can also be put in "Force" mode (F6) with which it is possible to manually control these movements (independently of the Controller signals). This possibility allows creating anomalous situations to observe the Controller's reaction. For example, leaving one of these buttons in "Force" mode and changing the wind direction so that the Controller changes the signal that reaches it, a specific incident will be created. |

The following graphs show three cases of the nacelle orientation and the corresponding shapes of the wind vane signal.

| ![](<lib/Desorientacion a Izquierdas.jpg>) | ![](<lib/Desorientacion a derechas.jpg>) | ![](<lib/Orientacion dentro de limites.jpg>) |
|---|---|---|
