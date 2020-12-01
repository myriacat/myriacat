![myriacat](../main/resources/myriacat.gif)


## ***myriacat*** - audio spectrum analyzer & SDR for Linux
- intuitive, dynamic user interface
- logarithmic view with A-weighting for audio engineering
- linear mode with sideband demodulator for signal hunting
- phase correlation meter, vectorscope, oscilloscope & cepstrum
- portable, lightweight, fluid 4K fullscreen graphics<br><br>


<img src="../main/resources/block_diagram.png" width="560" />


**[download](https://github.com/myriacat/myriacat/releases/latest/download/myriacat_v1.0_beta.tar.gz)**, 
unzip and type `./myriacat` to run.<br>
on exit, `myriaconf.txt` with editable input devices is created.<br>
minimum requirements: Linux 64bit, X11, OpenGL<br><br>


<details>
<summary><b>FAQ:</b> <sub><sup><i>click to expand</i></sup></sub></summary>

- **line in and microphone works, but no display when music/youtube/etc.. is played:**<br>
linux does not route the speaker-output back to programs.<br>
you need a virtual adapter, a software or a hardware loopback. (cable)<br>
easiest way with pulseaudio is to install "pavucontrol" and set "monitor of built-in Audio" under recording.<br>

- **change color of the spectrum**<br>
via colorcode in myriaconf.txt, or direct with <kbd>1</kbd>,<kbd>2</kbd>,<kbd>3</kbd> and <kbd>q</kbd>,<kbd>w</kbd>,<kbd>e</kbd><br>

- **playback of a 192ksps audiofile is cutoff at 22kHz**<br>
some distributions are capped at 22kHz audio.<br>
for audiophiles, specific HiFi/ HiEnd tests or other interests, those settings can be changed.<br>
it is not advised to use this configuration permanently.<br><br>
this is for Mint/Ubuntu with Pulseaudio. other distros might work different.<br>
do this on your own risk! - audio hardware is usually only designed for 20Hz - 20kHz.<br><br>
`cat /proc/asound/card0/pcm0p/sub0/hw_params` usually shows "rate 44100"<br>
`nano /etc/pulse/daemon.conf` remove the ";" in front of "; default-sample-rate = 192000"<br>
`pulseaudio -k && sudo alsa force-reload` to restart the driver and sound subsystem<br>
`cat /proc/asound/card0/pcm0p/sub0/hw_params` again. it will show "rate 192000" now<br><br>
download software generated **[96kHz_sine.wav](https://raw.githubusercontent.com/myriacat/myriacat/main/resources/96kHz_sine.wav)** (192kSps, 0 - 96kHz sweep, 16bit, 10 seconds, low volume)<br>
play it with any good audio player (vlc, xplayer, ..)<br>
set myriacat to normal linear mode (music button off), and<br>
change sps to 192k, channel to L+R, and realtime.<br>
best viewed with inital window-size (1024 pixel) and 2*zoom factor (2048 FFT size).<br><br>
its generally not usefull to use this settings.<br>
myriacat talks directly to the low level alsa hardware interface and can use<br>
192kSps from the HW input anytime, regardless of pulseaudio-configurations.<br><br>
</details>


<details>
<summary><b>applications:</b> <sub><sup><i>click to expand</i></sup></sub></summary>

- **logarithmic audio view:**<br>
real time audio monitoring of frequency characteristics, lossy compression quality analysis<br>
acoustic measurements, vocals aid, harmoics and repsonse tests, instrument tuning<br>

- **linear view:**<br>
scientific data visualization of analog signals, seismic logging, biofeedback research,<br>
ELF/ VLF receiver, Schumann resonances, lightnings, whistlers, spherics, bat detector,<br>
Ham radio, panadapter, Grimeton Radio (SAQ), alpha navigation,<br>
time signals, ripple control, DCF77, mains and trainpower, smartmeter,<br>
naval/marine/submarine communications, aviation beacons<br>

- **upper sideband demodulator:**<br>
select, filter, up/downconvert and listen to selected bandwidths from 270 millihertz to full 96kHz<br>

- **spectrogram:**<br>
logging and averaging of data up to one year<br>

- **oscilloscope**<br>
signal integrity and continuity, clipping and distortions<br>

- **vectorscope**<br>
polar view of stereo image width and position<br>

- **phase correlation meter**<br>
mono compatibility of the stereo signal<br>

- **cepstrum:**<br>
inspection of motors and gearboxes, speaker detection<br><br>
</details>


<details>
<summary><b>features:</b> <sub><sup><i>click to expand</i></sup></sub></summary><br>

- designed and written in C, with low level ALSA and OpenGL acces
- multithreaded in-house DSP kernel, no external libraries
- FFT complex transform, DIT, inplace, radix2, based on Cooley Tukey
- window size from 1024 to 262144 samples
- samplerate from 275sps to 192kSps, 24bit 
- powerspectrum resolution up to 1 millihertz
- demodulator bandwith from sub 1Hz to full bandwith
- windowsize from 256*160 pixels to 4K fullscreen
- waterfall logging of up to a year with scroll time display
- ruler to mark and measure data & harmonic series markers
- overlap-add FFT convolution filter for sideband demodulator
- vertical flank steepness (brickwall) filter without phaseshift
- A-weighting filter according to internation standard IEC 61672:2003
- processing of "hidden bins" in logview, no missing data
- smart buttons replace options and setting-screens, no invalid parameters possible
- single volume control for the whole signaltrain
- every setting is seamlessly changed on-the-fly
- direct hardware access for 24bit, 192kHz stereo audio soundcards
</details><br>




<b>license</b><br>
See the [LICENSE](../main/LICENSE.txt) file for details
<img align="right" width="128" src="../main/resources/logo_with_sign.png">
<br>

<b>feed the cat</b><br>
Litecoin LTC: `LaCh6jieaHP14D2VD36voiq4urkzaHZjGr`<br>




