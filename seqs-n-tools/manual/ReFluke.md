*ReFluke* is a noise generator, a *sample & hold* and a gate generator in one module.
Use it for noise sounds, random voltages that change with your clock, or short gates to trigger envelopes.

- **NOISE**: the noise color: **W**hite, **P**ink, **R**ed or **G**rey.
- **CLK DIV**: divides the clock at TRIG, from 1 to 16, to slow down the sample & hold.
- **SCALE**: sets the range of the S&H output, from **-1** to **1**. At 1 it uses the full 10V range; negative values flip it.
- **OFFSET**: moves the S&H output up or down.
- **N** / **G** switch: what the N/G output sends: **N**oise, or a short **G**ate (100 ms) on each divided clock pulse.

##### Inputs and outputs

**IN** replaces the internal noise as the source for the sample & hold.
Patch an LFO or any other signal here for a different kind of stepped voltage.

**TRIG** is the clock input for the sample & hold and the gate generator.

**N/G O** is the noise or gate output, depending on the N/G switch.
**S&H O** is the sample & hold output: on each divided clock pulse it grabs the value of the source and holds it until the next one.

##### Settings

Right-click the panel to set the **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

#### Starter tips

Patch a clock into TRIG and the S&H output into a quantizer such as [*ReQ*](ReQ.md#manual) for random melodies.

Use SCALE and OFFSET to keep the random voltage inside the range you need, for example a gentle filter movement.

Set the switch to G to get a short gate on each divided clock pulse, ready to trigger an envelope.
