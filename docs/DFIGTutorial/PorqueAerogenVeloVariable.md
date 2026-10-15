---
tags:
- wind gusts
- wind shear
- CL
- Cd
- lambda
- wind
- generator
- TSR
- subsynchronous
- electrical
- supersynchronous
- aerodynamics
- types of wind turbines
- pitch
- stochastic wind
- blade
- pitch rate
- torque
- tip speed ratio
- Cp
- Cpmax
- FACTS
- nominal wind
- nominal power
- Voltage-Fault-Ride-Through
- cutin
- cutout
- setpoints
- active power
- reactive power
- grid controllability
- controllability
- STATCOM
---

# Reasons for the use of Variable Speed Wind Turbines

In [Relationship between wind turbines and their location](Relacionentrelosaerogeneradoresy.md) some considerations are detailed that help to understand why DFIG-type wind turbines were developed. In fact, there is a predecessor of this technology, which is described in the tutorial of our "Rotor-Resistance-Controlled Wind Turbine Simulator", which also uses the concept of **variable-speed wind turbine**.

The main reason for the development of variable-speed wind turbines comes from the need for the **maximum exploitation of the power available in the wind over a wide range of wind values**.  
There are other achievements that justify the fact that DFIG-type wind turbines are really the most used currently in wind farms:  
- The improvement, with respect to other models, of the response to phenomena that cause high stress, such as *wind gusts*, wind speed differences along the height of the wind turbine (*wind shear*); the minimization of stresses on key components in normal operation, such as the blades, the tower or the power train.  
- The ability to accept *setpoints* for the *active power* and *reactive power*, which contributes to the controllability of the electrical grid to which they are connected.  
- Being able to make very smooth grid connection entries (*cutin*) and exits (*cutout*), which contributes to increasing the quality of the electrical supply, minimizing the stress on the grid and on the mechanical components of the wind turbine.

Other important improvements that have been incorporated into DFIG wind turbines are related to the behavior in relation to the electrical grid, especially the capacity, similar to other electrical production plants (thermal, combined cycle, hydroelectric), to withstand grid faults: this is known in the market as "**Voltage-Ride-Through**" capability. See [Grid fault tolerance capabilities (Voltage-Fault-drive-through)](RedElectricaExigencias.md).

In [Relationship between wind turbines and their location](Relacionentrelosaerogeneradoresy.md) we saw that it is convenient to divide the possible wind range into two: below and above the "**Nominal Wind**". Below, it is of interest that Cp is always the maximum, so that we extract the greatest power from the existing wind. Above, however, Cp must be adjusted so that the extracted power is "only" the one that can be sent to the grid, i.e. the "**Nominal Power**".

To achieve this, improvements have been necessary both in the manufacture of the wind turbine components and in the way of using them, so that they effectively behave as controllably as other electrical production plants.

The former has been achieved:

- By minimizing the stress on the blades, the tower and the power train when the wind turbine is in normal operating conditions.

- By minimizing the stress produced by environmental phenomena, such as gusts and non-uniform vertical distribution of the wind (wind shear).

The *controllability* as a production plant has been achieved after developing equipment that allows a smooth connection to the grid and an also smooth connection exit, and the ability to withstand common problems in the grid, such as the results of short-duration short circuits. Other added characteristics have been fundamental for the acceptance of wind turbines as desirable production plants: the ability to supply or consume reactive power, resulting from providing these equipment with Power Electronic Converters capable of functions similar to others used for the control and stability of the grid (for example STATCOMs).
