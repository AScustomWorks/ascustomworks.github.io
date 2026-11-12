*VC Filter Stereo* is a stereo resonant filter with a low pass and a high pass mode.
Both channels share the same controls, so the stereo image stays intact while you shape the tone.

- **FREQ**: the cutoff, from 40 Hz to 12 kHz. In low pass mode, frequencies above it are cut; in high pass mode, frequencies below it are cut.
- **RES**: resonance. Turn it up to boost the frequencies around the cutoff for a sharper, more vocal sound.
- **MIX**: balance between the dry and the filtered signal. Fully right (the default) you hear only the filter.
- **LP** / **HP** switch: low pass (removes highs) or high pass (removes lows). The change fades over a few milliseconds, so there's no click.

##### Inputs and outputs

FREQ, RES and MIX each have a CV input on the left, next to their knob.
Each voltage adds to its knob.

- FREQ follows about 1V/octave: +1V doubles the cutoff.
- RES and MIX: 10V covers the whole range.

The CV input next to the LP/HP switch flips the mode on each trigger.

The **L** and **R** inputs (marked **I**) take your signal.
With only L connected, the same signal goes to both sides.
The **L** and **R** outputs (marked **O**) are the stereo output.

The module is polyphonic: it filters up to 16 channels on each side, and the FREQ, RES and MIX CVs can be polyphonic too.
A mono cable into an input is used for every channel.

When you bypass the module in Rack, the inputs go straight to the outputs.

#### Starter tips

For a classic synth sweep, use low pass, turn RES up halfway and patch an envelope into the FREQ CV input.

Put it at the end of a stereo mix and slowly raise FREQ in high pass mode to build tension before a drop.

Patch a clock or a sequencer gate into the LP/HP CV input to jump between dark and thin sounds in time with the music.

Set MIX around the middle to keep some of the original sound under the filter.
