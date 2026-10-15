# Working area Power vs Frequency of the Grid

As mentioned in [Grid requirements](ConvertidoresBackToBackRequerimi.md), the frequency of the grid signals is not constant.

The following figure shows the "tolerable" area of the grid frequency value as a function of the total system (grid) load. (REE data).

![](<lib/Red - curva potencia vs frecuencia.png>)

The abscissas correspond to the frequency, while the ordinates correspond to the power in the grid (the produced and consumed one, which must be equal). The area shaded in red indicates acceptable operating conditions. The area shaded in yellow corresponds to the "desirable" operating conditions.

To understand this working area one must take into account the grid dynamics and the need for production to "always" adjust to demand in all its nodes. Let us suppose that we are with stable production and consumption, at a level of 80% of the maximum supported by the grid, with a frequency of 50 Hz and that, in a very short period of time, the conditions change: e.g., a new load enters (increase in total consumption) or one of the generators disconnects from the grid (decrease in available power): what happens is that there is a new distribution of the power that remains available (through a voltage drop at each supply point) and, in addition, a drop in the frequency of the generators that deliver power to the grid, due to their inertia (that is, the rotation shafts of the generators that remain connected slow down because they have more load). The different controllers of these generators will change their setpoints, increasing the mechanical energy incident on the rotor of each generator, to increase the new power demanded from it, and in this way maintain its frequency within the yellow zone. This whole mechanism of electrical power distribution requires a temporal evolution (the transition between the stable state before the change to the final stable state) and along the entire grid (each node has its own temporal evolution): the red area of the figure determines the margins from which the grid must not exit.

DFIG wind turbines are the first wind turbines that allow implementing, by themselves, a response mechanism against wind changes and grid changes compatible with the previous operating area, and therefore *they become generators connectable to the grid with the same possibilities as generators using other technologies* (thermal, hydraulic, cogeneration, etc.).
