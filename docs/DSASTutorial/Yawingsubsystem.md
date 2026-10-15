---
tags:
- yawing operation
- yawing
- CW
- CCW
- orientation
- maximum turns
- wind vane
- wind direction
- nacelle orientation
---

# Yaw system

## Generated signals

In the "Nacelle" Process the following signals are created, corresponding to the elements in the nacelle that have to do with the wind turbine yawing:

- the simulation of the two motor blocks that allow the right (**CW**) and left (**CCW**) rotation.

- the simulation of the number of turns on themselves of the **power cables** that go down from the nacelle to the base of the Tower,

- the simulation of the limit switch that detects that the **maximum turns** have been reached.

- the generation of the **wind vane** signal, using the values of the **wind direction** (system input) and the **nacelle orientation**.

## Algorithms used

- To generate <mark>the nacelle orientation signal</mark> it is obtained taking into account:

- ○The state of the input signals that govern the yaw motor state: *SynopticWindNacelle.YawCCWOut*, and *SynopticWindNacelle.YawCWOut*. Normally they are signals that come from the Controller (*Controller.Yawing.YCCWOut*, and *Controller.Yawing.YCWOut*, respectively).

- ○The rotation speed values of each of the motors that enter through the signals *'Nacelle.Yawing.CWYawingSpeed'* and *'Nacelle.Yawing.CCWYawingSpeed'* and that are normally connected with the Parameters "*Parameter.NacelleYawing.CCWYawingSpeed*, and *Parameter.NacelleYawing.CWYawingSpeed*. In a real wind turbine these values are in the order of **0.5 degrees/second**. The recommended values, to favor the simulation experience, are in the order of **10 degrees/second**.

- ○The algorithm used integrates the time in which both signals are active to calculate the current position of the nacelle orientation.

- To generate <mark>the number of power cable turns</mark>.

- ○From the nacelle orientation, counting the times it crosses the North direction.

- To generate <mark>the digital signal of having reached the maximum number of power cable turns</mark>.

- ○Comparing the number of power cable turns with the Parameter "*Parameter.NacelleYawing.MaxCableTwist*" value.

- To generate <mark>the wind vane signal</mark>.

- ○Using the nacelle orientation and the wind direction.

![](<lib/Yawsystem.png>)

![](<lib/YawinMotor y rueda dentada desde la torre.jpg>)

![](<lib/YawingMotor sobre rueda dentada.jpg>)
