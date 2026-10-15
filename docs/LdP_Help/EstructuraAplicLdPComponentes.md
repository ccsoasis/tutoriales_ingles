# Basic components

An LdP application (Simulator) is defined by a description in a configuration file, in which:

- Each one of the components used in the Simulator is declared.

- The connections between the output and input signals of each one of the components are declared.

- Auxiliary elements are defined: parameter values, help, definition of graphic Recorder configurations, etc.

The "components" of an LdP configuration can be of the following types:

| **Processes** | This element can contain none, one or more "*Process*" type elements. Each one of these refers to a DLL developed specifically to simulate a certain aspect or subsystem. |
|---|---|
| **Synoptics** | This element can contain one or more "Synoptic" type elements. These elements refer to DLLs developed specifically using graphic indicators. They constitute the user interface. |
| **Connections** | This element contains "*InternalConnection*" type elements. These elements contain an "output signal" and one or several "input signals". |
| **Parameters** | This element contains none, one, or more "Parameter" type elements. Each of them has an associated "output signal" with a name associated with a Process or Synoptic. There is a base Synoptic ("Parameters") that allows you to access these "Parameters" and change the associated value. It is usually used to define parameters of algorithms implemented in the different "Process" and "Synoptic" elements. |
| **StripRecorders** | (*Recorders*) This element contains a set of "*Panel*" type elements, each one of which defines the content and format of "*Recorder*s" (*Record*), through which the set of signals that are presented and the form of the representation are defined. |
| **Functions** | Element that contains none, one or more "*Function*" type elements. Each one of these elements implements a "*formula*": each formula has an associated output signal and a set of input signals corresponding to the variables it uses. |
