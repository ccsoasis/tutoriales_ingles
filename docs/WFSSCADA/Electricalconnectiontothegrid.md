---
tags:
- busbars
- generator
- electric diagram
- electrical measurement units
- point of common connection
- PCC
- grid
- common connection point
- main switch
- connection busbars
- thyristors
- bypass contactors
- current measurement transformers
- generator connection contactors
- power factor
- Softstarter
- controller
---

# Grid connection

The power connection of the wind turbine generator to the Grid is carried out, generally, through a step-up transformer that goes from the three-phase 690V to Medium Voltage (15 KV to 30 KV), although there are generators that work in Medium Voltage (5KV). This transformer can be located inside the Tower (case of Spain), or outside, very close to the Tower. In the most powerful wind turbines, the transformer is located in the Nacelle. The output of this transformer connects with the closest power cable, which connects it with the Substation, to the *Common Connection Point* (*PCC*).

Internally, the power cable connection varies from one wind turbine to another. In the following figure the main components are shown for a wind turbine with a squirrel-cage generator with two possible connection types (which is equivalent to having two independent generators).

![](<lib/Esquema electrico conexion generador.png>)

These elements are inside a cabinet that complies with various safety regulations (IP56 type). Its main components are:

- The **Main Switch**: which can be actuated by hand, from the outside, and is also controlled (only in the disconnection operation) by the wind turbine Controller.

- The **connection busbars** (thick lines in the previous figure diagram): constitute the power connections between the cables that come down from the generator and the grid cables. There are usually several groups, grouped by panels, according to the arrangement where the other power elements are placed (mainly the Thyristors and their Bypass contactors).

- The **Thyristors** and their **Bypass contactors**: these are the physical components of the *Softstarter* mechanism used to carry out the generator grid connection operation.

- The **current measurement transformers** (one per phase).

- The **generator connection contactors** (one per connection type).

- Additionally there is usually in this wind turbine type a **capacitor bank** (not shown in the previous diagram), located in the Nacelle, very close to the Generator, to control the *power factor*.

- The *electronic* and *electrical* elements (relays, electrical connection panels, etc.) and the main **Controller** are also usually located in this cabinet.
