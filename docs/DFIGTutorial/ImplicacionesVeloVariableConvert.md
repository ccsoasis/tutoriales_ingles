---
tags:
- synchronous speed
- slip
- DC link
- RSC
- GSC
- doubly fed induction generator
- full converter
- negative frequencies
- rotor side converter
---

# Implications for the Electrical Converter

**Implications for the electrical converter**

The mechanical-electrical conversion part of a variable-speed wind turbine must be able to operate under the conditions imposed by the Power Train control algorithms.

This means being able to operate in a speed range that has a ratio between the minimum and maximum value of around 2.

The configuration known as Doubly-Fed Induction Generator meets these requirements. This configuration is composed of an Electric Generator with a Rotor accessible through rings (see [figure](Vistasconstructivasdemaquinaselc.md)), whose stator is connected directly to the grid and whose rotor is connected to a Power Electronics set known as "[Back-to-Back Converter](ConvertidoresBackToBack.md)" (see following figure).

![](<lib/Formulario Generador Induccion doblemente ali.png>)

Figure 1.

The idea of this configuration is based on using a type of electric generator with a very proven technology and adding to it the Power Electronics equipment necessary to solve the problem of the operating speed range. To understand the problem it must be remembered that induction electric machines are characterized by a curve that relates the mechanical torque on their shaft with the speed of the same, shown in the following figure. In it it is seen that the behavior changes direction around a specific speed value: the *synchronous speed*. Above the synchronous speed the torque is negative, indicating that the machine will try to decelerate the shaft: that is, it works as an electric generator, whose output power will correspond to that value of the "opposing" torque. When it is positive (below the synchronous speed), the mechanical torque that it will apply to the shaft will try to accelerate the mechanical load connected to it, that is, we will have a motor.

![](<lib/MaquinaInduccionParvsRPMs2Puntos.jpg>) Figure 2

In the previous figure, the shaft rotation speed is represented by the variable "**Slip**", which is related to the speed through the formula:

"Slip" (= 1 - *CurrentSpeed* / *SynchronousSpeed*)

The Slip value for the synchronous speed is 0.

In the figure it can be seen that the relationship between the speed (slip) and the torque is linear in the vicinity of the synchronous speed, but in a very small range: in the case of the figure less than 5%. The synchronous speed is proportional to the frequency of the grid to which the stator is connected: for this reason an induction machine by itself is not usable for variable-speed wind turbines.

One possible solution is not to connect the stator to the grid: this solution exists on the market and consists of using an asynchronous machine, even a squirrel-cage one, whose stator is connected to a rectifier, which "charges" a capacitor (normally known as "**DC Link**"), which feeds a Power Electronic Converter, which is the one connected to the grid. In this way the synchronous speed can be made variable, according to the needs of the Power Train. However, this solution has the drawback of needing a Power Electronic Converter that must be able to manage all the power of the wind turbine. These wind turbines are part of the "**Full converter**" family. This is not the solution adopted in DFIGs.

In DFIGs the idea is to use the physical phenomena that occur in the induction machine so that the magnetic flux created in its air gap corresponds, in speed and phase, to the one corresponding to the stator, which is connected directly to the grid, regardless of the rotor shaft rotation speed. This is achieved by making the currents flowing through the rotor have specific frequencies and phases for each rotor shaft rotation speed and for each mechanical power applied to it. The main benefit is that the power electronic circuits to perform this functionality only require withstanding a power that is between 25% and 30% of the total power of the wind turbine, thus making it more competitive.

The key consists of <u>*complementing the angular speed of the magnetic flux created by the rotor currents*</u> so that the resulting flux has an angular speed identical to that of the flux created by the stator, which is connected directly to the grid. Any flux created by the rotor, since it is mounted on its shaft, which is rotating, has a "real" angular speed that corresponds to the mechanical speed of the rotor plus the one due to the frequency of the currents flowing through it.

Let us set an example: suppose we have a 50 Hz grid and a two-pole-pair generator. In this case, if the stator is connected directly to the grid it will create a magnetic flux in the air gap whose angular speed will be 1,500 rpms (= (50 Hz * 60 s) / 2 pole pairs). This speed, seen in the Power Train (in the blades) will be divided by the gearbox ratio. Let us assume a characteristic value, e.g. 90, for this ratio: the 1,500 rpms of the generator rotor shaft will correspond to 16.67 rpms (=1500/90) in the Power Train.

Let us now suppose that the Power Train control algorithm tells us that, for a certain wind, we need the Power Train to operate at 15.15 rpms. The Controller will take care of that by controlling the acceleration and the blade angle. When these desired rpms have been reached, the 15.15 rpms of the Power Train will correspond to 1,364.7 rpms (=15.15 * 90). If in this situation we fed the generator rotor winding with a direct current, the angular speed of the flux created by the rotor would be the one due to the angular speed of the Power Train, i.e. 1,364.7 rpms, different from the magnetic flux created by the stator: it is clear that this is not a situation that allows us to send power to the grid.

However, if instead of supplying direct current we supply the rotor with currents with a frequency of 2.253 Hz (value corresponding to the rpms difference, but measured in Hz [= (1500 - 1354.7) / 60]), then the angular speed of the flux created by the rotor will also be exactly 1,500 rpms. If in addition we can control the phase of these currents so that the flux created by the rotor goes somewhat ahead of the magnetic flux created by the stator, then it will "pull" the latter and this flux difference (note that it is only the phase) will create a current in the stator that will be sent to the grid, so that we will be generating power.

Another different situation can be with a higher wind speed, in which the Controller decides that the "appropriate" rpms for the Power Train control are, say, 20.26 rpms. This means that the generator rotor will rotate at 1,823 rpms [=20.26 * 90]. In this case we would have to apply rotor currents with a frequency of **-**5.383 Hz [=(1500 - 1823)/60]. How can negative frequencies be generated? In fact this expression refers to a "change of direction" of the magnetic flux rotation, i.e. what we have to do is to make the flux rotate in the opposite direction to the previous case. Fortunately this is very easy to do in a three-phase circuit: it consists of changing the connection of the grid phases. That is, if the three-phase windings of the induction machine rotor are connected to the grid phases in the "A", "B" and "C" sequence, the produced magnetic flux will rotate in one direction. If we connect these windings with the "A", "C" and "B" or "C", "B" and "A" sequence, the produced magnetic flux will rotate in the opposite direction: this is the equivalent effect of the negative frequency.

Assuming that in a DFIG we have the rotor connected to an electronic circuit, the above means that this circuit must be able to change the phase of the rotor currents. This case has another important implication: power must not be supplied to the rotor but rather taken from it, since part of the mechanical power applied to the rotor "comes out" through the rotor. This has important implications in the operation of the Electronic Converter that is directly connected to the rotor, which is known as *Rotor Side Converter* (see following figure), since, in this case, it must work as a rectifier that feeds the "intermediate storage" (capacitor in the figure, called "DC Link"). See a more detailed description in [Operating modes](ConvertidoresBackToBackModosFunc.md).

Figure 1 shows the DFIG connection and its Back-to-Back converters. These are named "Rotor Side Converter" (RSC) and "Grid Side" (GSC).

![](<lib/Formulario Generador Induccion doblemente ali.png>)

Figure 3

When the rotor delivers power (see figure 1) it is converted to direct current and stored in the **DC Link**. The GSC converter takes that energy and sends it to the grid. In this case the GSC acts as in the "Full converter" wind turbines.

When power must be supplied to the rotor (Figure 3) the RSC acts as a specialized power converter, since the currents it must inject into the rotor must have the frequency and have a specific phase shift that depends on the rotor speed and on the active and reactive powers. In this case the RSC is fed from the DC Link, which in turn receives power from the grid through the GSC, which, in this case, behaves as a controlled rectifier.

The "DFIGB2B" application allows exploring in detail the evolution of the rotor variables taking into account all the conditions: rotor speed, mechanical torque or mechanical power forced or evacuated by the rotor, grid voltage, desired active and reactive powers.
