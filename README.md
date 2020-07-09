# Information

Naked Drums is a multi-mics drumkit from Wilkinson Audio, with 10 round-robins,
up to 5 velocity layers and several mic layers (Direct, OH, Close room,
Far rooms, Mid-side and Wide OH). Originally available free in Kontakt nki format,
now created as SFZ format v2 (ARIA extensions) with flac samples by kinwie.

## Shells

- Yamaha Recording Custom - Cherry
- Remo Heads
- 22" Kick Drum
- 10", 12", 13",  14", 16" Toms
- Ayotte 14" x 5" silver sparkle snare
- Pearl 13" x 6.5" Joey Jordison Signature Snare

## Cymbals

- Mixture of Sabian HH/AA/AAX and some Zildjian A Series
- 2 Splashes
- 2 Crashes (bow and bell)
- 2 Chinas
- Ride (bow and bell)
- Hi-Hats

## Preamps

- Vintage Neve 1073
- Vintage Neve 1081
- BAE 1073
- API 512

## Converters

- Apogee Symphony IO
- Apogee Rosetta 800


# Installation

For the ARIA Player multi (.ariax) files to work properly,
you need to place the "Wilkinson Audio" folder into your ARIA Player/Sforzando
"User files path" directory:

```
[User files path]\Wilkinson Audio\Naked Drums\
```

Then you can load the ariax files or just drag'n drop it to ARIA Player GUI.

# Structure

Presets in "Stereo" folder are version for stereo-output Sforzando,
full to less mic layers used.
So less mic layers also means less RAM and polyphony used.
Individual 16 mics are in the "Multi" folder used by `.ariax` presets for
ARIA Player. You can also load them with 16-instances of Sforzando.

The channel/slots are:

1. Kick In
2. Kick Sub
3. Snare Tops
4. Snare Bottom
5. Tom 1
6. Tom 2
7. Tom 3
8. Tom 4
9. Tom 5
10. Hats
11. Ride
12. Overheads
13. Close Room
14. Far Rooms
15. Mid-Side
16. China Wide OH

This SFZ version using a flexible structure for the need of adjusting/modifying
parameters, key-mapping, etc, to affect all mic layers and kitpieces
simultaneously in an easy way. All the main settings are placed in "macro.txt"
file and the key-mapping in "keymap.txt" file in the "Data" folder.
So for general user tweaks, can be done in these two files.
For example, there is a "User" folder which contains "Naked Drums GM" and
"Naked Drums TD-12" presets with different key-mapping and mic layers used.
By learning a little bit of sfz format, you will be able to make presets of your own.

# Controls

Sforzando's generic controls range :

- 0% -to- 100%
- Center value is 50% (set-to-default by Ctrl-click)
- Volume at 0% will also turn off the mic layer and saving polyphony
- Pan center is 50%. Lower value go Left and higher value go Right

Kitpiece controls (volume and pan) in the "Stereo" version are for the Direct
mics only (Kick, Snare, Toms, Hats and Ride). Mic layers name are the volume
control for each mic layer globally. An example, to make cymbals louder or quieter,
turn up or down the "Overheads" control.
In the "Multi" version, each kitpiece volume can be adjusted independently in
the respective mic channel.

Snare Top using two mics. There is a "splitter" in the Snare Tops channel
to split these two mics into individual mono track (L-R) that can be routed
to your DAW tracks for individual processing when needed. The splitter use CC67,
so you can just press sforzando's Left Pedal to activate it.

To adjust volume to velocity tracking (amp_veltrack), open the macro.txt file
and change the value of `#define $VELTRACK`. Range from 0 to 100.
The default is set to 99. Lower value means lower velocity gets louder.

# Features

This kit features Polyphonic Aftertouch usage for cymbal choke that commonly used
by E-Drums kits like Roland TD. Choking a cymbal is done by grabbing the cymbal
pad and this kit will response to that message.
For the use with Keyboard controller or DAW piano-roll, choking the cymbal by
other key.
The cymbal choke keys are placed at key 60 and above.

* A little issue only for the Crash Edge choke with key, is that, the choke key needs
to be pressed before releasing the crash edge key.

There are 2 hihat modes,

- Non-variable : using notes for all articulations
- Variable : using MIDI CC to switch between articulations

Common MIDI CC used by E-Drums for controlling the hihat is CC 4, switch from
0-127, Open - Half - Closed/Tight.

Switching between these 2 modes using Keyswitch (note 12 and 13,
and this also can be change in the keymap)

* Note, that changing the keywitch for the ARIA Player version need to be done
from keyboard controller or DAW midi track to affect all channel/slots at once.
Changing keyswitch from ARIA Player GUI only affect the respective slot.

# Additional Info

- This sfz version is 'side-ward' compatible with the original wav files, by putting all the wavs into this sfz "Samples" directory, and then change the `#define $ext` to wav (in the macro.txt).

- Caution for `.ariax` multi version : Do not change volume and pan (CC7 & CC10) from your Keyboard/MIDI controller/DAW MIDI track, because it will modify all the ARIA Player's slots/channels simultaneously.

# License

<a rel="license" href="https://creativecommons.org/licenses/by/4.0/">
<img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />
This work is licensed under a <a rel="license" href="https://creativecommons.org/licenses/by/4.0/">
Creative Commons Attribution 4.0 International License</a>.
