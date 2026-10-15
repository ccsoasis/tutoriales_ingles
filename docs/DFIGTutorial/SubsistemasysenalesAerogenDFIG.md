# Subsystems and signals of a DFIG wind turbine

The following table presents a list of the inputs to the Controller of a DFIG wind turbine and of the units controlled by it, and the name of their variables.

| Sensors and inputs | Controlled devices and outputs |
|---|---|
| **Environmental**: Wind — Speed, Direction; Temperature | **Controller** + **Back-to-Back Converters** |
| **Electrical grid**: Phase-to-phase voltage; Current of each phase; Relative phase; Frequency | **Yawing motors**: CCW left-turn motors, CW right-turn motors |
| **Operations**: START, STOP; Active Power SetPoint; Reactive Power SetPoint | **Pitch angle** |
| **Other sensors**: Temperatures — Generator, Rotor bearing, Yawing motors; **Angular position** of the Generator rotor; Safety button; Nacelle orientation | **Cooling fans** |
| | **Main contactor** |
| | **Generator**: Rotor current and voltage; **Contactors**: Stator, Rotor, Crowbar, GSC |
