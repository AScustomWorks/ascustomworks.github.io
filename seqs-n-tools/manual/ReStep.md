*ReStep* is a 1 to 4 step sequencer that you can chain.
Add or remove modules to build sequences of any length, even while the music is playing.

- **1** to **4**: the step knobs. Each one sets a voltage from 0V to 10V.
- Mute switch next to each step: mutes the gate of that step. The step still plays its CV and keeps its place in time, so the sequence stays in sync.
- **STEPS**: the length of this module's sequence, from 1 to 4 steps.

The gate length adapts to the clock: 70 ms or half of the time between clock pulses, whichever is shorter.
At any tempo every step gets its own separate gate.

##### Inputs and outputs

Every row has an input (**I**) and an output (**O**):

- **CLK**: clock in and out.
- **RST**: reset in and out.
- **GATE**: gates in and out.
- **CV**: the step voltage in and out.

**RUN** starts the sequence; connect it only on the first module of the chain, from [*ReCon*](ReCon.md#manual).
**STRT** and **NXT** pass the turn from one module to the next.

##### Chaining modules

To chain several *ReStep* modules, starting from *ReCon*:

- Connect CLK O to CLK I of the next module, on every module but the last.
- Connect RST O to RST I of the next module, on every module but the last.
- Connect NXT to STRT of the next module, on every module but the last. Then connect NXT of the last module to STRT of the first one to close the loop. Do not connect NXT to the RUN input of the next module: RUN is only for the first module.
- Connect GATE O to GATE I of the next module. The GATE O of the last module goes to your envelope.
- Connect CV O to CV I of the next module. The CV O of the last module goes to your oscillator.

With a single *ReStep* you don't need STRT and NXT; the module handles that for you.
You still need *ReCon* (or any trigger) on RUN to start it.

##### Settings

Right-click the panel to set the **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

#### Starter tips

Change STEPS on each module of the chain while you play to mutate your sequences: the result is always in sync.

Mix it with [*ReStepOne*](ReStepOne.md#manual) for sequences of odd lengths, like 5 or 7 steps.

Put a quantizer such as [*ReQ*](ReQ.md#manual) after the last CV O to turn the knobs into notes of a scale.
