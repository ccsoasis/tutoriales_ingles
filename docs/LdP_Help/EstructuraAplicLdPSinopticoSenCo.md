---
tags:
- signals and connections
- analog
- digital
- input signals
- output signals
- output signal
---

# Synoptic for editing Signals and Connections

**Synoptic for signal visualization and connection editing**

This synoptic, when visualized, presents the "*Internal connections*" list. See the following figure corresponding to a certain simulator.

![](<lib/Sinoptico Senales inicial.jpg>)

Each line corresponds to the connection of an "*output signal*" with an "*input signal*". The red background ones correspond to analog signals, and the gray background ones to digital.

The nomenclature of the names corresponds to the concepts of "Component," followed by "Process" within this component, followed by the actual name of the signal. "Parameters" is similar to "component."

Clicking on the column header ("Output" or "Input") displays the same content but sorted alphabetically. The following figure shows the same content but sorted by the "Output" column.

![](<lib/Sinoptico senales ordenado por Salida.jpg>)

A column can be placed in front of another by "dragging" it. For example, the following figure corresponds to the same content as the previous one, but where we have placed the "Input" column first (looking from the left side). (Left-click on the header of the "Output" column and, without releasing the button, drag it to the left of the "Input" column).

![](<lib/Sinoptico senales entrada primero.jpg>)

An "output signal" can be connected to several "input signals": this is best seen with a tree view. The content can also be presented as a set of trees, one per signal, by doing the following:

- Press with the right mouse button on any of the column headers. A space will appear above them, as shown in the following figure.

![](<lib/Sinoptico senales detalle treeview 1.jpg>)

- Select and drag the header of the column that will act as the tree root. You will obtain a presentation similar to the one in the figure.

![](<lib/Sinoptico senales treeview expandido.jpg>)

In this example, we have expanded the tree corresponding to the output signal "Controller.Control.PitchOut," which is connected to "SynopticWindNacelle.PitchControllerIn" and also to "SynopticDriveTrain.PitchIn."

## Additional tabs

The additional tabs in this synoptic allow you to access the list of all signals, both input and output.

![](<lib/Sinoptico senales salidas.jpg>)

![](<lib/Sinoptico senales senales entrada.jpg>)
