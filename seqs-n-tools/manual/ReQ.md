*ReQ* is a scale and octave quantizer: it turns any voltage into notes of the scale you choose.
Set the root note, the octave range and the scale, then tune your sequencer while you watch the note on the display.

The display shows the root note, the octave range, the scale and the quantized note.

- **ROOT**: the root note. Quantizing starts from that note.
- **RANGE**: the octave range, from 1 to 10 octaves. Notes outside the range keep their name and move by octaves into it: notes above go to its top octave, notes below go to its bottom octave. The root note is added after the range is applied.
- **SCALE**: the scale. The options are None, Chromatic, Major, Minor, Harmonic Minor, Melodic Minor, Natural Minor, Diatonic Minor, Ionian, Dorian, Phrygian, Lydian, Mixolydian, Aeolian, Locrian, Pentatonic, Blues, Turkish and Indian.

##### Inputs and outputs

ROOT, RANGE and SCALE each have a CV input on the left.
For ROOT and SCALE, 0V to 10V covers all the options.
For RANGE, each volt adds one octave.

**IN** is the voltage to quantize and **OUT** the quantized note, in 1V/octave.
IN and OUT are polyphonic: they carry up to 16 channels, each one quantized on its own.
The ROOT, RANGE and SCALE CVs apply to all channels; the display shows channel 1.

##### Settings

Right-click the panel to set:

- **"Range response"**: where the octave range sits.
	- **Unipolar** (0V up, the default): the range starts at 0V (C4) and goes up. With the range at 4 it covers 0V to +4V. Ideal for sequencers with 0V to 10V knobs.
	- **Bipolar** (centered on 0V): a MIDI keyboard below C4 also works. With the range at 4 it covers -2V to +2V; with an odd range the extra octave goes up (3 covers -1V to +2V). The display shows ±4, and the RANGE tooltip shows the current voltage window.
- **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

#### Starter tips

Put *ReQ* after a [*ReStep*](ReStep.md#manual) chain: every knob position becomes a note of the scale.

Patch [*ReKey*](ReKey.md#manual) into the ROOT CV input to transpose the whole sequence by pressing a key.

Use a small RANGE, like 1 or 2, to keep a random or noisy voltage inside a playable melody.
