---
tags:
- switch
- synoptic
- substation
- unifilar
- symbols
- interlocking
---

# Legend of the symbols in the unifilar schematic

| ![](<lib/Rele-52-L.png>) | **Switch**: can be opened or closed in any situation. The connection or disconnection can be done *'hot'*, which implies that internally electrical arcs will occur that these devices are designed to withstand (for a maximum number of 'operations'), without risk for the other nearby devices nor for the human operator. |
|---|---|
| ![](<lib/Interruptor-Desconexion-y-Puesta-a-Tierra.png>) | **Disconnector**: should only be changed of state when there is no current or there cannot be current through it. If it is opened when there is current passing through it or closed when its terminal connected to the wind turbines has load (C-1, or C-2 or C-3 closed), then an electrical arc occurs. In this case, the device generally remains *damaged*. The line that joins the two switches indicates "**interlocking**": that is, in this case, the disconnector that connects with the evacuation line cannot be operated if the *disconnector* that connects the internal line to ground has not been opened previously (this position is used as a safety method in the Substation operations). |
| ![](<lib/Trafo-corriente.png>) | Current measurement transformer in the line. One per phase. |
| ![](<lib/Trafo-alimentaciones.png>) | Voltage measurement transformer in the line. One per line. |
| ![](<lib/Descarga-a-Tierra.png>) | Overvoltage protection and grounding system. |
| ![](<lib/Rele-50-51.png>) | Current imbalance detector. |
| ![](<lib/Rele-81.png>) | Detector that the frequency is kept within its allowed limits. |
| ![](<lib/Rele-27.png>) | Voltage below its lower limit detector. |
| ![](<lib/Rele-59.png>) | Voltage above its upper limit detector. |
