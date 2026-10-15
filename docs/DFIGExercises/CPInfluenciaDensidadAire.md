# Influence of the air density

!!! tip "🎯 Influence of the air density"
    ***Objective:*** Check how a change in the air density (parameter "Ambient.AirDensity") affects the wind turbine stable operating point and the Pitch value.
    ***What to observe:*** The displacement of the constant wind lines in the "Power vs RPMs" panel and the Pitch change when reducing the density from 1.225 to 1.15 g/m³.
    💡 With less air density, is more or less Pitch needed for the same power? Why?

!!! warning "❓ Guiding questions"
    1. When reducing the air density from 1.225 to 1.15 g/m³ with wind at 13 m/s, does the stable operating point (point D) change? How?
    2. Why is the new Pitch (0.048) lower than with the default density (0.057)?
    3. What practical implication does the air density have for the installation of wind turbines at high altitudes?

As explained in [Relationship between wind turbines and their location](../DFIGTutorial/Relacionentrelosaerogeneradoresy.md), the mechanical power obtainable from the wind depends on the air density. This experiment allows checking the changes that occur in the operating conditions of a variable-speed wind turbine (for example, a DFIG) when this occurs.

- Put the wind turbine in disconnection mode (press STOP if in production).

- Set the wind above the Nominal, e.g., 13 m/s.

- Press START.

- Observe that the production operating point (D) in the "Power vs RPMs" panel (upper left of "*Operational curves ..*") is approximately on the wind power line at 11 m/s.  
In the lower right panel the pitch, in this case, has a value of 0.057 (in pu's).

![](<lib/DFIG opCurva a densidad aire 1-225.jpg>)

- Change the "Ambient.AirDensity" parameter value from the default (1.225 g/m<sup>3</sup>) to 1.15 g/m<sup>3</sup> and observe that:

![](<lib/DFIG opCurva a densidad aire 1-15.jpg>)
