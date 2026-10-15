---
tags:
- normally closed
- normally open
---

# Contactor problem detection logic

The logic to detect the position of a contactor through two wires is to use an XOR function.

![](<lib/Funcion XOR.png>)

Fig 1

It starts from two contacts mechanically attached to the main contactors, which are represented in Fig 1 by the two contacts connected to the "NC" (from *Normally Closed*) and "NO" (from *Normally Open*) inputs, respectively.

The "*State*" signal that reaches the Controller, corresponding to the contactor *state*, is associated, in the scheme of Fig 1, with the "NC" input. There is another signal that also reaches the Controller (OK/Fault) that "*validates*" the "State" signal. This signal corresponds to the **XOR** logical function, applied to both signals coming from the Contactor.

The mechanical and electrical design of the NC and NO contacts is such that both signals must have *opposite values in normal operation*. The XOR function logic table is the following:

| **NC** | **NO** | **OK/Fault** |
|---|---|---|
| 0 | 0 | 0 |
| 1 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 1 | 0 |

The *OK/Fault* signal value, taking into account fault situations, are the following:

- 1.If +Vcc has no voltage, both NC and NO will have 0 volts → *State* = False   and *OK/Fault* = False

- 2.If the cables that join the contacts in the Contactor and the Controller are both broken, both NC and NO will have 0 volts → State = False   and OK/Fault = False

- 3.If only one of the two cables that join the contacts in the Contactor and the Controller is broken, then, *when a change occurs in the value of the one that is not broken*, both NC and NO will have the same value and therefore → *OK/Fault* = False
