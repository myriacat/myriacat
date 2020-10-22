![myriacat](../main/myriacat.gif)

## *myriacat* - real time spectrum analyzer for Linux
- intuitive, dynamic user interface
- logarithmic view with A-weighting for audio engineering
- linear mode with sideband receiver for signal hunting
- phase correlation meter, vectorscope, oscilloscope & cepstrum
- fast power spectrum with smooth waterfall spectogram up to 4K Fullscreen!
- in-house DSP kernel<br><br>

### Download
get the latest version of [myriacat](https://github.com/myriacat/myriacat/releases/latest/download/myriacat_v1.0_beta.tar.gz) here.<br><br>

### Usage
myriacat is portable. open zip folder and type `./myriacat` to run.<br>
on exit, the file `myriaconf.txt` with editable input devices is created.<br>
minimum requirements: Linux 64bit, X11, OpenGL, 24 bit stereo soundcard<br><br>

### FAQ

<details>
<summary>no signals are shown</summary>
linux does not route the speaker-output back to programs. you need a software or hardware loopback (cable)
easiest way with pulseaudio is to install "pavucontrol" and set "monitor of built-in Audio" under recording.
</details>

<details>
<summary>scrolltime is not shown</summary>
the time depends on sps, decimation and screensize. its not shown in vsync or logarithm mode.
</details>

<details>
<summary>can't use sps other then 44k1 and 48k</summary>
those are the supported hardware rates. to use other samplerates, use a softwaredevice like "default" (OS does resampling).
</details>

<details>
<summary>the speed/view/size on my 8K, 400FPS monitor is bad</summary>
dont use vsync, myriacat is tested for up to 2K, 50-120fps monitors at this time.
if the UI is too small on high-dpi devices, you will need to find a way to upscale the program.
</details>

<details>
<summary>playback of a 192kHz audiofile is cutoff at 24kHz</summary>
most of the test files on various audio-sites are not what they claim to be.
if you have a file with actual 192kHz sps (96kHz signal) it will be show on myriacat.
for output over the playback device, you also need to change linux alsa configs, as they are capped at 48ksps.
</details>

### License
See the [LICENSE](../main/LICENSE.txt) file for details.<br><br>

### feed the cat
Litecoin LTC: `LaCh6jieaHP14D2VD36voiq4urkzaHZjGr`<br>
