---
tags:
- brake
- brake disc
- pump
- pump flow rate
- VCU
- HCU
- emergency stop
---

# Overspeed mechanism parameters

| **Parameter** | **Use** |
|---|---|
| *Nacelle.GeneratorSpeedVCU* | This value establishes the maximum rotation speed the electric generator shaft can reach (in rpms), before the specific emergency stop protocol is started. |
| *Nacelle.RotorSpeedforHCU* | This value establishes the maximum rotation speed the blade shaft can reach (in rpms), before the specific emergency stop protocol is started. This emergency stop is started if the one relative to *Nacelle.GeneratorSpeedVCU* has failed and the power train keeps accelerating. |
