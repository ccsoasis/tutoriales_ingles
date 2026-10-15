---
tags:
- brake disc
- fail-safe
- brake shoe
- hydraulic actuator
- pump
- valve
- pressure switch
- hysteresis
- hydraulic brake circuit
- brake valves
- brake circuit pressure
- brake released
---

# Brake system

| ![](<lib/Brakes hydraulic circuit.png>) Hydraulic brake circuit | ![](<lib/Circuito de frenos indicadores espaol.png>) Graphic indicators related to the brake circuit. They are in "presentation only" mode but can switch to "command" mode (F6). See their interconnection description in [Indicator connections](Algoritmodecontroldefrenosyseale.md). |
|---|---|

The hydraulic circuit is represented through a specific active graph, which includes:

- The ***brake shoe*** that presses against the brake disc.

- The ***hydraulic actuator*** that contains a spring to implement the "Fail/Safe" operation.

- A ***tank*** **with the oil** used in the hydraulic circuit.

- A ***hydraulic pump*** that allows maintaining the pressure in the circuit.

- A ***braking valve***, which serves to rapidly reduce the pressure in the circuit, so that the actuator spring forces the shoe against the brake disc and thus immobilizes it.

There is a set of graphic indicators where the signals related to this circuit are presented. These indicators can be put in "*command*" mode (accessible with the "F6" key) to simulate faults.

- **Pump state**: comes from the Controller. When put in command mode it directly controls the pump start/stop.

- The **state of the two brake valves** (the soft brake one is not represented in the previous graph). These signals come from the Controller.

- The **pressure switch state** of the hydraulic circuit. This device has hysteresis (different limit depending on whether the pressure is rising or falling): these two limits define the green zone in the lower clock. This signal is a Controller input.

- The "**Brake circ. pressure**" slider indicates the pressure, in % over the nominal.

- The **limit switch state** that detects that the distance between the shoe and the brake disc is sufficient for it not to be braked. It is indicated by the "**Brake released**" button. It is a Controller input signal.
