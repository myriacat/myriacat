![myriacat application screenshot](https://raw.githubusercontent.com/myriacat/myriacat/main/resources/screen21.png)
<br>
<br>

## ![myriacat](https://raw.githubusercontent.com/myriacat/myriacat/main/resources/namesign.png)
- Linux spectrum analyzer with VLF SDR
- up to **4K fullscreen**, fluid realtime Display
- fast, intuitive, portable & lightweight<br>
- get newest **[myriacat](https://github.com/myriacat/myriacat/releases/download/v1.2/myriacat_1.2.tar.gz)** here<br>

<br>

![block diagram](https://raw.githubusercontent.com/myriacat/myriacat/main/resources/block_diagram.png)
<br>

> 💡 **use myriacat as spectrum analyzer for your music/youtube etc:**<br>
> linux does not route the speaker-output back to programs, the easiest way is<br>
> to install pavucontrol, and set "monitor of built-in Audio" at the recording tab.<br>

<br>
<details>
<summary><b>FAQ:</b> <sub><sup><i>click to expand</i></sup></sub></summary>
  
- **minimum requirements:**<br>
Linux 64bit on AMD64 compatibles with Alsa audio, X11 and OpenGL (Mint, Ubuntu, Debian, Manjaro, ..)<br>
for extended analysis outside the HiFi range, a 24bit/192kHz Soundcard is recommended.<br>

- **configuration:**<br>
on exit, `.myriaconf.txt` with editable input devices is created.<br>
available devices can be listed with `arecord -l`<br>
only 24bit HW can be addressed directly, others will be only available under "default"<br>

- **antenna for DX?**<br>
the common Realtek ALC887 (24bit/192Sps) audio Codec allows<br>
source impedances up to 40KOhm on the ADC (mic input).<br>
a cable to a metal Doorframe or Radiator is sufficient to see<br>
50KW Time signal stations 500 miles away.<br>
preamplifiers and tuned Antennas are recommended for weak Signals.<br><br>
16bit USB Audio Dongles often need much lower impendance sources,<br>
its not possible to receive weak Signals without LF preamplifiers.<br>

- **change color of the spectrum**<br>
via colorcode in myriaconf.txt, or direct with <kbd>1</kbd>,<kbd>2</kbd>,<kbd>3</kbd> and <kbd>q</kbd>,<kbd>w</kbd>,<kbd>e</kbd><br>

- **playback of a 192ksps audiofile is cutoff at 22kHz**<br>
some distributions are capped at 22kHz audio for playback.<br>
for audiophiles, specific HiFi/ HiEnd tests or other interests, those settings can be changed.<br>
this is for Mint/Ubuntu with Pulseaudio. other distros might work different.<br>
do this on your own risk! - audio hardware is usually only designed for 20Hz - 20kHz.<br>
it is not advised to use this configuration permanently.<br><br>
`cat /proc/asound/card0/pcm0p/sub0/hw_params` usually shows "rate 44100"<br>
`nano /etc/pulse/daemon.conf` remove the ";" in front of "; default-sample-rate = 192000"<br>
`pulseaudio -k && sudo alsa force-reload` to restart the driver and sound subsystem<br>
`cat /proc/asound/card0/pcm0p/sub0/hw_params` will show "rate 192000" now<br><br>
play software generated **[96kHz_sine.wav](https://raw.githubusercontent.com/myriacat/myriacat/main/resources/96kHz_sine.wav)** (192kSps, 0 - 96kHz sweep, 16bit, 10 seconds, low volume)<br>
set myriacat to linear mode (music button off), 192k, L+R, and realtime.<br>
best viewed with initial window-size (1024 pixel) and 2*zoom factor (2048 FFT size).<br><br>
its generally not useful to use this settings.<br>
myriacat talks directly to the low level alsa hardware interface and can use<br>
192kSps from the HW input anytime, regardless of pulseaudio-configurations.<br><br>
</details>


<details>
<summary><b>applications:</b> <sub><sup><i>click to expand</i></sup></sub></summary>

- **logarithmic audio view:**<br>
essential precision tool for recording, mixing and mastering<br>
real time monitoring for video streaming, live events and recording Studios<br>
audio FX visualizer for DJ's and Professional Audio Engineering<br>
visual feedback for vocalists and content creators<br>
evaluate harmonics, frequency response curves, acoustic characteristics measurements<br>
instrument tuning, note training, vocal aid<br>
lossy compression quality analysis<br>
hydroacoustics, whalesounds, aquatic studies and marine sound visualization<br>

- **linear view:**<br>
pixelexact linear visualization of analog signals for scientific research<br>
ham radio, panadapter, ripple control, DCF77, smartmeter<br>
naval/submarine communications, alpha navigation, aviation beacons<br>
wideband and narrowband sonogram, passive sonar, signal hunting<br>
radio astronomy, SID monitor, lightning detector, whistlers, spherics<br>
seismic logging, schumann resonances<br>
forensic analysis, pattern detection<br>
bioresonance feedback<br>

- **upper sideband demodulator:**<br>
downconvert and listen to selected bandwidths from 270 millihertz to full 96kHz<br>
LF continuous wave and communications receiver<br>
VLF SDR, Grimeton Radio SAQ receiver<br>
ultrasonic, infrasound, sonar and sonography converter<br>
bat detector<br>

- **oscilloscope**<br>
check for signal integrity and continuity<br>
catch clipping, offset and distortions<br>

- **vectorscope, goniometer**<br>
polar view of stereo image width and position<br>

- **phase correlation meter**<br>
mono compatibility of the stereo signal<br>

- **cepstrum:**<br>
inspection of motors and gearboxes,<br>
acoustic signature vessel identification,<br>
DEMON (Detection of Envelope Modulation on Noise),<br>
speaker detection<br><br>
</details>


<details>
<summary><b>features:</b> <sub><sup><i>click to expand</i></sup></sub></summary><br>

- designed and written in C, with low level ALSA and OpenGL access
- multithreaded in-house DSP kernel, without external libraries
- complex Fourier Transformation, DIT, inplace, radix2, based on Cooley Tukey
- FFT window size from 1024 to 262144 samples
- samplerate from 275sps to 192kSps, 24bit 
- powerspectrum resolution up to 1 millihertz
- demodulator bandwidth from sub 1Hz to full bandwidth
- window size from 256*160 pixels to 4K fullscreen
- waterfall logging up to >100 years with scroll time display
- measuring ruler & harmonic series markers
- overlap-add FFT convolution filter for sideband demodulator
- vertical flank steepness (brickwall) filter without phaseshift
- A-weighting filter according to international standard IEC 61672:2003
- hidden bin processing in log-view, no missing data
- smart buttons replace options and setting-screens, no invalid parameters possible
- single volume control for the whole signaltrain
- every configuration is seamlessly changeable on-the-fly
- savestate memorizes all settings for next use<br><br>
</details>


<details>
<summary><b>changelog:</b> <sub><sup><i>click to expand</i></sup></sub></summary>

- **v1.2**<br>
extended long time measurements up to >100 Years<br>
reversed average selector<br>
updated colors<br>
minimal visual changes<br>
enforce max screensize of 4096*2048<br>
  
- **v1.1**<br>
adapt main spectrum shading to new mesa driver specification<br>
change goniometer presentation to fix software rendering bug<br>
convert ruler seconds to timestamp<br>
update font spacing<br>
adjusted colors<br>
tested on:<br>
Mint cinnamon 18.3 - 20.1,<br>
Ubuntu Gnome 20.10,<br>
Debian KDE Plasma 10.7.0 and<br>
Manjaro xfce 20.2.1<br>

- **v1.0**<br>
first public release<br><br>
</details><br>




<b>license</b><br>
See the [LICENSE](../main/LICENSE.txt) file for details
<img align="right" width="128" src="../main/resources/logo_with_sign.png">
<br>

<b>feed the cat</b><br>
Litecoin LTC: `LaCh6jieaHP14D2VD36voiq4urkzaHZjGr`<br>




