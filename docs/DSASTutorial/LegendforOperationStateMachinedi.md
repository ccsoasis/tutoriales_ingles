# Legend of the Operation S.M. Diagram

LIST OF NAMES USED IN THE OPERATION STATE MACHINE.

STATES:

| **Name** | **Short name** | **Description** | **ID** |
|---|---|---|---|
| SSTOPSM | SSTOPSM | Entry State. Also resting state after StopSequence received | 16 |
| St | St | Testing wind speed | 1 |
| sB | sB | Decision point for connection on 6 (Small) or 4 (Large) poles | 2 |
| SPrepare4CutinLarge | SPreCutinL |  | 3 |
| SPrepare4CutinSmall | SPreCutinS |  | 4 |
| SW4BrakeReleased | SW4BrRelea | Waiting for brakes released | 5 |
| SG2Cutin | SG2Cutin | Going to Cutin | 6 |
| SThyristorsON | SThyrON | Thyristors fired | 7 |
| SGG | SGG | Stable production at Large connection | 8 |
| Sg | Sg | Stable production at Small connection | 9 |
| SGSmall2Large | SGS2L | Changing from Large to Small connection | 19 |
| SGLarge2Small | SGL2S | Changing form Small to Large connection | 10 |
| SGoingSt | SGoingSt | Going to testing for wind speed | 17 |
| SUntwistingCables | SUntwiCabl | Untwisting power cables | 15 |
| SW4Idle | SW4Idle | Intermediate state going to stop | 18 |
| SG2Down980 | SG2D980 | Intermediate state going from Large to Small connection | 11 |
| STestTwistedCables | STTwisCabl | Test if cables must be untwisted before cutin | 14 |

EVENTS

| **Name** | **Short name** | **Description** | **ID** |
|---|---|---|---|
| ENoErrors | ENEr | The SequenceSTOP State Machine reported no errors | 2 |
| EUntwistCables | EUnTwist | The power cables must be untwisted | 19 |
| ESTOPSeq | ESTOP | A SequenceSTOP started | 1 |
| EInsufficientWind | EInsufWind | Wind is not enough for Cutin | 10 |
| EStart | EStart | User pressed the "START" button | 5 |
| EEnoughWind | EEnoughWind | There is enough wind to start cutin | 9 |
| EEnoughWind4Large | EEnough4L | The wind is enough for 4 poles connection (Large) | 11 |
| EWOnlyForSmall | EWOFSmall | The wind is enough only for 6 poles connection (Small) | 12 |
| EWindOverMaxForCutin | EWOM4Cutin | The wind is too high for trying a cutin | 21 |
| EToutBrakeReleased | WTOBRel | Timeout of the BrakeReleased timer | 7 |
| ECrossedCutinRPMs | ECrosCutin | The RPMs crossed the limit for cutin (1000 for Small and 1500 for Large) | 8 |
| EBypassOnLarge | EBypassL | Bypass on with generator in Large connection | 3 |
| EBypassOnSmall | EBypassS | Bypass on with generator in Small connection | 4 |
| EWCrossedLarge2Small | EWCrossL2S | The wind speed (decreasing) crossed the limit for changing from Large to Small connection | 13 |
| ERCrossedBelowSynch | ERCrossBSyn | The RPMs crossed (going down) the synchronous speed (1000 or 1500) | 14 |
| ERCrossedBelow1500 | ERCrossB1500 | The RPMs crossed below Large connection synchronous speed | 16 |
| ECablesUntwisted | ECableUntd | Cables now untwisted | 18 |
| ERBelowIdle | ERBelwIdl | The RPMs crossed (decreasing) the value for entering Idle state | 17 |
| ERPMsBelow980 | ERpmB980 | The RPMs crossed (decreasing) the value for changing to Small | 15 |

Actions
