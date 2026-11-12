*ReNote* transposes a sequence by octaves and semitones, with three independent channels.
Feed one sequence into the top channel and use the other two to build chords on the fly.

Each channel has:

- **OCT**: octave transpose, from -3 to +3 octaves.
- **SEMI**: semitone transpose, from -7 to +7 semitones.

##### Inputs and outputs

Each channel has an input (**I**), an output (**O**) and two **CV** inputs, one for OCT and one for SEMI.

- The OCT CV input: 0V to 10V sweeps the octave transpose from -3 to +3 octaves (5V = no change). It is added to the OCT knob.
- The SEMI CV input follows 1V/octave, rounded to semitones: each 1/12 V adds one semitone and 1V adds a full octave. It is added to the SEMI knob. It accepts -10V to 10V.

The inputs of channels 2 and 3 are linked to the channel above, as the bracket on the panel shows.
When nothing is connected to them, they use the signal of the channel above, so one sequence can feed all three channels.

##### Settings

Right-click the panel to set the **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

#### Starter tips

For a chord from one sequence, patch it into the top I, then set channel 2 to +4 semitones and channel 3 to +7 semitones for a major chord.

Patch a keyboard such as [*ReKey*](ReKey.md#manual), a quantizer such as [*ReQ*](ReQ.md#manual), or any 1V/octave sequence into the SEMI CV input to transpose the channel by exactly the notes it plays.

For a wider range, chain the channels: connect O of channel 1 to I of channel 2, and so on.
