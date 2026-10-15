---
tags:
- slip
- synchronous speed
- mechanical torque
---

# Induction generators with variable Rotor Resistance

## Base characteristic

The following figure 1 shows the "*Mechanical torque vs Shaft rotation speed*" characteristic of an induction *machine*. (*Torque* = Mechanical torque)

![](<lib/RRC Torque vs Slip.jpg>) Fig 1

The abscissa axis shows the shaft rotation speed in *slip (****s****)* format with respect to the *synchronous speed*.

Cases:

#### s= 0

Corresponds to the **synchronous speed**. The mechanical torque is 0, that is, the shaft is rotating but has no mechanical load (negative torque), nor is there any external motor coupled (positive torque). As an example a machine with 2 pole pairs fed at 50 Hz would have a synchronous speed of 1,500 rpms (= 50 Hz * 60 seconds / 2 pole pairs).

#### s < 0

The shaft rotates at a speed below the synchronism one. There is a mechanical torque that is braking the shaft: the machine in this case is behaving as a *motor*, and transforms electrical energy that enters the stator into mechanical torque.

#### s = -1

The shaft is stopped.

#### s > 0

The shaft rotates at a speed above the synchronism one. There is a mechanical torque created by an external motor (the Power Train of a wind turbine, for example), which is transformed into electrical energy that comes out through the stator. The machine in this case works as a *generator*.

#### Rotor winding resistance influence

The following figure shows a detail of the previous figure centered on the generation zone, and using several cases obtained by varying the rotor winding resistance. *R1* corresponds to a value below all the others, and corresponds to the winding's own resistance.

![](<lib/RRC Familia curvas con R rotor y zona de inte.jpg>) Fig 2

We see that *the same power* (the one represented by the horizontal <mark>red line</mark>) can be obtained *at different speeds* (slips), simply by changing the rotor total resistance.

This idea is the one used to solve the criterion described in [Reasons for the development of Wind Turbines with Rotor Resistance control](RazonesparaeldesarrollodelosAero.md).

Our interest zone is the one marked in <mark>green</mark>, where we have set a slip limit (10% = 0.1).
