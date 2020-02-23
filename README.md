# python_audio
This repository will have my python audio coded
# Python modules you need
sudo -H pip3 install sounddevice<br>
sudo -H pip3 install soundfile<br>

# Find out what audio interface is avalabale
sudo python3 -m sounddevice<br>
  0 HDA Intel PCH: ALC3246 Analog (hw:0,0), ALSA (2 in, 0 out)<br>
  1 pulse, ALSA (32 in, 32 out)<br>
* 2 default, ALSA (32 in, 32 out)<br>
## Playing 1khz tone to specker devce (1 and 2 should work as seen above)
sudo python3 play_sound_file.py 1kHz_44100Hz_16bit_05sec.wav -d 1
## Testing sending mic input to soundcard
sudo python3 ./wire.py -i 1 -o 1 -s48000 -c1<br>
or try<br>
sudo python3 ./wire.py -i 1 -o 1 -s44000 -c1 <br>
You should here feedback on specker from microphone change -i and -o to your interface<br>
optional arguments:<br>
  -h, --help            show this help message and exit<br>
  -i INPUT_DEVICE, --input-device INPUT_DEVICE<br>
                        input device ID or substring<br>
  -o OUTPUT_DEVICE, --output-device OUTPUT_DEVICE<br>
                        output device ID or substring<br>
  -c CHANNELS, --channels CHANNELS<br>
                        number of channels<br>
  -t DTYPE, --dtype DTYPE<br>
                        audio data type<br>
  -s SAMPLERATE, --samplerate SAMPLERATE<br>
                        sampling rate<br>
  -b BLOCKSIZE, --blocksize BLOCKSIZE<br>
                        block size<br>
  -l LATENCY, --latency LATENCY<br>
                        latency in seconds<br>
