*ReBit* is a trigger sequencer and clock divider with four dividers in one column.
Use each divider on its own, or mix them at the SUM output to create trigger patterns.

- Divider knobs: each one divides the clock from 1 to 32. At 0 the divider is off.
- Mute switch next to each knob: silences that divider. It keeps counting in the background, so when you unmute it, it comes back exactly in time.
- Reset button: restarts all the dividers, like the RST input.

##### Inputs and outputs

**CLK** is the clock input and **RST** the reset input.

Each divider has its own output (**O**) on the right.
**SUM** mixes the four dividers into one trigger pattern.

After a reset, every divider starts counting again from the next clock pulse and fires when its turn comes: a /4 divider fires on pulses 4, 8, 12…, a /3 divider on pulses 3, 6, 9….
You can change any divider while it plays: it stays locked to the bar.

##### Settings

Right-click the panel to set the **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

#### Starter tips

As a simple clock divider, set one knob to the division you want and use its own output.

For a trigger pattern, set each knob to a different division and use SUM.

Feed it a fast clock (for example the 16th output of a clock module), or the output of another *ReBit* or [*ReBeat*](ReBeat.md#manual), for more complex patterns.

Patch the reset output of your clock module to RST to keep the patterns locked to the bar.
