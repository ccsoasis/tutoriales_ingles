---
tags:
- brake
---

# Brake system

The brake system is simulated using the following criteria:

- Modification of the brake circuit pressure according to:

- ○the pump state.

- ○the discharge valve state.

- ○the circuit loss level.

The associated parameters are:

| **Parameter** | **Use** |
|---|---|
| *NacelleBrake.PumpCaudal* | Determines the pump flow rate, in percent with respect to the nominal pressure, per second. |
| *NacelleBrake.LeakageBrakeHydrCircuit* | Used to simulate the total pressure losses due to the hoses, the hydraulic connection elements, the pump tightness losses, etc. Measured in flow rate with respect to the nominal pressure per second. |
