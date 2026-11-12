*ReKey* is a one-octave keyboard on the panel.
Use it to change the root note of [*ReQ*](ReQ.md#manual) by hand, or to play notes into an oscillator.

- Keys: click a key to select it. The light on the key shows the active one.
- **1/V KEY** / **OCT** switch: the keyboard mode.
	- **KEY**: works as a helper for *ReQ*. Connect the CV **OUT** to the ROOT CV input of *ReQ*, then press a key to transpose the root note.
	- **OCT**: a simple one-octave keyboard in 1V/octave, to send notes to an oscillator.

##### Inputs and outputs

The CV **IN** input changes with the mode.
In KEY mode, a 1V/octave signal here is scaled to work with *ReQ*.
In OCT mode, the signal is added to the current key and sent to the output.

The CV **OUT** output sends the voltage of the selected key.

**G** is the gate output: it goes HIGH while you hold a key down.
Send it to an envelope to play notes by hand.

##### Settings

Right-click the panel to set the **"Panel"** theme: **Follow Rack**, **Light** or **Dark**.

#### Starter tips

With *ReQ* after your sequencer and *ReKey* on its ROOT CV, you can change the key of the whole song live.

In OCT mode, patch a sequencer into IN and use the keys to transpose it.
