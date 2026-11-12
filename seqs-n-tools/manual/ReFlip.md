*ReFlip* adds chance to your gates: each gate passes or not, depending on the odds you set.
It has three sections that work on their own, so you can add probability to any sequencer.

Each section has:

- **ODDS**: the chance that a gate passes to the output. Fully left no gate passes; fully right every gate passes.

##### Inputs and outputs

Each section has a gate input (**I**), a gate output (**O**), a clock input (**CLK**) and a CV input for ODDS.
The ODDS CV adds to the knob: 10V adds the full range.

What the section does depends on what you connect:

- **Gate and clock**: the clock sets when a new random value is drawn, and the gate passes according to the odds.
- **Gate only**: each gate draws its own random value.
- **Clock only**: the clock itself passes according to the odds, which turns *ReFlip* into a random trigger generator.
- **No cables**: the output stays at 0V.

Gates that arrive before the first clock also follow the odds.
Each section only uses its own CLK input.

##### Settings

Right-click the panel to set the **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

#### Starter tips

Put *ReFlip* between a sequencer's gate output and your envelope, and turn ODDS down until some notes start to drop out.

Usually you'll use the same clock as your sequencer, but try a different clock, or a pattern from [*ReBit*](ReBit.md#manual), for even more variation.

On hihats, a section with only a clock connected makes random triggers that keep the groove moving.
