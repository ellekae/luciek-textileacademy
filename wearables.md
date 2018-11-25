---
description: prototyping a wearable artefact incorporating the attiny
---

# wearables



### AUDIO

The Audio file to store on the SD card must be in the .wav format with 44100 Hz, 16-bit stereo quality. In theory, audio files can be converted using iTunes:

```text
Click _> Edit > Preferences > Import Settings_
Change the dropdown to _WAV Encoder_ and Setting: _Custom > 16.000kHz to 32kHz, 8-bit, Mono_
Right click any file in iTunes, and select _"Create WAV Version"_
```

.. however most are AAC protected files which cannot be converted. An alternative is [this](https://audio.online-convert.com/convert-to-wav) online wav converter. 

### SPEAKER

![](.gitbook/assets/us512340_tesla_coil_for_electro-magnets_page1_800x1200.png)

  
measure the resistance of the speaker. the circuit requires an 8OHM speaker. 

### VOLUME CONTROL

soft, embedded volume slider based on leah buechley's [time sensing bracelet](https://www.instructables.com/id/Time-Sensing-Bracelet/) and kobakant's [embroidered potentiometers](http://www.kobakant.at/DIY/?p=2331). 

#### LINKS

{% embed url="http://kicad-pcb.org/" %}

{% embed url="https://www.arduino.cc/en/Tutorial/SimpleAudioPlayer" %}

{% embed url="https://www.instructables.com/id/Arduino-Audio-Output/" %}

{% embed url="https://www.instructables.com/id/Arduino-Audio-Input/" %}

{% embed url="https://www.instructables.com/id/Easy-ATTiny-Serial-Communication-with-Tiny-AVR-Pro/" %}

{% embed url="http://cnmat.berkeley.edu/recipe/how\_and\_why\_add\_pull\_and\_pull\_down\_resistors\_microcontroller\_i\_o\_" %}

{% embed url="https://github.com/ghmartin77/KidsMP3Player/blob/master/KidsMP3Player/DFMiniMp3.h" %}

{% embed url="http://www.kobakant.at/DIY/?p=2936" %}

{% embed url="https://www.youtube.com/watch?v=8tNrPVi4OGg" %}

