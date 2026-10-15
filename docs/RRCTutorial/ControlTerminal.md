# Control Terminal

This synoptic mimics the wind turbine Operator Control Terminal, and also the "Manual" command buttons that may exist in the Controller panel.

To improve the didactic aspect, in this synoptic a set of internal variables are shown directly, which are usually only accessible in a real Terminal by navigating through a set of hierarchical menus.

Most of the indicators have functionalities similar to those described in the Double Speed with Active Stall wind turbine tutorial (*DSASWTSimulator*) for the "*Control Terminal*" synoptic. Here the indicators specific to this Terminal are discussed.

The "Power vs Slip Graph" menu option is described in detail in the [following](PotenciavsDeslizamientodelRotor.md) section.

![](<lib/Control Terminal en STOP.jpg>) Fig 1

| ![](<lib/PotActivaDeseada.jpg>) | With this graphic indicator the *maximum power* desired from the wind turbine value can be changed. This value determines the horizontal section value. |
|---|---|
| ![](<lib/RRC potencia factor de potencia y pot disipad.jpg>) | These indicators correspond to: "**Gen. Power**": The power currently being generated (in Ws). "**PF**": current power factor. "**RCCPower**": power dissipated in the Rotor circuit (In Ws). See [Control electronic circuit](Circuitoelectrnicodelcontrol.md). |
| ![](<lib/RRC PWMRext.jpg>) | Value of the IGBT gate signal "Duty Cycle" (**DutyCycle**). See [Most significant signal graphs](Grficosdelassealesmssignificativ.md). |
