# Using OBS and Zoom together

This repo contains an OBS profile, Scene Collection, and Stream Deck profile that should help you connect OBS and Zoom up to use OBS as a virtual camera and share audio between the two with minimal fuss.

* When using the **Webcam** scene it will display your webcam to both your stream/recording target as well as to Zoom via the Virtual Camera. This is useful for streaming to both Twitch and to Zoom.

* When using the **Zoom** scene it will display your Zoom window to your stream/recording target, it is recommended to turn off your Zoom Camera when you do this do avoid looping your image. This is useful for hosting multiple people in a stream.

> Note: This should work on both Windows and Mac, but so far is only tested on Windows.

## OBS

This was set up using OBS 26.1.1 on Windows with this repo located at `c:\OBS-AND-ZOOM\`. Earlier versions may not work with the plugin.

1. Install the Audio Monitor (0.4.1 tested) plugin from [here](https://obsproject.com/forum/resources/audio-monitor.1186/). Be sure to restart OBS after installing it.

1. Download and install virtual cables from [VB-Audio](https://vb-audio.com/Cable/), I recommend throwing the authors a few dollars and getting the A+B Pack (available for both Windows and Mac) but you can get away with just the one free cable if you're cheap.

## Zoom Setup

1. Set your Microphone to **VB-Audio Cable A**

1. Set your Speakers to **VB-Audio Cable B**

1. Set you Camera to **OBS Virtual Camera**

1. **Settings** -> **Keyboard Shortcuts**

    1. Enable Global Shortcut for **Start/Stop Video**

    1. Enable Global Shortcut for **Mute/Unmute my Audio**

## OBS / Scene Setup

1. Import the `c:\obs-and-zoom\ZoomOBS.json` Scene Collection from this repository into OBS.

1. Import the `c:\obs-and-zoom\ZoomOBS` profile from this repository into OBS.

1. Select the **Zoom + OBS** Profile

1. Select the **Zoom + OBS** Scene Collection

### Background

1. Modify this to an image of your choice

### Microphone

1. Change the **Audio - Microphone** source to your preferred microphone input (mine is a Yeti)

1. **Microphone** -> **Filters** -> **Zoom Mic** should be "VB-Audio Cable A"

1. **Audio - Zoom Speaker** source should be "VB-Audio Cable B"

1. **Audio - Zoom Speaker** -> **Filters** -> **Headphones** should be "Headphones (realtek audio)" (or whatever your headphone device is)

## Cheap and Nasty Single Virtual Cable

If you insist on only using the free single virtual cable you can follow the above settings except set the Zoom microphone to be the same Microphone as OBS, and disable the **Microphone** -> **Filters** -> **Zoom Mic** filter. However it is likely this will cause your audio and video to be slightly out of sync in zoom.

## Stream Deck setup

This is currently a very simple Stream Deck setup that will switch between the "Webcam" and "Zoom" scenes as well as toggle the Zoom Audio and Camera on/off via hotkeys.

1. Import `c:\obs-and-zoom\OBS+Zoom.streamDeckProfile` into Stream Deck.
