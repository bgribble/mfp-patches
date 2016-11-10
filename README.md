### bgribble's MFP patch repo

MFP is https://github.com/bgribble/mfp ... see the README there
for an overview. 

These patches are created for my own use.  I hope they are
interesting as demos and examples for people interested in MFP,
but that's not the main reason I'm making them :) 

These are the patches that will **eventually** live here.  Right now
most are just placeholders.

### Mixer 

`[mix8bus 12]`: 12x8x2 mixer

I use this mixer to combine and route audio coming in to my
laptop from an external multichannel audio input.   It's set up
with 4 stereo panned busses, 4 aux sends per channel, mutes, and
master gain.  The number of channels is a creation parameter. 

STATUS: working, but sloooow to load and uses too much CPU 

### Step sequencer 

`[stepseq 16,3]` 16-step 3-value step sequencer 

This is a MxN step sequencer, with M steps each outputting N
values and a gate.  It operates in clocked or addressed mode and
has several options for clocked step ordering. 

STATUS: Basic functionality is working.  Clocked (Bang to inlet 0)
and addressed (number to inlet 0) modes, with a "stride" (number to 
inlet 1) that can set the step increment to any positive or negative
value.

### Delay 

`[tdelay]` 

This is a simple delay patch.  It's set up with up to 4
seconds of delay and a panner for ping-pong effects.  It will
do tap-tempo or numeric delay times.  

STATUS: Prototypes done but this patch is not started 

### Mono reverb 

`[plate~]`

Wrapper around a LADSPA reverb plugin I like ("plate" from Steve Harris' 
swh-plugins).  Mono in, stereo out. 

STATUS: Implemented

### Stereo reverb 

`[zreverb]` 

Wrapper around the lovely Zita reverb.

STATUS: Implemented

### Looper 

This is a variant of the Akai Headrush clone in the MFP demos
directory.  It's more designed to be clocked and loop in sync
with the clock.  

STATUS: Prototypes done but this patch is not started 

### Master

The master patch loads all the stuff above and connects it
together.  

STATUS:  Nothing done 

### QuNeo 

I use a Keith McMillen QuNeo as a flexible control surface.  This
patch manages its state and mangles its outputs. 

STATUS:  Nothing done 
