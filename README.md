Slight modification of the Pro54 cmajor synth: https://github.com/cmajor-lang/cmajor/tree/b303b3a5179515e3227d6745e568e1b7d130e1d1/examples/patches/Pro54
To add midi support.

- Sustain (64) and sostenuto (66) work.
- All knobs and buttons included from the original Pro53 mappings.
- The GUI reflects knob and button changes triggered by midi.
- Added pickup function (very cool): if a knob parameter is changed in the GUI, midi is not received until the physical knob reaches the new GUI value.
  This is useful to sync the midi controller with default patches. Especially when using a controller that can't cover all the knobs in one program.

Functions missing:
- Keys held by sustain and sostenuto should be kept pressed in the GUI like in the original Pro53. Useful for visual feedback.
- I'd prefer the pickup function to freeze the GUI knob until the related midi control is armed again, but that was too complicated to include for me.

The code might be redundant and dirty. It just works for me.
There is a proper related commit open. https://github.com/cmajor-lang/cmajor/commit/b303b3a5179515e3227d6745e568e1b7d130e1d1
