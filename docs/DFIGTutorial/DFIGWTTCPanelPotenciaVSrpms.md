---
tags:
- operational working curve of the DFIG
- regions of operation
- operational curves of variable speed wind turbines
- mechanical power
- speed
- cutin
- cutout
- wind gusts
---

# Mechanical and electrical powers vs Rotor speed

## Power diagram as a function of the Power Train speed.

In addition to what is explained in [Implications of the desired behavior](Implicacionesdelcomportamientode.md), this panel presents the mechanical power extracted from the wind and also the electrical power delivered to the grid.

| ![](<lib/Potencia vs rpms espanol.jpg>) | <mark>Green lines</mark>: curves of the mechanical wind power as a function of the Power Train RPMs, for a given Wind value. (Note that these curves do not imply that the Pitch angle is constant but rather the adequate one to obtain the maximum in each case). <mark>Blue curve</mark>: curve formed by the points that guarantee obtaining the greatest wind power for each Power Train RPM value. Maximum Power Point Track (MPPT) algorithm. <mark>Red curve</mark>: desired operational curve for the Power Train control. Defined by points A, B, C, D and E, and a section of the MPPT curve. The vertical axis indicates the Power in pu's (per Unit). The horizontal axis indicates the Power Train rpms, also in pu's. Two powers are presented: the mechanical power extracted from the wind and the electrical power sent to the grid. The values are indicated in the numerical indicators and also through two icons. The numerical indicators can present their respective values in pu or real units. ![](<lib/DFIG PowervsRotor BotonesPUs.jpg>)![](<lib/DFIG PowervsRotor BotonesReales.jpg>) The icon ![](<lib/DFIG CruzPotenciaMecanica.jpg>) indicates the position of the mechanical power being extracted from the wind. The icon ![](<lib/IconoIndicadorPotencia.jpg>) indicates the electrical power being sent to the grid. Observing the evolution of the relative positions of these two icons is of great help to follow the wind turbine responses to operational changes. For example during wind gusts. |
|---|---|

The reasons for this panel are several:

1. First, to have a quick idea of the wind turbine situation in relation to the target situation (red curve).

2. Second, to allow easily following the evolution of the operating point in key cases, such as during the connection to the grid and start of production (*cutin*), or in the disconnection (*cutout*) or when there are wind gusts.

3. Third, to have a clear and simple vision of the relationship at all times between these two powers.

4. Fourth, to get an idea of the complexity of the implicit functions in the Power Train control, given the non-linear behavior of several of the subsystems, in particular the Cp calculation.

5. Fifth, to observe the position of the case of the electric generator operation at its synchronous speed. This point is very important to size the Back-to-Back converters. See [Operating modes](ConvertidoresBackToBackModosFunc.md).
