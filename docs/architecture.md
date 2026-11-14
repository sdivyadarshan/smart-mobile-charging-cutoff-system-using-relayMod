# System Architecture

The prototype has four functional subsystems:

1. **User input:** Trigger switch and timer-module buttons.
2. **Timing/control:** External digital timer relay module.
3. **Power switching:** Relay contact in series with the USB charger's positive conductor.
4. **Status indication:** LED indicators and active buzzer.

## Signal flow
The user selects a time interval. The trigger switch initiates the module's configured timing operation. The module controls its relay output, and the relay makes or breaks the phone-side USB +5 V path. LEDs and buzzer provide status feedback according to their wiring.

## Power domains
The USB charger supplies the phone. The timer module has a supply requirement of its own, which must be taken from the module's documentation. Do not parallel separate supply outputs. Properly wired dry relay contacts can isolate the control electronics from the switched load path.

## Control boundary
Timing is performed internally by the timer module. This version has no microcontroller firmware, phone app, battery telemetry, or battery-full sensing.

The timeout action depends on timer mode. Document the exact module model and measured output states before producing a detailed pin-level schematic.
