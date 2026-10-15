# Monitoring of the Generator and Back-to-Back Converters variables

!!! tip "🎯 Monitoring of the Generator and the Back-to-Back Converters"
    ***Section objective:*** Explore the relationship between the generator electrical variables and the Back-to-Back converters behavior in different wind and reactive power conditions.
    ***What to observe:*** How the stator and rotor active and reactive powers vary, the angles and moduli of currents, and the RSC power sign when crossing the synchronism speed.
    💡 In this simulator the GSC does not contribute reactive power: all the reactive "comes out" through the Stator. Keep this in mind when interpreting the B2B signals.

The Back-to-Back converters are a key component in the operation of a DFIG. The relationship between the Generator and the Back-to-Back is complex. In the following experiments the evolution of key signals will be explored to understand this relationship. See [Description of the Back-to-Back Converters](../DFIGTutorial/ConvertidoresBackToBack.md).

In the configuration of this simulator the Back-to-Back converters have a behavior without limitations and without losses, so that these relationships are presented more clearly.

Likewise, in the implemented Back-to-Back Control algorithm it has been decided that the GSC converter (the one that sends power to the grid when the working mode is supersynchronous) does not contribute Reactive Power, which is contributed/consumed only through the Stator. This is a common case, but not that of all DFIG wind turbine models.

In the first experiment the case of the evolution of these signals when there is a slow change of the wind speed is explored. That is, it allows having a diagram of the relationship of these signals with the wind in a quasi-stable situation.

In the second, the evolution against changes of the Desired Reactive Power will be observed.
