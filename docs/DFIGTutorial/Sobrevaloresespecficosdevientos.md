# About specific wind values

### WindMaxForOperation:

Maximum wind compatible with production <u>without a time limit</u>. Typically in the order of 25 m/s.

Maximum value of sustained wind speed at which the WindTurbine will work continuously. Around 25 m/s. See WindMaxForTemporalOperation.

### WindMaxForTemporalOperation

Maximum wind compatible with production <u>with a time limit</u>. Typically in the order of 28 m/s with a maximum of 10 minutes.

Maybe in a gust of wind, the wind exceeds WindMaxForOperation but not maintained continuously. The WindMaxForTemporalOperation value is a higher value than WindMaxForOperation but lasting less than a certain period of time, typically 10 minutes. If it lasts longer, the turbine is switched off (cutout). Typically 28 m/s.

### WindAbsoluteMax:

Absolute maximum wind: wind above which, if the generator is in production, a normal disconnection is carried out immediately (cutout).

### WindMaxForCutin

Maximum wind to start the stator grid connection operation (cutin). Typically in the order of 20 m/s. The criterion for applying this limitation consists of assuming that if the wind is so high before the connection, there are great possibilities that after entering connection (production) the WindMaxForOperation value will be reached quickly, which would mean having to stop.

For this limitation to come into operation, the wind must be higher than this value (WindMaxForCutin) for a long period of time (i.e. it cannot come from a gust).

### WindMinForAutomaticYawing

Minimum wind for Automatic Yawing: below this wind the Controller does not take into account the nacelle misorientation. This is a very low limit (between 2 and 3 m/s), lower than WindMinForCutin.

### WindMinForCutin

Minimum wind that the Controller considers to start the grid connection operation. Typically between 4 and 6 m/s.
