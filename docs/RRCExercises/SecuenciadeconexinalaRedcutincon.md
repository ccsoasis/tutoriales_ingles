---
tags:
- cutin
- Nacelle.DriveTrain.PWMOut
- power vs slip graph
- start
---

# Grid connection sequence (cutin) with wind below the nominal

!!! tip "🎯 Cutin with wind below the nominal"
    ***Objective:*** Observe the complete grid connection sequence with low wind (6 m/s) and check that in this regime the RRC wind turbine behaves like a squirrel-cage generator (DutyCycle = 100%).
    ***What to observe:*** The signal evolution in the "General" recorder, the DutyCycle (PWM) value and the operating point position in the "Power vs Slip" synoptic (on the red line).
    💡 When the PWM is 100%, the IGBT is always in conduction: what effective resistance does the rotor present?

!!! warning "❓ Guiding questions"
    1. On which line of the "Power vs Slip" synoptic is the operating point located during the whole operation with 6 m/s? What does that mean?
    2. Does the DutyCycle (PWM) change at any moment during the cutin and stable production? Why?
    3. How does this cutin sequence differ from the one a conventional squirrel-cage generator (without RRC control) would carry out?

This practice consists of observing the key variable evolution when there are no incidents reported by the Controller and the wind is below the nominal.

You must proceed as follows:

- 1.In the "*Running* ..." synoptic, press "*Run*".

- 2.Set a **6 m/s** wind value in "*SynopticWindNacelle*".

- 3.Click on the "*Manual STOP*" incident box, in "*Control Terminal*".

- 4.In "*Control Terminal*" make sure the "Power vs Slip" synoptic is visible. Press the "*Power vs Slip Graph*" menu option.

- 5.In "Control Terminal" press the "**START**" button.

- 6.Observe the signal evolution in the "General" recorder until the production entry (cutin) occurs. You must have a record similar to the one in the following figure.

![](<lib/Clase.jpg>)

## Comments:

- The 2nd panel shows the Nacelle.DriveTrain.PWMOut signal evolution. This signal corresponds to the DutyCycle of the signal applied to the IGBT of the rotor resistance change mechanism. See details in [Control electronic circuit](../RRCTutorial/Circuitoelectrnicodelcontrol.md). The ordinate axis scale is logarithmic: this is because the evolution of this signal corresponds to the desired inverse resistance value (see [Most significant signal graphs](../RRCTutorial/Grficosdelassealesmssignificativ.md)) and this method is the best to observe the variations of this signal type. See [DutyCycle Graph](../RRCTutorial/Grficosdelassealesmssignificativ.md).

- Observe that the DutyCycle (PWM) value is always 100%, that is, the IGBT is always in conduction. Therefore this case is totally similar to using a squirrel-cage generator. Check it by observing in the "Power vs Slip" synoptic that the operating point (yellow point) is on the red line (equivalent to squirrel cage).

![](<lib/Pot vs deslizacion con 6 ms.jpg>)
