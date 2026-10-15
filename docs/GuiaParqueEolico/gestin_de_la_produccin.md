# Production Management

The production of a wind farm is controlled using the following functionalities:

- **Modifying the production setpoint of each one of the wind turbines**, if they have this functionality. That is, if they are of the *Doubly Fed* (DFIG), or "*Full Converter*" families, or have *Rotor Resistance Control*.  
The *production setpoint* allows *reducing the power that the wind turbine generates*, below the one corresponding to the existing wind at each moment. This functionality is used to implement the active power control (see [tutorial](../WFSSCADA/IntegracionconlaRedElectrica.md)).

- **Stopping or starting the appropriate number of wind turbines**. This possibility is for all wind turbine types.

In this simulator all the wind turbines are of the family called "with Squirrel Cage Generator" that do not admit a production setpoint. Therefore the way to control the farm production is done by starting or stopping wind turbines. These operations are carried out in the central grid of the main synoptic, where we have access to the SCADA. Press **[here](../WFSSCADA/SCADAview.md)** to access the detailed description.

The **start-up** or the **stop** of a certain wind turbine is carried out by pressing with the left mouse button on the chosen wind turbine cell corresponding to the "**Start/Stop**" column of the grid. If the content is the ![](Forward.png) symbol, it means the wind turbine is stopped, and without production: pressing it corresponds to sending the "START" command to the wind turbine. If the symbol is ![](paro.png), it means it is in production, and pressing it corresponds to sending the "STOP" command to the wind turbine.

To carry out these operations it is necessary to take into account:

- The **availability of each wind turbine**: each wind turbine may or may not be available due to some fault, or scheduled maintenance.

In the simulator this availability can be controlled through the controls functionality in the "**Operating state definition of the selected wind turbine**" section, located immediately below the wind turbine control grid. Its operation is described in the [tutorial](../WFSSCADA/Maintenanceview.md).
