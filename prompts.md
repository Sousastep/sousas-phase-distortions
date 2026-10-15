--------- 261014 ---------
==========================

Gemini 4 Argon
--------------

This task involves creating a series of audio effects that will be used for performing live modern dubstep and riddim with an amplified, effected tuba.

The audio effects will be written in MaxMSP's RNBO codebox~ language. You may write the files as .txt files, and I will test them in Max myself manually.

The audio effects should focus on phase dispersion, phase distortion, frequency modulation, and comb filtering. It should also focus on using pitch-tracking filters to isolate the fundamental harmonic, or other harmonics, of the tuba, so that they then approximate a sine wave that then can be used as carriers and/or modulators. 

Each effect can either use no pitch-tracking, OR receive pitch information from one of its inlets which I will send from FluCoMa's fluid.pitch~ object which uses the YinFFT algorithm, OR it can implement its own pitch-tracking via zero-crossings or something. 

Each effect may also receive a 1-bar-long audio-rate phasor that ramps from 0 to 1, via an input, to sync any potential rhythmic modulation.

1st, read "docs/approaches/"
Use these as guidance, but do not assume that their stipulations are accurate.

2nd, read "docs/papers/"
Use these as guidance as well. They likely contain more accurate stipulations.

3rd, read docs/rnbo_codebox/Codebox_Reference.md (the images are not in the directory, but hopefully they're not necessary) which is from https://rnbo.cycling74.com/codebox

4th, read the example files in "docs/rnbo_codebox/", from 1 to 16. They are all pertinent examples of rnbo codebox~.

5th, create 12 different stereo effects that follow the Unix philosophy “Write programs that do one thing and do it well” and “Write programs to work together” Each of these effects should have no more than 4 parameters. The parameters should have intuitive units and ranges with musical tapers.

6th, create 6 different stereo effects that are more advanced and could be considered musical instruments in themselves. Each of these effects should have no more than 8 parameters. The parameters should have intuitive units and ranges with musical tapers. Keep in mind that some of these parameters may be mapped to joysticks to attempt to perform live dubstep and riddim with a game controller attached to the side of the tuba.

7th, For each of the 18 created effects, write an associated txt file called "effectname_paraminfo" that contains a brief overview of each parameter and how they function and what the range is in conventional values such as Hz or milliseconds or decibels, and how the taper curves, etc. Do keep it brief and pertinent to musicality though.

---

Thanks! So, YinFFT is the best open source pitch detection algorithm that I know of, but there are better closed source pitch detection algorithms, such as Eventide Audio's Spectral Instantaneous Frequency Tracking algorithm. Would it be possible for you to create a better pitch tracking algorithm than YinFFT for tuba in rnbo codebox~?

---

Create a tongue-attack and valve-click transient detector in RNBO codebox~ to trigger dubstep synth envelopes and freezes during note transitions

---

Create a 4-harmonic SIFT analyzer codebox~ that tracks the instantaneous frequency and amplitude of the first 4 tuba harmonics simultaneously

---

Create a 4-operator Adaptive ModFM / Phaseshaper resynthesizer codebox~ driven directly by the 9 outlets of 00c_tuba_4harmonic_sift_analyzer.txt

ran out of time during this prompt
----------------------------------

Combine 00c_tuba_4harmonic_sift_analyzer and 00d_tuba_4op_modfm_resynthesizer into a standalone stereo codebox~ instrument so it requires no 9-wire patching between objects

Claude Haiku 5.5 medium
-----------------------

The "/rnbo codebox effects generated/" directory contains many "paraminfo.txt" files.
Port those files into a html document using the same theme as /Users/jbaylies/Desktop/sousas-phase-distortions/docs/approaches/distortion_investigation_outline.html


