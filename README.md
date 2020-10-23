![myriacat](../main/myriacat.gif)

## ***myriacat*** - real time spectrum analyzer for Linux
- intuitive, dynamic user interface
- logarithmic view with A-weighting for audio engineering
- linear mode with sideband demodulator for signal hunting
- phase correlation meter, vectorscope, oscilloscope & cepstrum
- fast power spectrum with smooth waterfall up to **4K fullscreen!**
- multithreaded in-house DSP kernel, no external libraries
- pure C, no external libraries, lightweight & portable<br><br>

<img src="../main/block_diagram.png" width="560" />


**[download](https://github.com/myriacat/myriacat/releases/latest/download/myriacat_v1.0_beta.tar.gz)**, 
unzip and type `./myriacat` to run.<br>
on exit, the file `myriaconf.txt` with editable input devices is created.<br>
minimum requirements: Linux 64bit, X11, OpenGL, 24 bit stereo soundcard<br><br>


<details>
<summary><b>FAQ:</b> <sub><sup><i>click to expand</i></sup></sub></summary>

- **no signals are shown when music/youtube/etc.. is played:**<br>
linux does not route the speaker-output back to programs.<br>
you need a virtual adapter, a software or a hardware loopback (cable)<br>
easiest way with pulseaudio is to install "pavucontrol" and set "monitor of built-in Audio" under recording.<br>

- **only 44k1 and 48k sps are selectable**<br>
those are the supported hardware rates. to use other samplerates, use a softwaredevice like "default" (OS does resampling).<br>

- **playback of a 192kHz audiofile is cutoff at 24kHz**<br>
192ksps (96kHz signal) input will be shown if a suitable HW device is selected.<br>
to monitor recorded samples, the alsa config of linux needs to be modified, as its usually capped at 48ksps (24khz).<br><br>
</details>


<details>
<summary><b>applications:</b> <sub><sup><i>click to expand</i></sup></sub></summary>

- **logarithmic audio view:**<br>
real time audio monitoring, lossy compression quality analysis<br>
room accoustic measurements, instrument testing<br>

- **linear view:**<br>
scientific data visualization of analog signals, seismic logging, biofeedback research,<br>
ELF, VLF, Schumann resonances, lightnings, whistlers, spherics, bat detector<br>
time signals, ripple control, DCF77, mains and trainpower, smartmeter, Grimeton Radio (SAQ),<br>
naval/marine/submarine communications, aviation beacons, alpha navigation<br>

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

- FFT size from 1024 to 262144 samples
- samplerate from 275sps to 192kHz, 24bit 
- powerspectrum resolution up to 1 millihertz
- demodulator bandwith from sub 1Hz to full bandwith
- windowsize from 256*160 pixels to 4K fullscreen
- waterfall logging of up to a year with scroll time predictor
- ruler to mark and measure data & harmonic series markers
</details><br>

<img align="right" width="256" src="../main/logo_with_sign.png">

<b>license</b><br>
See the [LICENSE](../main/LICENSE.txt) file for details.<br><br>


<b>feed the cat</b><br>
Litecoin LTC: `LaCh6jieaHP14D2VD36voiq4urkzaHZjGr`<br>
