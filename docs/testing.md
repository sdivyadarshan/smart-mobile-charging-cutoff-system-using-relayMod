# Testing Checklist

Do not mark a test as passed until it has been performed and recorded on the physical build.

## Inspection and power
- [ ] Record timer relay module make/model.
- [ ] Confirm timer supply voltage and polarity from its label/manual.
- [ ] Confirm relay contact rating.
- [ ] Confirm charger output is regulated 5 V.
- [ ] Confirm independent 5 V outputs are not connected in parallel.
- [ ] Inspect insulation, solder joints, and cable strain relief.

## Timer and trigger
- [ ] Set a known short interval.
- [ ] Confirm the displayed setting.
- [ ] Activate the trigger switch and confirm timing begins.
- [ ] Verify STOP button behavior separately.
- [ ] Repeat the trigger test.

## Relay
- [ ] Measure COM–NO continuity at idle.
- [ ] Measure COM–NC continuity at idle.
- [ ] Observe contact state during countdown.
- [ ] Observe contact state after timeout.
- [ ] Confirm timeout opens the intended USB +5 V path.
- [ ] Check for unintended restart or latched state.

## Output and indicators
- [ ] Measure phone-side USB voltage and polarity before connecting a phone.
- [ ] Confirm expected 5 V output when charging is enabled.
- [ ] Confirm output is disconnected at timeout.
- [ ] Verify red LED behavior.
- [ ] Verify green LED behavior.
- [ ] Verify buzzer operation and duration.
- [ ] Check LED resistor and buzzer drive ratings.

## Supervised phone test
- [ ] Connect phone only after all previous checks pass.
- [ ] Confirm charging starts in the intended active state.
- [ ] Allow timer to reach timeout and confirm charging disconnects.
- [ ] Check for unexpected heating, smell, noise, or instability.

## Test record

| Date | Timer mode/interval | Measured output | Relay state | Result/notes |
|---|---|---|---|---|
| To be completed | To be completed | To be measured | To be observed | Not yet recorded |

No results are pre-filled because verified measurements were not provided.
