# How to Set up Video Recording
There are a few ways to record a video off or you Mac:

## Screenflow
This is the easiest way.

Download Screenflow https://www.telestream.net/screenflow/

You should be able to trial this software for a month, which should be enough time

## QuickTime + Soundflower + HandBrake
So your Mac can record video as it is with QuickTime. If for some reason you need to record sound out of your computer as well as your microphone, you'll need to install something like Soundflower. You should use HandBrake to compress your video, and reduce the time it takes to upload to YouTube, but then again, compressing your video can take a substantial amount of time anyways.

### Quicktime

1. open Quicktime
2. File>New Screen Recording or File>New Movie Recording
3. Save your file
4. Consider compressing with HandBrake

### Soundflower + Quicktime
This assumes you want to pipe sound from Skype and your microphone into Quicktime. The process should be similar with other applications.

1. Install SoundFlower: You can find the most current version here. https://github.com/mattingalls/Soundflower
You can download pre-compiled binaries or you can be a boss and build it yourself.

2. Open Audio MIDI Setup: On the bottom of your list of devices there is a '+' for adding devices, including virtual ones. You will be creating an aggregate device and a multi-output device. 

3. Make the aggregate device: This will be a new virtual input device. After you create it, you need to check built-in input and Soundflower (2ch). Ignore the drift thing.

4. Create the multi-output device: This will be a new virtual output device. After you create it you need to check  built-in output and SoundFlower (2ch).

5. Make sure built in output and built in input are still your default devices. You can close Audio MIDI Setup.

6. Configure Skype: Open Skype preferences and select the audio/video tab. You want your microphone to be just the built-in input, you can select "same as system" because your built in input should be your system's default device. You want the speakers to be your new multi-output device. (not the aggregate device because that's for input) We're done configuring Skype.

8. Before you start a QuickTime recording, select your aggregate device as your input.
Start recording

## HandBrake

https://handbrake.fr/

You can pretty much ignore all the options and just queue up your file and click start.