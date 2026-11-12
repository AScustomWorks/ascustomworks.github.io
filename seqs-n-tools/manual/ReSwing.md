*ReSwing* gives a clock or a gate sequence a *swing* (shuffle) feel by delaying every second pulse.
It has two identical channels.

- **SWING**: from 50% to 75%. At 50% the clock passes straight. At 66.7% the delayed pulse lands on a triplet. 75% is the maximum. The swing is the point inside each pair of pulses where the second pulse falls. The tooltip shows the value and marks "straight" (50%) and "triplet" (66.7%).

The lights flash green on the on-time pulses and orange on the delayed pulses.

##### Inputs and outputs

**I** is the clock input: clock, trigger or gate.
*ReSwing* measures the time between pulses.
The first pulse of each pair passes on time and follows the input gate.
The second pulse is delayed and keeps the length of the input gate.
The swing is read when the second pulse arrives.

**CV** adds 0% to 25% to SWING with 0V to 10V.
The result is limited to 75%.
Set SWING to 50% to use the full CV range.

**RST** makes the next pulse land on time.
A delayed pulse that has not started yet is cancelled.
Connect it to the same reset as your sequencer so the swing stays aligned with the pattern.

**O** is the output: the swung clock or gates.

The I and RST inputs of channel 2 are linked to channel 1.
With only channel 1 patched, both channels follow the same clock, each with its own swing.

##### Settings

Right-click the panel to set:

- **"Swing steps"**: **Free** (any value) or **Steps** (50, 54, 58, 62, 66.7, 71 and 75%). In Steps, SWING plus CV snaps to the nearest step. Applies to both channels.
- **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

##### Notes

*ReSwing* needs two pulses to measure the clock.
The first pulse after starting, or after the clock stops for more than 10 seconds, passes straight and counts as on time.

Clocks faster than 4 ms per pulse pass unchanged.

Every gate ends 1 ms before the next pulse, so the next module always sees a new pulse.
With long gates and high swing, the delayed gates come out shorter.

If the clock speeds up and a new pulse arrives before a delayed pulse has started, the delayed pulse is skipped.

#### Starter tips

Put *ReSwing* between your clock and your sequencers, and start around 58% for a gentle groove.

Use channel 1 for the drums and channel 2, with a different swing, for the bass.

For gates of a fixed length, patch [*ReGate*](ReGate.md#manual) after *ReSwing*.
