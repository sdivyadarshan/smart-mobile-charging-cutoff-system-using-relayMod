# Wiring and Connection Notes

This is a functional wiring guide, not a terminal-by-terminal schematic. The exact timer relay model and its terminal labels have not yet been recorded.

## Phone charging path
- Use a regulated 5 V USB charger.
- Route the USB cable's positive (+5 V) conductor through the relay's COM and selected NO/NC contact.
- Identify conductors with a multimeter; wire colors are not guaranteed.
- Insulate and strain-relieve every modified cable joint.

## Timer and trigger
- Power the timer module only within the input range printed on its PCB or specified in its manual.
- Connect the trigger switch to the documented trigger input.
- Configure the timing mode and interval using the module buttons.
- Do not assume the STOP button starts the timer; its behavior depends on the module.

## Relay behavior
For a conventional SPDT relay:
- De-energized: COM–NC closed; COM–NO open.
- Energized: COM–NO closed; COM–NC open.

The timer mode determines the relay state at idle, during countdown, and at timeout. Test these states with a multimeter before selecting NO or NC for the USB path.

## Indicators
- Use suitable series current-limiting resistors with LEDs.
- Confirm the buzzer's voltage/current rating. Use a driver transistor if the timer output cannot safely drive it.
- Confirm indicator polarity and timing against the measured relay/output behavior.

## Power precautions
- Never parallel independent 5 V supply outputs. Equal nominal voltage does not make this safe.
- Separate supplies may be used only when their outputs are not improperly tied together and the module wiring permits it.
- Do not apply 9 V to the phone's USB input.
- This build does not implement USB-C Power Delivery or fast-charge negotiation.

## Commissioning
1. Disconnect the phone.
2. Record timer model, input voltage, and relay contact rating.
3. Identify USB +5 V/GND with a meter.
4. Test timer and trigger operation without the phone.
5. Measure COM–NO and COM–NC continuity at idle, during timing, and after timeout.
6. Verify the phone-side USB output is correct 5 V polarity and that timeout opens the intended charging path.
7. Test LEDs and buzzer.
8. Connect a phone only after these checks pass, initially under supervision.

Follow the timer module's datasheet/manual; this document is not a substitute for it.
