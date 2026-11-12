*ReStepOne* is a single sequencer step that you can chain with [*ReStep*](ReStep.md#manual) modules.
Mix them to build sequences of any length, and modulate this step with CV.

- Step knob: sets a voltage from 0V to 10V.
- **ATTN**: attenuverter for the **CV IN** input, from **-1** to **1**. The scaled CV is added to the step knob.

The gate length adapts to the clock, as in *ReStep*: 70 ms or half of the time between clock pulses, whichever is shorter.

##### Inputs and outputs

Every row has an input (**I**) and an output (**O**):

- **CLK**: clock in and out.
- **RST**: reset in and out.
- **GATE**: gates in and out. The output on the right carries the gate of the whole chain. The orange output in the middle carries only the gate of this step.
- **CV**: the step voltage in and out.

**RUN** starts the sequence; connect it only on the first module of the chain, from [*ReCon*](ReCon.md#manual).
**STRT** and **NXT** pass the turn from one module to the next.

##### Chaining modules

To chain it with other modules, starting from *ReCon*:

- Connect CLK O to CLK I of the next module, on every module but the last.
- Connect RST O to RST I of the next module, on every module but the last.
- Connect NXT to STRT of the next module, on every module but the last. Then connect NXT of the last module to STRT of the first one to close the loop. Do not connect NXT to the RUN input of the next module: RUN is only for the first module.
- Connect GATE O to GATE I of the next module. The GATE O of the last module goes to your envelope.
- Connect CV O to CV I of the next module. The CV O of the last module goes to your oscillator.

##### Settings

Right-click the panel to set the **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

#### Starter tips

Patch a slow LFO into CV IN and set ATTN low for a step that drifts a little on every pass.

Use the orange gate output of this step to trigger something else, like an accent or a drum, only on this step.
