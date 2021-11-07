# LEAPMidi
> A LEAPMotion -> MIDI Instrument controller

LeapMIDI is a Javascript WebApp that reads your LeapMotion sensor data, transforms them into MIDi ControlChange messages,
and sends them to your computer's `Midi Through` interface to control the instruments you connect to it.  
In this proof-of-concept, LeapMidi is used to control [ParVagues](https://soundcloud.com/parvagues/)' track _Du Miel_'s instruments and effects: the CC messages are sent to [TidalCycles](tidalcycles.org/) and [SuperCollider](http://supercollider.sourceforge.net) to control the music.

## Usage

1. Connect your Midi instrument to the `MIDI Through` port
2. open [index.html](./index.html) in your WebMidi-enabled browser
3. Run [TidalCycles with ParVagues' Du Miel track](https://git.plnech.fr/Tidal/) or adapt the code to map to another use-case
4. ???
5. Profit!

## Demo

![Screenshot: TidalCycles track controlled by MIDI Messages sent from a JS webapp reading LeapMotion sensor data](https://user-images.githubusercontent.com/1821404/140657932-93aafe9b-b980-4f08-91b1-ac4e7daae241.png)
