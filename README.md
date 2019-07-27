# mpa-firmware
This Arduino sketch is a rudimentary firmware for a Teensy 3.6 using the new MPA USB Type added by [cores-mpa](https://github.com/curiousjp/cores-mpa).
In its current state, it listens for a MIDI kit on the 3.6's USB port, and when it receives a message, compares it to a list of note numbers and sets the pad appropriately. It tries to unset the pad 25ms later - it doesn't wait for a noteoff message.
Start/Select can be pressed either by shorting digital pin zero to ground using a switch, or by sending any continous control message (such as via a hat pedal) with a value of more than 0x5A.
Most of the arbitrary numbers can be changed by defines, and a define will also switch the midi notes to conform to what I have had reported about the Yamaha DTX 502 brain.