# Legend of the Security State Machine Diagram

**States of the Security State Machine**

| **Name** | **Description** | **Associated value** |
|---|---|---|
| SS0BypassOn |  | 1 |
| SS0BypassOff |  | 2 |
| SSWRpms0 |  | 3 |
| SSW4Idle |  | 4 |
| SSWToutHBrake |  | 5 |
| SSWToutSBrake |  | 6 |
| SSW4RBelowSynch |  | 7 |
| SSDecideBelowSynch |  | 8 |
| SSDecideAfterIdle |  | 9 |

**Events of the Security State Machine**

| **Name** | **Description** | **Associated value** |
|---|---|---|
| ESS1 | Stop Sequence 1 | 1 |
| ESS2 | Stop Sequence 2 | 2 |
| ESS3 | Stop Sequence 3 | 3 |
| ESS4 | Stop Sequence 4 | 4 |
| ESS5 | Stop Sequence 5 | 5 |
| ESRpms0 | RPMs arrived to 0 | 6 |
| ESSBTout | SoftBrake timer Time Out | 7 |
| ESHBTout | HardBrake timer Time Out | 8 |
| ESRBelowSynch | RPMs dropped below synch value | 9 |
| ESRIdle | RPMs dropped below Idle value | 10 |
| EBypassOn | Bypass connected | 11 |
| EBypassOff | Bypass disconnected | 12 |
| ENoIncidencesPending | No incidences pending | 13 |
| ED2Idle | Going to idle state | 14 |
| ED2SBrake | Going to stop by softbrake | 15 |
| ED2HBrake | Going to stop by hardbrake | 16 |
| ED2SS0BpOff | Going to Bypass off | 17 |
| ED2SS0UntwistCables | Untwisting cables | 18 |
