# Design Decisions and Rationale

## Timer-based cutoff
A preset interval on an external timer relay module was selected instead of phone battery-percentage detection. The prototype has no supported interface to read the phone's internal battery state.

**Trade-off:** It disconnects power after elapsed time, not at 100%. Charge level at cutoff varies with starting charge, phone load, and charger behavior.

## External timer relay module
The timer and relay control are handled by a ready-made module, avoiding custom microcontroller firmware in this version.

**Trade-off:** Timing range, trigger behavior, and relay logic depend on the exact module and selected mode. No Arduino sketch is included because none is part of the described build.

## Relay switching
The relay interrupts the USB +5 V conductor. Contact rating, contact resistance, wiring quality, and connector integrity must be appropriate for the charger's current.

## LED and buzzer feedback
Indicators communicate operating status without a phone app. Their active state must be matched to the actual timer output logic and verified wiring.

## Limitations
- Time-based cutoff only; no battery percentage/full-charge detection.
- No charging-current measurement or charge logging.
- No wireless connectivity or mobile application.
- Exact timer model and final terminal mapping still need to be recorded.
- Educational prototype only; not a certified charging product.
- USB-C fast-charge negotiation is not implemented.
