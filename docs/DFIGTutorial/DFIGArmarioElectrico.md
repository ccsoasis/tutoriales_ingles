---
tags:
- PCC
- point of common connection
- 690V
- medium voltage
- step-up transformer
- GSC
- grid side converter
- internal view
- main switch
- grid fault
- phase fault simulator
- start
---

# Electrical cabinet

The "*Electrical cabinet with the Back-to-Back converters*" synoptic shows the components of the power electrical circuit, including the Back-to-Back converters.

There is an external view shown in the following figure.

![](<lib/Armario electrico cerrado interruptor en On e.jpg>)

When "**Internal view**" is selected, the physical arrangement of the different elements is shown, as shown in the following figure.

![](<lib/Armario electrico interno con comentarios.png>)

In both, the indicator corresponding to the "**Main switch**" is active, so that by clicking the left button when the mouse is over it, it changes state. This switch must be connected for a start-up operation ("START") to be launched. If, while in production, this switch is disconnected, a stop operation is started. The same happens when a voltage loss occurs in one of the phases: this "*grid fault*" can be simulated directly on this synoptic from the *checkboxes* titled "**Phase fault simulator**".

The high-level scheme where the different components of the electrical circuit are reflected, both internal to the wind turbine (Generator, Back-to-Back, Crowbar, GSC, Rotor, Stator and Crowbar switches, and grid connection transformer), as well as the connection to the Electrical Substation of the Wind Farm and its Transformer, and the grid itself, connected through a circuit that allows modeling short circuits on it, is shown in the following figure.

![](<lib/GraficoDFIG.jpg>)

The description of the relationship between Generator and Back-to-Back, with schemes, is described in [Description of the Back-to-Back Converters](ConvertidoresBackToBack.md).
