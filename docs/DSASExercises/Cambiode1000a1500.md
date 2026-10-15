---
tags:
- large generator
- generator connection change
- small generator
- electrical schematic
- electrical cabinet
- grid connection
- cutin
- connection mode
---

# Being in production, wind modification to change the Generator connection from Small to Large

!!! tip "🎯 Change from 1000 to 1500"
    ***Objective:*** Observe the mode change associated with the 1000 to 1500 jump and its impact on the control.
    ***What to observe:*** Target speed, control state and power response.
    ***What to note:*** Variable that triggers the change, state before/after and transients.
    💡 Note whether power peaks/drops appear during the transition.

!!! warning "❓ Guiding questions"
    1. How much time elapses in the generator/mode change from low wind (&lt; 6.2 m/s) to high wind (&gt; 7 m/s)?
    2. In which state does the system remain immediately after the change?

The objective of this practice is to familiarize the student with the electrical generator grid "connection mode" change concept, and the reasons why that functionality is necessary.

In this class we assume the wind turbine is connected to the grid (producing), with a wind that forces the use of the generator 6-pole connection (Small generator). See [Set the conditions for the Production entry with low wind to occur](CutinVientoBajo.md).

In this experiment we will raise the wind so that a generator connection change occurs, to 4 poles (Large generator): this wind must be above the "*Min for Large Gen*". See [Functional wind values](../DSASTutorial/DatosTecnicosValoresVientos.md). The minimum wind for this transition to occur is 6.6 m/s. Modify the wind up to, for example, 12 m/s using the "Page Up" keys (see step 7 in [Set the conditions for the Production entry with low wind to occur](CutinVientoBajo.md)).

In a recorder with the "Cutin + Cutout + Production" panel you will be able to observe the following signal evolution.

![](<lib/Pasode-6-a-12-ms.jpg>)

You can check that as the wind increases the generated power increases: this occurs until the wind exceeds (for a certain time at least) the 6.6 m/s speed. When this value is exceeded, the Controller starts a *generator connection change* operation, which will go from 6-pole connection (*Small generator*) to 4 poles (*Large generator*).

To do so it has to disconnect the generator from the grid: to do so it changes the blade pitch so that the generated power drops and deactivates the Thyristor Bypass Contactor. At that moment the generator shaft turning speed has dropped below the "Small generator" synchronous speed, which is 1,000 rpms. In this situation, generator disconnected, is when the generator connection mode change is made. This is done with the contactors that are reflected in the "Electrical schematic" tab of the "Electrical cabinet" synoptic. See the following figure.![](<lib/EsquemaElectrico-ArmarioElectrico.jpg>)

At that moment, the Controller begins a grid connection operation (cutin): it controls the pitch so that mechanical torque is extracted from the wind, which accelerates the power train; when the generator turning speed approaches the synchronous speed (now 1,500 rpms) the progressive Thyristor conduction opening occurs (see [Soft starter (soft connection) to the grid](../DSASTutorial/Softstarter.md)), which culminates with the activation of the Thyristor Bypass Contactors.

A notable characteristic of the simulated wind turbine is that it is capable of carrying out this operation in a very short time, of the order of 25 seconds. This is important due to the production loss it entails.
