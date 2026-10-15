---
tags:
- manual turn
- wind
- effective wind speed
- power factor
- air density
- moment of inertia
- blade angle
- pitch
- generator connection
- yaw motors
- thyristors
- bypass
- brake hydraulic circuit pump
- HCU
- gearbox low-speed shaft
- VCU
- vibrations
- nacelle orientation
- incidents
- overspeed detectors
---

# Control Terminal synoptic

In a real Wind Turbine, the only way to know its actual status is by connecting the so-called "Control Terminal" to the Controller. The section [Operator Control Terminal](ControlTerminal.md) describes a typycal Control Terminal for the Dual Speed Active Stall family of Wind Turbines.

Using it, the operator can access the values of the internal variables of the subsystems, of the Grid, power production, pitch angles, wind speed, etc. Unfortunately, the user-interface is quite limited (typically 4 alfanumeric + symbols lines of 40 characters each), unsuitable for direct access to all its functionalities: this drawback is solved using a set of *hierarchical menus*; example: accessing the hydraulic circuit pressure is through the second submenu of the first menu in line 3. This approach is very convenient for already trained operators, but constitutes a heavy inconvenient for new students. 

In LdP-based Simulators, like this one, a more didactic and more generic solution has been chosen, focused on a single synoptic, which is presented in the following figure and described below.

![](<lib/Control terminal espaol inicial en produccion.png>)

## Main concepts of the Simulator "Control Terminal"

One of the objectives is that the student has immediate access to key variables to understand what is happening.

- Presentation of all the important variables in an accessible way



The upper left part, shows the most important commands signals from the Controller:

- **Pitch**: computed value of the blade pitch angle. In degrees. If everything is working properly, the pitch angle in the blades must be this one.
- 
- **Hydraulic Pump**: digital signal that controls the hydraulic pump.

- **Hardbrake**, **Softbrake**: digital command signals for the brake devices.

- **YCCW**, **YCW**: digital command signals for the yawing motors. YCCW => Turn to the left, YCW = Turn to the right.

- **Large Generator**, **Small Generator**: digital command signals for the electric generator connection cabinet.

- **Thyristors**, **Bypass Thyristor**: digital command signals for thyristors and bypass banks. 

In the table in the *upper central part* presents :

- Some parameters assume to be constant during the simulations:

    - The Power Train Moment of Inertia (hub + blades + gearbox + generator)

    - The air density

- Some interesting calculated variables:

    - The aerodynamic coefficient of the blade at that moment (Cp), dependent on the blade rpms, the wind and the pitch angle.

    - The power train acceleration (in real time).

In the next block, to  the right, data that are the result of the Simulation are presented:

- The rotation speed (RPMs) of the two shafts (generator and blades)

- The power being generated (and its power factor, uncorrected with any capacitor bank)

Further to the right we have the "START" and "STOP" buttons block.

- <mark style="background-color: green;">**START**</mark>: pressing it sends a *start-up request message (****cutin****)* to the Controller.

- <mark style="background-color: red;">**STOP**</mark>: pressing it requests the Controller to start the grid disconnection operation .(****cutout****)*

- The "**Turn left**" and "**Turn right**" buttons: to manually orient the Nacelle. These buttons are enabled only under the following conditions: there are no problems with the electrical power connection to the grid (that is, the main switch is connected, there are no reported incidents, and the Wind Turbine is not in Production).

- Further below we have the Wind indications and its Direction (entered in the [Nacelle Orientation and Wind synoptic (SynopticWindNacelle)](SinopticoOrientacionViento.md)), as well as the effective wind value, which, in the case of the figure is equal to the real one, since the nacelle is very well oriented. The nacelle orientation angle is also indicated: for this value one must take into account that each cable turn adds 360 degrees.

In the central part the signal values that are Controller inputs are presented:

- Whether the "*Power Train hydraulic brake*" is released.

- What type of generator connection is active.

- Whether there is any fault in the Three-Phase Grid Phases (F1,F2,F3)



This synoptic emulates the "[Control Terminal](Nuevotema4.md)" of a real wind turbine. Through it the machine start-up and stop are controlled, through the <mark style="background-color: green;">**START**</mark> and <mark style="background-color: red;">**STOP**</mark> buttons. In addition, it allows the manual orientation control ("**Manual yawing**").

Additionally it presents information about key variables and parameters in the machine operation.

- About the **Wind**: it gives the following information:

    - The **real wind speed**, measured by the anemometer, in m/s.

    - The **effective wind speed**, due to the nacelle misorientation respect to the wind direction. When this misorientation is 0 degrees, the two values coincide.

    - The **wind direction**, in degrees.

    - The **nacelle orientation**, in degrees. This value may be bigger than 360 degrees, as it also indicates the number of turns of the power cables. 

- **Generator** data:

    - **RPMs Generator** : revolutions per minute of the generator axis.

    - **Generated Power** : it is generating.

    - Its **(Electric) Power Factor**.

- **Power Train** data:

    - **RPMs blades**: revolutions per minute of the blades.

    - **Acceleration**: of the Power Train axis, in degrees per second squared.

    - **Cp** value, aerodynamic coefficient of the blade, under the current rpms and wind conditions.

- Parameters with which it is working:

    - Power Train Moment of Inertia (Hub, blades, gearbox)

    - Air density.

- Requested **blade angle** (**Pitch**) value.

- State of the **Generator connection** type: "Large gen", "Small gen".

- The **Thyristors** state and their **Bypass**.

- The **yaw motor** state "Turn left", "Turn right".

- The **brake hydraulic circuit pump** state.

- Whether there is voltage in each of the **grid phases**, "F1 F2 F3".

- The state of the gearbox low-speed shaft (**HCU**) and high-speed (**VCU**) **overspeed detectors**.

- The state of the "**Vibrations**" detector in the Tower.

Additionally this synoptic presents information on alarms, messages, etc., known in this simulator as "**Incidents**", both those that are "open", and those that have been recorded and have passed to historical "Incident history".
