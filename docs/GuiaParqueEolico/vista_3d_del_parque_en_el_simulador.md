# Farm 3D View in the Simulator

In this exercise you will become familiar with the Wind Farm 3D view, and the location of any of its wind turbines through the references in the SCADA grid or in the main synoptic part that presents the farm power cabling.

1. Make sure you are running the simulation: to do so go to the "**Running WFSSCADA**" synoptic, and use the second menu button, which must show "**Stop**".

2. In the central part of the main Synoptic, below the SCADA grid, find the "**Farm 3D View**" checkbox. Click with the left mouse button, so that it appears marked with a tick ![](CheckBoxChecked_SUAVE.png)  
.  
After a few seconds a synoptic will appear with the Farm 3D view: the "**WFS3D**" synoptic. The point of view will be "centered" on a certain wind turbine.

3. Move the mouse pointer within the "**WFS3D**" synoptic.

4. Press the left mouse button and, keeping it pressed, move the mouse: **the wind turbine view will change**, always keeping the wind turbine nacelle center in the synoptic center.

5. To **change the wind turbine** that occupies the synoptic center, you have two options:

    1. **Through the SCADA grid**: choose the row corresponding to the chosen wind turbine and double-click on any column (except those marked as "*Use*" and "*Start/Stop*"). You will observe that the synoptic center moves to present the chosen wind turbine.

    2. **Through the corresponding icon in the upper part of the Synoptic**, associated with the power cable connections.

6. Choose a wind turbine that is in "*State*" "Not Available": you will observe that its blades do not turn.

7. Choose a wind turbine that is in "*State*" "Stop": you will observe that its blades do not turn.

8. On a wind turbine that is in "*State*" "Stop" double-click on the cell corresponding to its row and the "**Start/Stop**" column: you will observe that the symbol changes from ![](Forward.png) to ![](paro.png), indicating that the wind turbine has started.  
Now you can stop it by pressing on the same cell. You will be able to see in the 3D view that the blades of that wind turbine begin to turn.  
  
NOTE: In reality, the start-up of a wind turbine takes at least 1 minute or more, depending on the wind turbine type and the existing wind. The stop of a wind turbine is in the order of a few seconds (10 to 15), also depending on the wind turbine type and the existing wind.

9. If you modify the **wind direction** in the synoptic (**circular control**), you will be able to see that all the wind turbines that are in "**Production**" change their orientation, following the changes you make in the wind direction.  
  
NOTE: You can check that the "**Orientation**" column cells in the SCADA grid indicate different values, but very close, to the specified direction. This is because the wind is not totally uniform in the Farm. In real cases, the orientation of a certain wind turbine can differ a lot from the one obtained from the meteorological station, due to the wind turbine wind vane miscalibration.
