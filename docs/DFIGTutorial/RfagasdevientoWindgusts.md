---
tags:
- pitch
---

# Wind gusts (Wind gusts)

DFIG wind turbines are designed to have good behavior when the wind shows wind gusts. This simulator allows using wind evolution files, of which the installation includes the ones shown in the following figure, which are accessed through the "Wind gusts" menu option.

![](<lib/Menu rachas de viento.jpg>)

These files have the "\*.wgt" extension and must be in the subdirectory "*\[InstallationDirectory\]\\WindFarmSimulator\\windgusts*". The displayed title coincides with the name of the corresponding file. The format of these files is described in [Wind profile creation](Creacindeperfilesdeviento.md).

The wind gust files included in the installation are particular cases of the standardized curve corresponding to the formula:

![](<lib/WindGustStandardFormula.png>)

In the following graphs two of them are shown. The abscissa axis corresponds to time, in seconds, and the ordinates to the *additional wind*.

| ![](<lib/DFIG WindGust Def 120x4.jpg>) This figure corresponds to the file "*Standard124x4.wgt*". The maximum wind rate of change is: **0.22 m/s/s** | ![](<lib/DFIG WindGust Def 60x10.jpg>) This figure corresponds to the file "*Standard60x10.wgt*". The maximum wind rate of change is: **2.8 m/s/s** |
|---|---|

The nomenclature used to name these wind gusts is determined by the two numbers: in "StandardGust100x4" the temporal extension is 100 seconds and the amplitude is 4 m/s.

![](<lib/Menu rachas editar.jpg>)

When one of these gust files is selected there are two possible functionalities:

- "*Edit*": Visualization and eventual edition of its values.

- "*Force*": Forcing of the total applied wind. The wind changes as time passes and its value at all times corresponds to the wind at the start of pressing "Force" plus the wind of the file corresponding to the time elapsed since that moment.

In the "Edit" mode a form appears that contains two panels:

![](<lib/Menu rachas vista en edicion.jpg>)

If you right-click, a submenu appears with the following two options:

![](<lib/Edicion racha viento 1.jpg>)

If the option "Adding a new point to the Profile" is chosen, the following synoptic appears in which we can enter the data of the new "point" (time instant and wind value for that instant).

![](<lib/Edicion rachas anadir punto.jpg>)

The new value is entered into the table, which is sorted by increasing time instant. The graph is also refreshed with the new values.

## Manual creation of a profile

A new wind gust "profile" can be created using the "(new)" item by clicking on "Wind gusts".

To add a new wind gust profile you have to select "(new)". You will be prompted with the following form:

![](<lib/WindNacelle add profile.jpg>)
