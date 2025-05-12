This is a fork of the Pro54 cmajor synth: https://github.com/cmajor-lang/cmajor/tree/b303b3a5179515e3227d6745e568e1b7d130e1d1/examples/patches/Pro54
It adds midi support.

- Sustain (64) and sostenuto (66) work.
- All knobs and buttons included from the original Pro53 mappings.
- The GUI reflects knob and button changes triggered by midi.
- Added pickup function (really cool). If a knob parameter is changed in the GUI, midi is not received for that parameter until the physical knob reaches the same value.

Functions missing:
- Keys held by sustain and sostenuto should be kept pressed like in the original Pro53. Useful for visual feedback.
- I'd prefer the pickup function to freeze the GUI knob until the midi control is armed again, but that was too complicated to include for me.

There is a commit related in progress.
https://github.com/cmajor-lang/cmajor/commit/b303b3a5179515e3227d6745e568e1b7d130e1d1
