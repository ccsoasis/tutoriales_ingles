# Data recording

This simulator, being an LdP application, keeps in memory the evolution of the different signals exchanged between its sub-systems.

When leaving it, it asks if you want to save these evolutions to disk. See figure.

![](<lib/Pregunta para salvar las senales.png>)

If the answer is "Accept", a database file is created in the "c:\\WFS\_Datalog\\Wind Farm Simulator\\aa-nn-dd-hh-mm-ss.sqlite" directory where "aa-mm-dd-hh-mm-ss" corresponds to the date the session began.

"aa" is the year, e.g., "16" for "2016"; "nn" is the month, "dd" is the day; "hh" is the hour; "mm" is the minute: and "ss" is the second, of the beginning.

This database is explorable with various free tools. E.g. the following figure shows the description content of an example opened with the "DB Browser for SQLite" application.

![](<lib/SCADA tablas.png>)

Some of these tools have functionalities to generate graphs. For example, the following figure shows the evolution of the power produced by one of the wind turbines in a simulation session.

![](<lib/SCADA visualizacion evolucion tabla bbdd.png>)

These data are exportable in various formats (CSV, Excel, etc.) For a complete description see the "***Signal value recording (datalogging)***" section in the "[***Introduction to LdP***](../LdP_Help/Introduccion.md)" tutorial.
