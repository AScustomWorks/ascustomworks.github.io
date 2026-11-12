*ReGate* turns triggers into gates of the length you choose, with two channels.
It also works the other way: set a short length to turn long gates into short triggers.

Each channel has:

- **LENGTH**: the length of the output gate. The tooltip shows it in milliseconds.
- **S** / **L** switch: the range of LENGTH. Short goes from 1 ms to 70 ms; Long goes from 1 ms to 490 ms.

##### Inputs and outputs

Each channel has an input (**I**) for a clock, trigger or gate, and an output (**O**) with the new gate.

LENGTH and the S/L switch each have a CV input, so you can change them from another module.

##### Settings

Right-click the panel to set:

- **"Overlapping gates"**: what happens when a new pulse arrives while the gate is still HIGH.
	- **Merge** (the default): the gate is extended, so pulses close together become one long gate. Useful for ties or slides.
	- **Retrigger**: the output drops for a moment and a new gate starts with its full length, so every input pulse gives a new gate. Use it when the gate is longer than the time between pulses, for example after [*ReSwing*](ReSwing.md#manual).
- **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

#### Starter tips

Patch a clock into I and the output into an envelope: LENGTH now sets how long each note is held.

Send the output to an envelope that controls a filter, then move LENGTH with an LFO for notes that open and close in different ways.

Feed the gates of a sequencer through *ReGate* with a short length to get clean triggers for drums.
