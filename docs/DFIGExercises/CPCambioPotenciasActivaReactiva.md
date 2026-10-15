---
tags:
- nominal power
- reactive power
---

# Desired Active and Reactive Power changes

!!! tip "🎯 Desired Active and Reactive Power changes"
    ***Objective:*** Explore the differential DFIG capacity to independently control the active and reactive power delivered to the grid, and observe how these changes affect the generator and B2B signals.
    ***What to observe:*** When changing the Active Power: evolution of the Pitch and of the point in "Power vs RPMs". When changing the Reactive Power: changes in rotor voltage and current (modulus and angle) without change in the Pitch.
    💡 The Reactive Power does not change the Pitch. Why? What parameter changes instead?

!!! warning "❓ Guiding questions"
    1. When reducing the Desired Active Power from 1500 kW to 800 kW, why does a small increase of the RPMs occur before stabilizing?
    2. When changing the Reactive Power to +400 kW, which B2B variables change and which do not? Why does the Pitch not change?
    3. What is the difference between the case of positive Reactive (+400 kW) and negative (-400 kW) in the rotor current and voltage?

One of the important differential characteristics of DFIGs is their capacity to set the generated active power (always below the Nominal Power) and, above all, to be able to set the reactive power delivered to or consumed from the grid. This last capacity is differential even with respect to other electrical energy sources and is one of the benefits of using the Back-to-Back converters.

The capacity to control the reactive power is highly valued due to its great contribution to guarantee the stability of the electrical system, so it has a significant price.

The simulator includes two linear controls in the Control Terminal (see [Control Terminal](../DFIGTutorial/TerminaldeControl.md)). The active power can be regulated (in this simulator) between 150 kW and 1,500 kW.

## Change of the desired active power

In the following graph the evolution of the wind turbine signals is presented when a relatively abrupt change of the desired active power is made from the Nominal (1,500 kW) to about 800 kW, with a wind above the Nominal. It can be seen that the wind turbine operating point changes by changing the Pitch, to reduce the mechanical power obtained from the wind.

![](<lib/DFIG SetPoint Active de 1500 a 800.jpg>)

Because priority is given to the command to lower the power delivered to the grid "as soon as possible", the mechanical power obtained from the wind follows the evolution of the power delivered to the grid with a certain delay, so that a small increase of the Power Train revolutions occurs.

It is very interesting to check the evolution of the operating point in the "Power vs RPMs" panel.

![](<lib/DFIG OpCuv limitacion a 800.jpg>)

In the "Power + Pitch vs Wind" panel it can be seen that the final Pitch is much higher than the expected one for the existing wind when there is no active power limitation.

## Change in the Desired Reactive Power

In this experiment, we set a wind above the nominal (e.g. 13 m/s) and remove the Desired Active Power limitation (that is, we set the corresponding control to 1500 kW), we observe the Pitch value (e.g. in the "*Control Terminal*" synoptic) and we present the "*Induction generator ...*" synoptic. We will obtain the following: Pitch = 1.5º and the values of the Generator and Back-to-Back signals as shown in the following graph.

![](<lib/Generador con 1500 KW y viento 13 - reactiva.jpg>)

NOTE: to change the presentation format of the variables do the following:  
1 - Press the label of each indicator: it will change to Modulus / Angle format.  
2 - Press the angle value: it will change from Radians to degrees (D).

### Case of reactive at +400 kW

Change the Desired Reactive Power value to (e.g.) +400 kW (go to the "<mark>Desired Reactive Power</mark>" control, select all the text by double-clicking with the left button, and type 400 followed by Enter) and observe that:

- The Pitch does not change:  
Reason: the Pitch controls the mechanical power extracted from the wind, which must not change because the active power sent to the grid has not changed.

- The following change:

![](<lib/DFIG con activa 1500 y reativa 400.png>)

### Case of reactive at -400 kW

If we change the Desired Reactive Power to (e.g.) -400 kW, the DFIG variables become the following:

![](<lib/DFIG con activa 1500 y reativa -400.png>)

The following change:

- The rotor voltage (only its magnitude, but almost nothing its angle)

- The rotor current (both the magnitude and the angle)

- The rotor power (both the magnitude and the angle)

- The GSC power.
