---
tags:
- digital
- states
- date
---

# Structure of the registration databases

The structure of the databases used to record the evolution of signals in a simulation is as follows:

- They are contained in a single file created with the SQLite 3.6 database engine.

- It has a table per signal, whether "output" or "input".

- Each table contains two fields that depend on the signal type (analog or digital). One of these fields ("*Date*") is common. See the following details:

- oFor the **analog signals** the fields are:

| **Field name** | **Field type** | **Description** |
|---|---|---|
| Date | Numeric (double) | Instant of change or sample with millisecond resolution. |
| ValueA | *Numeric* (single) | Value of the associated signal at the moment of Date |

- oFor **digital signals** the fields are:

| **Field name** | **Field type** | **Description** |
|---|---|---|
| Date | Numeric (double) | Instant of change or sample with millisecond resolution. |
| ValueD | *Boolean* | Value of the associated signal at the moment of Date |

The "*Date*" field values correspond to the date and time with millisecond resolution. The conversion formula is the following:

Instant = (DateFieldValue)/86400000 - 693593

Examples
