---
tags:
- moment of inertia
- Nacelle.DriveTrainMomentOfInertia
- set as time reference
---

# Moment of inertia influence on the Power Train rpms evolution

!!! tip "🎯 Moment of inertia influence"
    ***Objective:*** Analyze how the system moment of inertia affects the rotor acceleration and deceleration.
    ***What to observe:*** Rotor speed evolution against wind or setpoint changes.
    ***What to note:*** Response time, transition smoothness and presence of oscillations.
    💡 compare scenarios with different moment of inertia keeping the other variables constant.

In this practice the "**moment of inertia**" concept is explored and experiments are carried out with changes in its value.

The "*moment of inertia*" physical concept applies to mechanical systems that *turn*, and is a concept analogous to "mass" in mechanical systems that move. It has to do with the resistance to the turning speed change of a mass that turns around an axis.

In the case of a wind turbine the Power Train set is the part with the highest moment of inertia, mainly due to the blades (which weigh tons). It can change due to a blade model change, or due to other events, such as, for example, ice deposited adhered to the blades.

In this practice we will see the influence of the moment of inertia value on the time the wind turbine takes to reach connection (cutout). To do so we will carry out experiments changing this value using the "*Nacelle.DriveTrainMomentOfInertia*" parameter. Access the "[Parameters](../LdP_Help/EstructuraAplicLdPParametros.md)" synoptic.

![](<lib/parámetro-momento-inercia.jpg>)

Fig 1.

### Experiment 1 - With the default value.

- 1.Make sure the wind turbine is disconnected from the grid.

- 2.Set a not very high wind (e.g., 9 m/s)

- 3.Present a recorder with the "Cutin + Cutout + Production" panel (see [How to present a Recorder and choose a predefined Panel in it.](../DSASTutorial/Comopresentarenprimerplanoundete.md))

- 4.Make sure there are no open incidents, except "Manual STOP".

- 5.Press "START". You will obtain an evolution similar to the one presented in the following figure.  
![](<lib/regist-cutin-9-ms-200ms.jpg>)  
Fig 1.  
If you press the "Copy" button another synoptic like the one shown in the following figure will appear. The main difference consists in that, in the latter, you have a procedure to "measure distances in time".  
![](<lib/regis-copia-9ms-200ms-cutin.jpg>)  
Fig 2.  
When moving the mouse over this synoptic, the blue line will move. You can fix the time origin at any point with the right mouse button: "*Set as time reference*".  
![](<lib/regis-copia-9ms-200ms-cutin-poner-ref-tiempo.jpg>)Fig 3.  
From that moment you will have an indication of the time distance between the point where the mouse is at that moment, and the point chosen as reference. See the following figure.  
![](<lib/regis-copia-9ms-200ms-cutin-medida-tiempo.jpg>)

- 6.Note that, in this case, the elapsed time is 45.6 seconds.

### Experiment 2: with a higher moment of inertia value.

Repeat experiment 1, but changing previously the moment of inertia to a higher value. With a 6000000 value, you will obtain the following signal evolution.

![](<lib/regis-copia-9ms-200ms-cutin-medida-tiempo-mas.jpg>)

In this case, the time from brake release to production is 59.6 seconds.
