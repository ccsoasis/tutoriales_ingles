---
tags:
- recorders
- active copies
- time base
- active copy
- recorder
- predefined panels
- seconds per pixel
---

# Synoptic Recorder

## Strip Recorders

The LdP interpreter includes the possibility of creating any number of "Recorder" type synoptics, which show the evolution of a set of signals. The representation is specified by associating the Recorder with a "Predefined Panel." These synoptics consist of:

- A *Record* of *time base* that moves to the left, as time elapses.

- One or more "***Records***", located immediately below the date indicator, where the following are presented:

- oThe evolution of one or more signals.

- oA vertical axis on the right, labeled according to the range of signal values. It can be linear or logarithmic.

- oHorizontal lines (*marks*) corresponding to certain values.

The signals in a Register must be of the same type, "analog" or "digital." Each signal can have a different associated color.

![](<lib/SR pitch potencias frenos rpms viento 0.png>)

- The "***Predefined panels***" button presents the set of Predefined panels for the Simulator that is running.

- The "***Seconds per pixel***" button allows changing the time base scale between the values presented in the following figure:

![](<lib/Time per pixel listado espanol.jpg>)

- The "***Copy***" button creates a synoptic called "[Active copy](DefinicindeRegistradores.md)" (hardcopy) that allows visualizing the signal evolution at a certain instant and performing time measurements between instants in a graphic way.
