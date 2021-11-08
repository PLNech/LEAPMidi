# LEAPMidi
> A LEAPMotion -> MIDI Instrument controller

LeapMIDI is a Javascript WebApp that reads your LeapMotion sensor data, transforms them into MIDi ControlChange messages,
and sends them to your computer's `Midi Through` interface to control the instruments you connect to it.  

In this proof-of-concept, LeapMidi is used to control [ParVagues](https://me.plnech.fr/parvagues/)' track _Du Miel_'s instruments and effects: the CC messages are sent to [TidalCycles](tidalcycles.org/) and [SuperCollider](http://supercollider.sourceforge.net) to control the music.

![Screenshot: TidalCycles track controlled by MIDI Messages sent from a JS webapp reading LeapMotion sensor data](https://user-images.githubusercontent.com/1821404/140657932-93aafe9b-b980-4f08-91b1-ac4e7daae241.png)
_Example setup: Left a **TidalCycles** track, top right **LeapMIDI** tracking X/Y/Z positions of fingers, normalizing them as 0-127 CC values, and sending them via WebMIDI to **SuperCollider** via MidiThrough to control the track's instruments and effects. **LeapMotion Visualizer** bottom right debugs sensor data._

## Usage

0. Setup LeapMotion to send messages readable by the [SDKs](https://developer.leapmotion.com/), in a place where it sees your hands
1. Connect your Midi instrument to the `MIDI Through` port
2. open [index.html](./index.html) in your WebMidi-enabled browser
3. Run [TidalCycles with ParVagues' Du Miel track](https://git.plnech.fr/Tidal/) or adapt the code to map to another use-case
4. ???
5. Profit!

## Demo

[![See demo on YouTube](https://user-images.githubusercontent.com/1821404/140731197-53e4bcd2-6561-4ad3-ba76-c700ef37b9e3.png)](https://www.youtube.com/watch?v=2r48gRZh_UU)

In this demo, the left hand controls effects (left thumb -> global filter, left index -> bass distortion, etc) while the right hand controls individual instruments' volume.

## Thanks

- [TidalCycles](tidalcycles.org) for these mind-blowing possibilities of musical livecoding
- [WebMIDI](https://github.com/djipco/webmidi) for the powerful API and detailed [documentation](https://webmidijs.org/docs/latest/classes/Output.html#method_sendControlChange) 👏
- [LeapJS](https://github.com/leapmotion/leapjs/) for the easy setup and great [examples](https://github.com/leapmotion/leapjs/tree/master/examples)
