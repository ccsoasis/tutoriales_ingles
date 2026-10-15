# Wind Farm data recording

The data received by the SCADA are stored in a database or in sequential files with date indication.

In a Wind Farm the **SCADA data sources** are:

- From each one of the wind turbines:

    - Environmental variables (wind, wind direction, ambient temperature)

    - Electrical variables: active power produced, power factor.

    - Incidents reported by the Controller

- From the Meteorological Tower:

    - Ambient temperature.

    - Ambient humidity

    - Atmospheric pressure.

    - Wind (at two heights)

    - Wind direction

- From the electrical Substation:

    - Official measurement of the active power produced and the power factor.

    - Substation operation incidents.

In the Simulator, any variation in any of the signals is recorded. This recording is made in memory. When leaving the Simulator, the program asks if you want to save the in-memory data in a database. If the answer is positive, an SQLite type database is created, consisting of a file created in the "**C:\\WFS\_Datalog**" subdirectory. Below this directory a directory is created per Simulator type. Below each one of these "Simulator type" subdirectories a database is created whose name corresponds to the instant the Simulator was executed. For example: the file  
'*C:\\WFS\_Datalog\\Wind Farm Simulator\\22-02-05-13-40-21.sqlite*' corresponds to the session record of the "*Wind Farm Simulator*" that *began* on "(20)23-02-05-13-40-21"

The structure of these databases is described in detail in the **[tutorial](../WFSSCADA/Datalogging1.md)**. For each "internal signal" in the Simulator (see the ["Data Recording"](../WFSSCADA/Datalogging1.md)), the created database contains a table with two fields "*Date*" and "*Value*". In the case of *analog signals* the second field is called "*ValueA*", and "*ValueD*" if it is *digital*. These databases can be accessed through several "open-source" programs (examples: "*DB Browser for SQLite*", "*SQLiteBrowser*", etc.). In general, these programs offer functionalities to present the data in tabular form, or in plot form. Also to **export their data to other formats**, such as spreadsheets, CSV files, etc., for later analysis.
