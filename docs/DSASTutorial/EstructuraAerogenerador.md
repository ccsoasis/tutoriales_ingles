---
tags:
- anemometer
- bypass contactor
- controller
- disc brake
- grid
- pitch
- SCADA
- thyristors
- yawing operation
- control unit
- start of production
- exit production
- supervisory control and data acquisition
- control terminal
- operation and maintenance
- cutout
- stop
- cutin
- HAWT
- nacelle
- tower
- rotor shaft
- rotor bearing
- gearbox
- flexible coupling
- generator
- yaw mechanism
- wind vane
- hydraulic brake command system
- capacitor bank
- of the mechanical torque
- variable-pitch blades
- power factor
- autonomous
- misalignment
---

# Structure of a Horizontal Axis Wind Turbine

A horizontal axis wind turbine (known as ***HAWT*** in English) is an **electrical energy production plant** made up of a set of subsystems, located in: the Blades and the Hub, the nacelle, the Tower and the Foundation.

- The **Blades**, are fixed to the **Hub**. They may have the capacity to rotate along their longitudinal axis (*variable-pitch blades*).

- The **Hub**, which acts as a mechanical connection between the Blades and the Rotor Shaft. The Blades are connected to it, either through a fixed connection (fixed-pitch wind turbines), or with a platform that allows them to rotate on their longitudinal axis (variable-pitch wind turbines).

The ***nacelle*** is located on the **Tower**, on a platform that allows rotating in the horizontal plane. On this platform the following are located:

- The **Rotor Bearing**, which supports the weight of the Blades and the Hub, and from which the Rotor Shaft comes out.

- The **Rotor Shaft**, which mechanically connects the Hub with the Gearbox.

- The **Gearbox**: a fixed-ratio gearbox, with two shafts:

- an input or low-speed one, connected with the Rotor Shaft;

- and another, output or high-speed one, which connects with the Generator shaft through a **flexible coupling**.

The previous elements are known as "***Power Train***" (***DriveTrain*** in English).

- The ***Disc Brake***, generally located on the gearbox high-speed shaft (Generator side), although it also exists on the low-speed shaft (on the Power Train). It is used to:

- Keep the Power Train position fixed (immobile) when the wind turbine is being repaired.

- **Exceptionally**, as a Power Train brake mechanism.

- The ***flexible coupling*** that joins the gearbox high-speed shaft with the Generator shaft. This element solves the problems associated with the misalignment of these two shafts, and with the different mechanical stresses (abrupt wind changes, abrupt electrical load changes, etc.) that can occur. It usually also acts as a limiter of the mechanical torque that the Generator receives.

- The electrical ***Generator***. It can be of several types, and may have associated Power electronic devices.

In addition, there are auxiliary elements, such as:

- The ***yaw mechanism*** (***yaw*** in English), in charge of changing the nacelle orientation.

- The **orientation fixing mechanism**. This mechanism is a brake that prevents the nacelle from rotating horizontally, which occurs when it is misoriented with respect to the wind.

- The ***wind vane***, used to know the difference between the wind direction and the nacelle orientation.

- The **anemometer**, which measures the wind speed.

- The ***hydraulic brake command system***.

- The ***gearbox lubrication system***, which usually also includes an oil filtering and purification mechanism.

- **Fans** of the Generator and of the gearbox lubrication system.

- Several **sensors**:

- Of **temperature**: of the Generator, of the gearbox oil, of the rotor bearing, etc.

- Of **revolutions** measurement in the two gearbox shafts.

- Of **pressure**: in the brake hydraulic circuit.

The **power cables**, the ones that connect the Generator with the grid connection, located at the lower part of the Tower, fall freely for a certain distance, to then be attached to the Tower wall.

Depending on the wind turbine model, the nacelle may also contain:

- A **capacitor bank**, used to control the delivered *power factor*.

- The **step-up transformer** (from 690 V to medium voltage, typically 15 kV). This option has the advantage of decreasing the power cable losses, by decreasing the current through them.

From the point of view of the functional structure of a wind turbine we can distinguish the following aspects:

- All the mechanical, hydraulic, electrical **subsystems** that are located **in the nacelle** or in the Tower.

- The **Power electrical system**, including the Generator and the **electronic Power converters**, with their connection to the grid.

- The **Control Unit** (or **Controller**), which is an electronic subsystem that takes care that all the previous subsystems <u>work in a coordinated way</u>, according to **safety** and **energy conversion efficiency** criteria.  
For this, it receives information from a set of sensors associated with the mentioned subsystems, and emits signals that control certain components within those other subsystems.  
The Controller is responsible for the wind turbine working as an **autonomous production plant**: this is a differential characteristic with respect to other electrical production plants, which are usually attended by a team of local specialists. It is the wind turbine itself that, once it has received the "*production start*" (***cutin*** in English) order, checks whether the current wind, electrical grid, temperature, subsystem level, vibration, etc. conditions are adequate, and if they are, it starts the operation sequences necessary to connect to the electrical grid and deliver the produced energy according to the setpoint received from the customer. All this without needing any information from any external device.  
Similarly, when it receives the "*exit production*" or "*stop*" (***cutout*** in English) order, it triggers a sequence that ends disconnecting the wind turbine from the grid in an orderly way.  
The Controller can receive "orders" through two channels:

- Through a communications system, generally connected to a ***SCADA*** (**S**upervisory **C**ontrol **a**nd **D**ata **A**cquisition), and located in the Wind Farm itself or in a remote place.

- A local connection, through which what is known as "***Control Terminal***" is connected, a portable device used by the Operation and Maintenance personnel to know the wind turbine state and to send control commands.
