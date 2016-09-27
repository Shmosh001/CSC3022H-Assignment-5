Name: Osher Shuman
Student Number: SHMOSH001
Due Date: 15 May 2015
Assignment 5

Audio.h - Template class for manipulation of audio files. Contains a general template and a partial specialization template for a stereo (2 channel) audio file.
driver.cpp - runs when the program is called. Arguements are used to determine what kind of audio file is being inputted, and what operation will be applied to the file.


Instructions:

Program invocation: samp -r sampleRateInHz -b bitCount -c noChannels [-o outFileName ] [<ops>]
soundFile1 [soundFile2]


Description of arguements:
• -r Specifies the number of samples per second of the audio file(s) (usually
44100)
• -b Specifies the size (in bits) of each sample. Only 8bit and 16bit should be
supported in your program. More on this later on.
• -c Number of channels in the audio file(s). Your program will only support 1
(mono) or 2 (stereo).
• “outFileName” is the name of the newly created sound clip (should default
to “out”).
• <ops> is ONE of the following:
• -add: add soundFile1 and soundFile2
• -cut r1 r2: remove samples over range [r1,r2] (inclusive) (assumes
one sound file)
• -radd r1 r2 s1 s2 : add soundFile1 and soundFile2 over sub-ranges
indicated (in seconds). The ranges must be equal in length.
• -cat: concatenate soundFile1 and soundFile2
• -v r1 r2: volume factor for left/right audio (def=1.0/1.0) (assumes
one sound file)
• -rev: reverse sound file (assumes one sound file only)
• -rms: Prints out the RMS of the soundfile (assumes one sound file
only). More details will be given later on.
• -norm r1 r2: normalize file for left/right audio (assumes one sound
file only and that r1 and r2 are floating point RMS values)
• [extra credit] -fadein n: n is the number of seconds (floating point
number) to slowly increase the volume (from 0) at the start of
soundFile1 (assumes one sound file).
• [extra credit] -fadeout n: n is the number of seconds (floating point
number) to slowly decrease the volume (from 1.0 to 0) at the end of
soundFile1 (assumes one sound file).
• “soundFile1” is the name of the input .raw file. A second sound file is
required for some operations as indiceted above.
The sample rate, bit count and number of channels should be used for both the
input files and the resulting output file.
