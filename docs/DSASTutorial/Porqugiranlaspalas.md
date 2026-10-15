---
tags:
- Cp
- wind
- pitch
- Betz
- tip speed ratio
- TSR
---

# Concepts about the extractable wind power

In ["Why do the blades rotate?"](PFAPorquegiranlaspalas.md) the basic concepts that allow understanding why the wind force perpendicular to the blade rotation plane makes them rotate are presented. One consequence is that that rotation force depends on the blade shape and also on their angle with respect to the rotation plane: the greater that angle (**Pitch**) (that is, the less blade surface "faces" the wind) the less that force will be.

The formula that gives us the extractable wind power is the following (see references in the [Bibliography](Bibliography.md)):

**ExtractedWindPower** =  
        0.5 \* **AirDensity** \* **BladeSweptArea** \* **Wind**<sup>**3**</sup>   \*  **Cp**(*Wind, BladeRotationSpeed, Pitch*)

Where **BladeSweptArea** is π \* **BladeRadius**<sup>**2</sup>, *BladeRadius* is the distance from the blade tip to the Hub center, and Pitch is the blade attack angle with respect to the blade rotation plane.

The *Pitch influence is through the* [Aerodynamic coefficient](Conceptossobrelapotencia.md) (**Cp**), which is a complex function whose theoretical maximum value is 0.59 (Betz law) and that depends:

- on the Wind,

- on the blade rotation speed and

- on the Pitch.

It is also seen that the Wind influence comes through the **Wind**<sup>**3**</sup> term, and also through the **Cp**.

The Cp function shape depends on the blade geometry, and, once a certain geometry is set, the value depends on three variables:

- 1.The wind speed.

- 2.The blade rotation speed.

- 3.The blade attack angle (Pitch).

Fortunately, these three variables can be reduced to two using the mathematical artifice of a variable that relates the wind speed with the blade rotation speed. This variable is known as ***TSR*** (from ***Tip Speed Ratio***: relationship between the blade tip linear speed and the wind speed).

The definition of this auxiliary variable is the following:

**TSR = 2 \*** π **\* BladeRadius \* (BladeRotationSpeed rpms****)/60) / WindSpeed**

Using this TSR variable, the Cp function remains dependent on only two variables: TSR and Pitch: **Cp (TSR, Pitch)**

In the following [sections](Conceptossobrelapotencia.md) significant data of this function are presented.
