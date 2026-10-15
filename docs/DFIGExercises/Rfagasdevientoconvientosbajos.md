# Wind gusts with low winds

!!! tip "🎯 Wind gusts with low winds"
    ***Section objective:*** Explore the DFIG behavior against wind gusts when the average wind is low (below the nominal), comparing the effect of slow gusts (active MPPT) and rapid ones (Pitch comes into play).
    ***What to observe:*** How the Power Train inertia dampens slow gusts, the interaction between the Power Train Controller and the B2B, and when the Pitch begins to act.
    💡 In which type of gust (slow or rapid) does the Pitch remain practically constant? Why?

In this class the objective is to observe the influence of wind gusts on the Power Train and on the generated Electrical Power when the average wind is low.

As expected, when the gusts have a reasonably slow evolution, the wind turbine response "follows" the wind evolution with a certain delay, due to the Power Train inertia, but reproducing its shape. You can change the parameter that determines this inertia (Moment of Inertia: "*Nacelle.DriveTrain.MomentOfInertia*") to check it.

When the gust evolution is faster, changes occur in the powers that do not exactly follow the wind gust evolution. This is due to the interaction between the Power Train control mechanisms and the Back-to-Back converters. The power waveforms do not entirely follow the shape of the wind evolution.
