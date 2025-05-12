Slight modification of the Pro54 cmajor synth: https://github.com/cmajor-lang/cmajor/tree/b303b3a5179515e3227d6745e568e1b7d130e1d1/examples/patches/Pro54
To add midi support.

- Sustain (64) and sostenuto (66) work.
- All knobs and buttons included from the original Pro53 mappings.
- The GUI reflects knob and button changes triggered by midi.
- Added pickup function (very cool): if a knob parameter is changed in the GUI, midi is not received until the physical knob reaches the new GUI value.
  This is useful to sync the midi controller with default patches. Especially when using a controller that can't cover all the knobs in one program.

Problems:
- Keys held by sustain and sostenuto should be kept pressed in the GUI like in the original Pro53 (visual feedback).
- The pick-up function works only sonically, not visually. If a midi CC is disarmed, the GUI knobs related to it remain resposive (only visually). GUI knobs shouldn't move along midi changes, the Midi controller's picks up.

There is a proper commit on midi implementation open. https://github.com/cmajor-lang/cmajor/commit/b303b3a5179515e3227d6745e568e1b7d130e1d1
