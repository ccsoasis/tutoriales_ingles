---
tags:
- session
---

# Signal value logging (datalogging)

LdP records changes occurring in each of the Simulator signals in a database in a completely transparent manner. The temporal resolution of these records is 1 millisecond.

This recording is independent of any visible synoptic recorders.

Each "*session*" of each *configuration* (simulator) creates a database file. The name of said file corresponds to the session initial date and is found below a subdirectory whose name is the configuration. For example, the file "C:\\WFS\_Datalog\\*WFS\_SCADA*\\10-10-04-15-20-35.sqlite" corresponds to a session of the "*WFS\_SCADA*" simulator that began on October 4, 2010 at 15:20:35.

The files are "SQlite" type (see [SQLite org](https://www.sqlite.org/)) and their structure is described in [Structure of the registration databases](EstructuraAplicLdPDatalogEstruct.md).

These files are written at the end of the session, provided that the user responds affirmatively to the message that appears after clicking "Exit" and confirming the exit.

![](<lib/Salvar evoluciones en disco.jpg>)
