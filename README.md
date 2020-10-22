![myriacat](../main/myriacat.gif)

## *myriacat* - real time spectrum analyzer for Linux
- intuitive, dynamic user interface
- logarithmic view with A-weighting for audio engineering
- linear mode with sideband demodulator for signal hunting
- phase correlation meter, vectorscope, oscilloscope & cepstrum
- fast power spectrum with smooth waterfall spectogram up to **4K Fullscreen!**
- multithreaded in-house DSP kernel<br><br>

<img src="../main/block_diagram.png" width="480" />


### Usage
download the latest portable version of [myriacat](https://github.com/myriacat/myriacat/releases/latest/download/myriacat_v1.0_beta.tar.gz) here, 
open zip folder and type `./myriacat` to run.<br>
on exit, the file `myriaconf.txt` with editable input devices is created.<br><br>
minimum requirements: Linux 64bit, X11, OpenGL, 24 bit stereo soundcard<br>


<big>FAQ</big><small>(click to unfold)</small>

Normal text
<sub><sup>Small text</sup></sub>

<big><big>tutorial</big>tutorial</big>tutorial<small>tutorial<small>tutorial</small></small>


**FAQ**<sub><sup>(click to unroll)</sup></sub>


### FAQ
<details>
<summary>(click to unroll)</summary>

**no signals are shown when music/youtube/etc.. is played:**<br>
linux does not route the speaker-output back to programs.<br><br>
you need a virtual adapter, a software or a hardware loopback (cable)<br>
easiest way with pulseaudio is to install "pavucontrol" and set "monitor of built-in Audio" under recording.

**only 44k1 and 48k sps are selectable**<br>
those are the supported hardware rates. to use other samplerates, use a softwaredevice like "default" (OS does resampling).<br>

**playback of a 192kHz audiofile is cutoff at 24kHz**<br>
192ksps (96kHz signal) input will be shown if a suitable HW device is selected.<br>
to monitor recorded samples, the alsa config of linux needs to be modifed, as its usually capped at 48ksps (24khz).<br>

</details>

### applications:
<details>
<summary>(click to unroll)</summary>
  
**logarithmic audio view:**<br>
real time monitoring, lossy compression quality analysis.

**linear view:**<br>
scientific data visualization of analog signals, seismic logging, biofeedback research,<br>  
ELF, VLF ,Schumann resonances, lightinings, whistlers, sferics,<br>
time signals, ripple control, DCF77, mains and trainpower, smartmeter, Grimeton Radio (SAQ),<br>
naval/marine/submarine communications, aviation beacons, alpha navigation,<br>
bat detector<br>

**upper sideband demodulator:**<br>
select, filter, up/downconvert and listen to selected bandwidths from 270 millihertz to full 96kHz

**spectrogram:**<br>
logging and averaging of data up to one year.

**cepstrum:**<br>
inspection of motors and gearboxes, speaker detection
</details>


### License
See the [LICENSE](../main/LICENSE.txt) file for details.<br><br>

### feed the cat
Litecoin LTC: `LaCh6jieaHP14D2VD36voiq4urkzaHZjGr`<br>
