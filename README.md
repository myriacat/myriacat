![myriacat](../main/myriacat.gif)

## *myriacat* - real time spectrum analyzer for Linux
- intuitive, dynamic user interface
- logarithmic view with A-weighting for audio engineering
- linear mode with sideband receiver for signal hunting
- phase correlation meter, vectorscope, oscilloscope & cepstrum
- fast power spectrum with smooth waterfall spectogram
- in-house DSP kernel<br><br>

### Download
get the latest version of [myriacat](https://github.com/myriacat/myriacat/releases/latest/download/myriacat_v1.0_beta.tar.gz) here.<br><br>

### Usage
myriacat is portable. open zip folder and type `./myriacat` to run.<br>
on exit, the file `myriaconf.txt` with editable input devices is created.<br>
minimum requirements: Linux 64bit, X11, OpenGL, 24 bit stereo soundcard<br><br>

### First use
Mint, Ubuntu and other Pulseaudio distributions can use `pavucontrol` to<br>
capture from `monitor of built-in Audio` for internal audio monitoring<br><br>

### FAQ

<details>
<summary>no signals are shown</summary>
linux does not route the speaker-output back to programs. you need a software or hardware loopback (cable)
easiest way with pulseaudio is to install "pavucontrol" and set "monitor of built-in Audio" under recording.
this setting will apply only for this one program, and is therefore the least invasive way.
</details>

<details>
<summary>scrolltime is not shown</summary>
the time depends on sps, decimation and screensize. its not shown in vsync or logarithm mode.
</details>
<details>
<summary>can't use sps other then 44k1 and 48k</summary>
those are the supported hardware rates. to use other samplerates, use a softwaredevice like "default" (OS does resampling).
</details>








### License
See the [LICENSE](../main/LICENSE.txt) file for details.<br><br>

### feed the cat
Litecoin LTC: `LaCh6jieaHP14D2VD36voiq4urkzaHZjGr`<br>
