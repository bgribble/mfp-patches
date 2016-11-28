### bgribble's MFP patch repo

MFP is https://github.com/bgribble/mfp ... see the README there
for an overview. 

These patches are created for my own use.  I hope they are
interesting as demos and examples for people interested in MFP,
but that's not the main reason I'm making them :) 

### Mixer 

`[mix8bus 12]`: 12x8x2 mixer

I use this mixer to combine and route audio coming in to my
laptop from an external multichannel audio input.   It's set up
with 4 stereo panned busses, 4 aux sends per channel, mutes, and
master gain.  The number of channels is a creation parameter. 

### Step sequencer 

`[stepseq 16,3]` 16-step 3-value step sequencer 

This is a MxN step sequencer, with M steps each outputting N
values and a gate.  

### Delay 

`[monodelay~]` 

This is a simple mono delay patch using the builtin `[delblk~]` object. 
It's set up with up to 5 seconds of delay, feedback, and wet/dry mix. 

### Mono reverb 

`[plate~]`

Wrapper around a LADSPA reverb plugin I like ("plate" from Steve Harris' 
swh-plugins).  Mono in, stereo out. 

### Stereo reverb 

`[zreverb]` 

Wrapper around the lovely Zita reverb.

### QuNexus

I use a Keith McMillen QuNexus as a flexible control surface and
interface between MIDI and CV.  This patch routes note events and 
CV data to and from the qunexus.

