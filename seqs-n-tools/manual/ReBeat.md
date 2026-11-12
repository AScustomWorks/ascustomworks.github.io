*ReBeat* is a trigger sequencer and clock divider with sixteen dividers in a grid of 4 rows and 4 columns.
Each row and each column has its own output, so one module gives you eight different trigger patterns.
It's best suited for drum patterns, but you can use it to trigger anything.

- Divider knobs: each one divides the clock from 1 to 32. At 0 the divider is off.
- Mute switch next to each knob: silences that divider so you can change the pattern without touching the knob. It keeps counting in the background, so when you unmute it, it comes back exactly in time.
- Reset button: restarts all the dividers, like the RESET input.

##### Inputs and outputs

**CLOCK** is the clock input and **RESET** the reset input.

The four outputs (**O**) on the right mix the dividers of each row.
The four outputs (**O**) at the bottom mix the dividers of each column.

After a reset, every divider starts counting again from the next clock pulse and fires when its turn comes: a /4 divider fires on pulses 4, 8, 12…, a /3 divider on pulses 3, 6, 9….
You can change any divider while it plays: it stays locked to the bar.

##### Settings

Right-click the panel to set the **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

#### Starter tips

Send each row to a different drum (kick, snare, hihat, percussion) and build the groove with the knobs.

Use the mute switches to drop parts in and out during a performance.

Feed it a fast clock (for example the 16th output of a clock module), or the output of another *ReBeat* or [*ReBit*](ReBit.md#manual), for more complex patterns.

Patch the reset output of your clock module to RESET to keep the patterns locked to the bar.
