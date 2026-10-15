---
tags:
- recorder
- sampling rate
- open incidents
- main switch
- manual stop
- recovered
- incident history
- approval
- locate the synoptic
- Page Up
- Page Down
- Up arrow
- Down arrow
- wind direction
- change the wind
- Left turn
- Right turn
- effective wind speed
- control terminal
- VeloEficVien
- run
- nominal power
- nominal wind
- start
- blade rotation speed
- generator shaft rotation speed
- nacelle orientation
- hydraulic circuit pressure
- pump
- brake release
- pitch
- wind speed
- thyristor bypass contactor
- grid connection
- cutin
- Gen. Grande
- Gen. Pequeño
- functional analysis
- unwinding
- power cables
- brake mechanism
- power train
- synchronous speed
- small generator
---

# Set the conditions for the Production entry with low wind to occur

!!! tip "🎯 Cut-in with low wind"
    ***Objective:*** Identify the wind speed condition that allows starting the generation.
    ***What to observe:*** Wind speed, system state and transition from stop to operation.
    ***What to note:*** Approximate wind value at the start instant and subsequent evolution.
    💡 observe whether there is hysteresis between stop and start.

!!! warning "❓ Guiding questions"
    1. How much time elapses from pressing **Start** (in grid disconnection state) until the **grid connection** and the production start? Measure two cases:
        - Low wind (for example 6 m/s).
        - High wind (for example 14 m/s).

The objective of this practice is to familiarize the student

- with the different available synoptics.

- with the creation of the necessary conditions for the wind turbine to go from stopped to production.

- 1.Make sure the simulation is running: in the "*Running Simulator* ..." synoptic press "**Run**".

- 2.Observe that the Pitch angle goes to -90º. You can check it in the Power Train synoptic  
![](<lib/Vista3D90grados.png>)  
![](<lib/Hubcon90grados.png>)  
Also in the "WindNacelle" synoptic:  
![](<lib/WindNacelle90grados.png>)  
And in the "Control Terminal" synoptic:  
![](<lib/ControlTerminal-Pitch-90.png>)

- 3.Check in the "Electrical cabinet ..." synoptic that the "*Main switch*" is connected. See the following figure:  
 ![](<lib/ArmarioElectricoConectado.jpg>)![](<lib/DSAS MainContactor.jpg>)  
Fig. Detail of the "*Main switch*"

- 4.In the "Control Terminal" synoptic check that in the "*Open incidents*" tab there are no incidents that must be acknowledged (except "*Manual STOP*").  
For example, if you have 'run' the simulation and the "Main switch" was not connected, the Controller will detect the lack of main electrical supply and will report some incidents like the ones shown in the following figure, noting the date they were detected (year-month-day hour:minute:second,millisecond):  
![](<lib/ControlTerminal-espanol-con-incidencias-inici.jpg>)  
  
If you change the "Main switch" to 'On', at which moment, the Controller will detect that the conditions that produced the incidents have disappeared, and will note the instant it occurs in the column titled "*Recovered*". See the following figure.  
![](<lib/CT-espanol-con-incidencias-restauradas-detall.jpg>)  
  
This type of incidents require being *'acknowledged'* by the operator: to do so you must check (with the mouse) the "Ok" column box of each one of them (first two items in the previous figure). When you do it you will see they disappear from the *'Pending incidents'* list and will pass, automatically, to the "*Incident history*" tab list, as shown in the following figure:  
![](<lib/CT-espanol-historial-incidencias.jpg>)  
  
This list collects the record that the Controller itself maintains of the incidents that have been occurring. In other practical classes you will see that there are incidents that do not need to be 'acknowledged' by the operator: that is, the Controller will continue the execution of the planned 'protocol' when the incident conditions have disappeared, without requiring the operator to acknowledge it.

- 5.In this situation, the 'Open incidents' list must show only "Manual STOP", as in the following figure:  
![](<lib/CT-espanol-solo-ManualSTOP.jpg>)  
  
The Controller is in a situation to receive the "START" order. *In this particular Controller type*, the (manual) order from the Control Terminal must be preceded by the operator's 'approval', for which you must check the box corresponding to the "Manual STOP" line in the previous list. See the following figure.  
![](<lib/CT-espanol-ManualSTOP-checked.jpg>)  
  
Note that the 'acknowledgment' of this incident is not reflected in the 'Incident history'.  
From this moment, the Controller is available to receive the 'manual' "START" order.  
If you press the "START" button the wind turbine evolution will depend on the wind speed. Before pressing it:

- 6.Make sure you have visible a "Recorder" where the "Predefined panel" named "Cutin + Cutout + Production" is presented, as shown in the following figure. See [How to present a Recorder and choose a predefined Panel in it.](../DSASTutorial/Comopresentarenprimerplanoundete.md)  
![](<lib/RegistradorCutinCutoutProduccion.jpg>)

- 7.
    Change the wind speed to 6.0 m/s. This is a low wind value: the simulated wind turbine generates a 1,300 kW nominal power at a nominal wind of around 12 m/s. A 6 m/s wind is below the "Max. for Large Generator" wind (See [Functional wind values](../DSASTutorial/DatosTecnicosValoresVientos.md)), so we know the Generator 6-pole connection will be used (Small generator).  
To do so, locate the "SynopticWindNacelle" synoptic (See [How to present a certain synoptic in the foreground](../DSASTutorial/SinpticodelTerminaldeControl.md))
      
In this synoptic place the mouse over the wind indicator (white background part). See the following figure.  
![](<lib/Viento-dirección-13.jpg>)  
  
You can change the wind in two ways:

- 1.**Typing** directly the desired value.  
Note that when you change the value, the background changes to yellow until you press the "Enter" key on the keyboard. If you want to abort the change, before pressing "Enter", you can press the "ESC" key (top left of the keyboard).

- 2.**Using the** "*Page Up*", "*Page Down*", "*Up arrow*" and "*Down arrow*" keys.  
This is the preferred method and allows changing the value in 1 m/s steps (Page Up / Page Down) or in 0.1 m/s steps (Arrows).  
<mark>This is the preferred method</mark> because it limits the wind change speed to reasonable values, while in method 1, these changes can be very abrupt.

- 8.You can take advantage to change the wind direction, using the same procedure on the "*Wind direction*" indicator.

- 9.Press the "START" button and observe the evolution of the following signals in the recorder and in the different synoptics.

- 1.**Blade rotation speed:** in SynopticDriveTrain, Control Terminal and Recorder.

- 2.**Generator shaft rotation speed**: in Control Terminal and Recorder.

- 3.**Nacelle orientation**: in SynopticWindNacelle and Recorder.

- 4.**Hydraulic circuit pressure**, **pump** operation and **brake release**: in SynopticDriveTrain and Recorder

- 5.The **Pitch** angle: in SynopticDriveTrain (both in the 'Internal view' and in '3D view'), in Control Terminal, in SynopticWindNacelle and Recorder.

- 6.**Wind speed**: in SynopticWindNacelle, in Control Terminal and Recorder.

- 7.The **Thyristor Bypass Contactor** state (grid connection): in Electrical Cabinet (internal view), in Control Terminal and Recorder.

- 10.You will obtain a signal evolution in the recorder similar to the one presented in the following figure:  
![](<lib/Registrador-con-cuitn-a-6ms.jpg>)

- 11.You can check that, after some time (a few seconds) after pressing START, the Controller drives the orientation motors ("*Left turn*" and "*Right turn*") until the Nacelle orientation 'appreciably' coincides with the indicated wind direction, but not exactly. This is because the Controller assumes that there is a certain uncertainty in the wind direction measurement, and that, on the other hand, moving the Nacelle 'requires' energy and therefore has a cost. The result is that if the error between the 'measured' wind direction and the Nacelle orientation is within a certain margin, it 'decides' that it is oriented.  
The value of this margin in the simulator is exaggerated for didactic purposes.  
Likewise the Nacelle turning speed in the simulator is not realistic, although this is a value that can be changed, even during the simulation execution, using the *NacelleYawing.CWYawingSpeed* and *NacelleYawing.CCWYawingSpeed* parameters. The default value is 10 degrees/second, while in reality this value is around 0.5 degrees/second.

- 12.The "**Effective Wind Speed**" concept.  
This value corresponds to the value of the *wind that is frontal to the blade turning plane*, that is the wind that effectively serves to make the blades turn.  
If the wind turbine is not oriented, this value corresponds to the product of the real wind speed multiplied by the cosine of the misalignment angle. It corresponds to the red vector in the following figure.  
![](<lib/Viento-eficaz.jpg>)  
  
This effective value is presented in the "**VeloEficVien**" indicator of the "*Control Terminal*" synoptic. When the Nacelle is oriented, this value coincides with the wind speed value. This can be checked in the evolution of both values in the recorder figure, in the last channel, where it is seen that they converge on the same value when the Nacelle is oriented.

- 13.**Functional analysis of the event sequence during the grid connection operation** (cutin):

- 1.If the Nacelle is not oriented to the wind, it starts the orientation operation. It may need to previously carry out a power cable unwinding operation.

- 2.The Controller, from the wind value measurement, *decides* that the generator, which has two possible connections (corresponding to stator windings at 4 or 6 magnetic poles, "**Gen. Grande**" and "**Gen. Pequeño**" respectively), is going to be connected with 6 poles ("Gen. Pequeño"). In this case the *synchronous speed* is 1,000 rpms.

- 3.The Controller, before starting the operation itself, decides to check the brake mechanism situation (shoe state, spring, etc.). To do so it activates the brake, while placing the blade Pitch at a value at which it knows the wind produces a mechanical torque value on the blades sufficient for this check.

- 4.If everything goes well it proceeds to release the brakes: to do so it closes the hydraulic circuit valve and starts the pump.

- 5.The power train begins to accelerate.

- 6.The Controller monitors the power train acceleration value, and acts on the Pitch (which is the acceleration source) so that this value is kept below a certain level.

- 7.When the generator speed approaches the synchronous speed, the Controller activates the Thyristors. The Thyristor conduction angle follows a pattern of starting with little conduction angle until total conduction after a few seconds (typically 2 to 4 seconds).  
See the animation in [Soft starter (soft connection) to the grid](../DSASTutorial/Softstarter.md).

- 8.When the total Thyristor conduction is reached, the Controller activates the Thyristor Bypass Contactors, which short-circuit them: in that situation there is no current passage through the Thyristors and they deactivate. The wind turbine is in Production.
