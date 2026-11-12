*ReCon* is the control center for a chain of [*ReStep*](ReStep.md#manual) and [*ReStepOne*](ReStepOne.md#manual) sequencers.
It lets you pause, reset, start and stop the whole sequence from one place.

- **PAUSE**: freezes the sequence on its current step. Press it again and the sequence continues from that same step on the next clock pulse. The light stays on while the sequence is paused.
- **RESET**: sends the sequence back to step 1 of the first module, no matter which module is playing.
- **RUN**: starts and stops the whole chain.

##### Inputs and outputs

Patch your master clock into **IN** (next to **CLOCK**) and connect **OUT** to the clock input of the first *ReStep*.

The two **EXT** inputs let another module press RESET and RUN for you, for example the reset and run outputs of a clock module.
Each one has its own **OUT** that goes to the first *ReStep*: RESET OUT to its reset input, RUN OUT to its run input.

Connect RUN only to the first module in the chain.
A module with its run input connected acts as the first module of the chain.

##### How it behaves

PAUSE only takes effect between clock pulses, so it never cuts a clock pulse or adds a false one, and the sequence stays in sync with the clock.

If the sequence is running, RESET makes step 1 start on the next clock pulse.
If the reset arrives together with a clock pulse (for example from a clock module's reset output), step 1 starts on that same pulse.
If the sequence is stopped, RESET leaves it ready at step 1.

When you start with RUN, the sequence begins at step 1 of the first module on the next clock pulse.
When you stop it, every module in the chain stops at once.

##### Settings

Right-click the panel to set the **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

#### Starter tips

Use the reset and run outputs of your clock module in the EXT inputs, so pressing play on the clock starts the sequence from the top.

Use PAUSE to hold a note for a few bars during a performance, then let the sequence carry on exactly where it was.
