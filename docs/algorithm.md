# Operating Algorithm

## Inputs
- User-configured time interval
- Trigger-switch activation
- Timer relay module's selected operating mode

## Outputs
- Relay contact state controlling USB +5 V
- LED status indication
- Buzzer notification

## Functional sequence

```text
START
  |
Power timer module according to its specification
  |
User sets desired interval
  |
Wait for trigger activation
  |
Trigger starts configured timing operation
  |
Timer module controls relay output
  |
Has timeout occurred?
  | No
  +----> Continue timing
  |
 Yes
  |
Relay changes to its configured timeout state
  |
Verify USB +5 V charging path is open
  |
Configured completion indication
  |
WAIT FOR NEXT CYCLE
```

This is a functional algorithm, not source code. Relay behavior is mode-dependent and must be verified. Phone battery percentage is not an input; no automatic full-charge detection is implemented.
