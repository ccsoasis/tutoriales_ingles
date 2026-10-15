# Details of the representation of magnetic flows in the Generator

![](<lib/Representacion DFIG con vectores y textos esp.png>)

The magnetic flow created by the stator coil rotates at a speed corresponding to the frequency of the grid, taking into account the number of magnetic poles of the Generator, and referring to the axis of the Power Train. That is, in case of this simulator that has a Generator with two magnetic poles, powered at 50 Hz and with a multiplier with relation to 1: 90, this speed is of

((50 Hz \* 60) rpms / 2 polos) / 90 = 16.67 rpms.

The magnetic flow created by the rotor coil, taking into account only the reflection of the excitement created by the RSC voltage, rotates at a speed corresponding to the frequency of that voltage. Green Vector.

| ![](<lib/DFIG sincrono.gif>) Modo sincrono | ![](<lib/DFIG subsincrono.gif>) Modo subsincrono | ![](<lib/DFIG supersincrono.gif>) Modo supersincrono |
|---|---|---|

The actual magnetic flow in the air gap due to the rotor rotates at a speed that is the sum of the previous speed plus the mechanical turning speed of the axis of the Potencia.Red Vector.

In production, the red vector "goes ahead" of the black vector.

NOTE: It is possible to change the "refreshment" speed of the real-time presentation of these vectors. Just press the right button on the above graph: this action presents the following form, where it is possible to change the refreshment interval (in milliseconds).![](<lib/DFIG PeriodoRefrescoVectores.jpg>)

The "DFIGB2B" application from ACMSL allows calculating the Generator signals. The "**Calculations for DFIG with ideal B2B**" application allows a complete polar representation of all these variables. See next figure. Notice the position of the vectors for Rotor Flux and Stator Flux.

![](<lib/DFIGB2Bv2 inicial solo principal.jpg>)
