*ReRatchet* repeats clock pulses: each pulse can come out as a fast burst of 1 to 8 pulses, a *ratchet*.
It has three identical channels.
Put it between your clock or sequencer and what it plays: a drum, [*ReGate*](ReGate.md#manual) or an envelope.

- **COUNT**: how many pulses each burst has, from 1 to 8.
  The display shows the count in use, knob plus CV.

The burst is spread evenly over the time until the next pulse, so it always fits the tempo.
Each pulse of the burst is a gate that lasts half of its slot.

The green light next to RTCH flashes on single pulses and the orange light next to OUT flashes on bursts.

##### Inputs and outputs

**CLK** is the clock input: the pulses you want to repeat.
It can be a clock, the gates of a sequencer or a swung clock from [*ReSwing*](ReSwing.md#manual).
*ReRatchet* measures the time between pulses to spread the burst.

**RTCH** chooses which pulses become bursts:

- HIGH (above 1V): the pulse comes out as a burst of COUNT pulses.
- LOW: the pulse comes out as a single pulse, so the rhythm never drops a beat.
- Not connected: every pulse comes out as a burst.

The input under **COUNT** adds 0 to 7 to the knob with 0V to 10V.
The result is limited to 8.
Set COUNT to 1 to use the full CV range.

**OUT** is the output: single pulses and bursts.

RTCH and COUNT can come from a module driven by the same clock, like [*ReFlip*](ReFlip.md#manual), [*ReBit*](ReBit.md#manual) or [*ReStep*](ReStep.md#manual): its new value is used on the same pulse.

The CLK and RTCH inputs of each channel are linked to the channel above.
With only channel 1 patched, all three channels follow the same clock and the same RTCH, each with its own COUNT.

##### Settings

Right-click the panel to set the **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

##### Notes

*ReRatchet* needs two pulses to measure the clock.
The first pulse after starting, or after the clock stops for more than 10 seconds, passes as it comes in.

*ReRatchet* follows swung clocks, pauses and tempo changes, so a burst never runs into the next pulse.
If a new pulse arrives before a burst has finished, the rest of the burst is skipped.

At very fast clocks the burst gets fewer pulses, and the fastest clocks pass unchanged.

*ReRatchet* has no reset: every pulse is handled on its own.
If the pattern shifts, reset the modules before it, like your sequencer or *ReSwing*.

#### Starter tips

Patch a clock into CLK and a hi-hat after OUT, set COUNT to 2 or 3 and leave RTCH empty: every beat becomes a roll.

For random rolls, send the same clock to *ReFlip* and its output to RTCH.
The *ReFlip* odds set how often a burst comes out.

For a fixed pattern, send a divided clock from *ReBit* to RTCH: the burst always lands on the same beat.

To roll only on the 4th beat of the bar, use *ReStep* with the clock: its GATE O goes to CLK and its CV O to RTCH.
Set steps 1 to 3 to 0V and step 4 to 10V.

For a different number of pulses on every beat, patch a random voltage, like the S&H output of [*ReFluke*](ReFluke.md#manual), into the COUNT input.
