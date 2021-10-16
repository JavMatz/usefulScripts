# Personal repository of useful *sh* scripts #

## trackSplitter ##

Needs [ffmpeg](https://ffmpeg.org/) and [taffy](https://github.com/jangler/taffy). 

Splits a **mp3** file in mp3 tracks using given timemarks (and other info) in a **csv** file and tags them accordingly.

For this script to work as intended you need:

- An input file in mp3 format.
- A csv file named `ProcList` with the following columns (see `exProcList.csv` for an example):
	- `Track Number`, `Start of track`, `End of track`, `Song name`, `Artist`

The input file and `ProcList` need to be in the same directory.

Then run
	`trackSplitter input.mp3 album_of_tracks`

The script then splits the input file in tracks using the `ProcList` file and [ffmpeg](https://ffmpeg.org/). The tracks are put in a new folder (*Tracks*) created in the same directory as the input file and are tagged and named with the pattern 'Track_Number - Artist - Song_name.mp3' with [taffy](https://github.com/jangler/taffy).

While the script was obviously created to be used with music stuff it can be used to split, for example, a recorded interview in parts or an audiobook by chapters.

## ytDownloadAudio ##

A wrapper for [youtube-dl](https://github.com/ytdl-org/youtube-dl) and [taffy](https://github.com/jangler/taffy).

