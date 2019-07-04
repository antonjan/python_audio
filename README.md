# python_audio
This repository will have my python audio coded
# Find out what audio interface is avalabale
python3 -m sounddevice<br>
  0 HDA Intel PCH: ALC3246 Analog (hw:0,0), ALSA (2 in, 0 out)<br>
  1 pulse, ALSA (32 in, 32 out)<br>
* 2 default, ALSA (32 in, 32 out)<br>
# Playing 1khz tone to specker devce (1 and 2 should work as seen above)
python3 play_sound_file.py 1kHz_44100Hz_16bit_05sec.wav -d 1
