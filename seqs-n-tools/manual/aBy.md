*A/B/Y* is a switch for signals, with two sections.
Send one signal to output A or B, or pick which of two signals, A or B, goes to the output.

- **IN ▶ A/B** (top section): click the button to send the **IN** signal to output **A** or output **B**.
- **A/B ▶ OUT** (bottom section): click the button to choose which input, **A** or **B**, goes to **OUT**.

The light on each button shows the current position.
Switching fades over 10 ms, so it doesn't click, even when you switch again in the middle of a fade.

##### Inputs and outputs

Each section has an **EXT** input: a trigger there works like a click on the button, so another module or a sequencer can do the switching.

The signal inputs and outputs are *polyphonic*: one cable can carry up to 16 signals, and the button switches all of them at once.
In the top section, **A** and **B** carry as many channels as **IN**.
In the bottom section, **OUT** carries as many channels as the larger of **A** and **B**, in both positions, so the voices of a polyphonic module after it don't move when you switch.
If one input is mono and the other is polyphonic, the mono signal is copied to every channel.

It works the same for audio and for CV.
Switching between two pitch CVs (1V/octave) sounds like a short glide, because of the 10 ms fade.

##### Settings

Right-click the panel to set the **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

#### Starter tips

Patch a clock divider into EXT to switch between two sounds every bar.

Use the top section to send one sequence to two different voices and swap between them during a performance.

Use the bottom section to pick between two sequences, or two effects, with a single trigger.

Merge several signals into one cable with VCV *Merge*, switch them with *A/B/Y* and split them with VCV *Split* to reroute a whole group of signals at once.
