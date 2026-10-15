---
tags:
- wind gusts
---

# Wind gusts

The "*Wind gusts*" manager in this panel is accessible through the second menu option.

![](<lib/SynopticWindNacelle menu rafagas.jpg>)

Each entry in the dropdown menu allows access to the visualization and edition of a gust type. In the simulator installation a set of predetermined gusts is supplied.

The first of them corresponds to the wind evolution in a real wind turbine during 12 hours.

The ones named "*StandardGustXXX*" correspond to gusts where the wind follows a Gaussian bell type evolution, as shown in the following figures.

| ![](<lib/DFIG WindGust Def 120x4.jpg>) This figure corresponds to the gust from the **Standard124x4**.wgt file. The maximum change speed is 0.22 m/s/s | ![](<lib/DFIG WindGust Def 60x10.jpg>) This figure corresponds to the file Standard60x10.wgt. Maximum rate of wind change: 2.8 m/s/s |
|---|---|

The last option allows defining an additional gust profile: see [How to define gusts](Cmodefinirrfagas.md).

NOTE: the gust wind values are added to the wind value that existed at the beginning of its "execution".  
That is, if for example we have a wind of **7** m/s and we "force" the "StandardGust124x4" type gust that has a maximum peak of **4** m/s, the real wind value applied to the blades will reach **11** m/s.  
   
The gust can be stopped at any moment.
