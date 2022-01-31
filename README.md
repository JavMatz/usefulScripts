
# Table of Contents

1.  [Personal repo of useful shell sripts](#orgd0bec21)
    1.  [trackSplitter](#org31d1ad3)
    2.  [Quality of life](#org3e5ca79)
        1.  [ytDownloadAudio](#orga8135a0)
        2.  [power<sub>check</sub>](#orga8e4bb7)
    3.  [Keyboard shortcuts](#orge379c04)
        1.  [kdb-screenshot](#orge3440b9)
    4.  [Status bar stuff](#org2d658ce)
        1.  [sb-volume](#org4c52904)


<a id="orgd0bec21"></a>

# Personal repo of useful shell sripts


<a id="org31d1ad3"></a>

## trackSplitter

Need [`ffmpeg`](https://ffmpeg.org/) and [`taffy`](https://github.com/jangler/taffy).

Splits a **mp3** file in mp3 tracks using given time marks (and other optional info) in **csv** file and tags them accordingly.

For this script to work as intended you need:

-   An input file in mp3 format.
-   A csv file named `ProcList` with the following columns (see `exProcList` for an example)
    -   `Track Number`, `Start of track`, `End of track`, `Song name`, `Artist`

The input file and `ProcList` need to be in the same directory.

Run `trackSplitter input.mp3 album_of_tracks`.


<a id="org3e5ca79"></a>

## Quality of life


<a id="orga8135a0"></a>

### ytDownloadAudio

Script that facilitates downloading audio from YouTube with [`youtube-dl`](https://github.com/ytdl-org/youtube-dl) and [`taffy`](https://github.com/jangler/taffy).

Run `ytDownloadAudio yt_link track_artist track_album`. `track_artist` and `track_album` are optional arguments. 


<a id="orga8e4bb7"></a>

### power<sub>check</sub>

Uses [`acpi`](https://sourceforge.net/projects/acpiclient/files/acpiclient/) to check if your laptop's power cable is connected. Useful for laptops with dead batteries (like mine).


<a id="orge379c04"></a>

## Keyboard shortcuts


<a id="orge3440b9"></a>

### kdb-screenshot

Uses [`scrot`](https://github.com/resurrecting-open-source-projects/scrot) to take a screenshot of the whole screen or just and area of it if an argument is passed.

Ideally you want to bind this to the `print screen` key of your keyboard, for example:

-   `Print Screen` -> `kbd-screenshot`
-   `Shift + Print Screen` -> `kbd-screenshot 1`


<a id="org2d658ce"></a>

## Status bar stuff


<a id="org4c52904"></a>

### sb-volume

Uses `amixer` to echo the actual volume level or echo `M` if audio is muted.

You may want to call this in your status bar of preference.

