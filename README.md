# Personal repository of useful *sh* scripts #

## power_check ##

Needs [acpiclient](https://sourceforge.net/projects/acpiclient/files/acpiclient/) and [libnotify](https://gitlab.gnome.org/GNOME/libnotify)

Checks if the AC adapter of a laptop is connected and sends a notification if it's not.

## trackSplitter ##

Needs [ffmpeg](https://ffmpeg.org/). 

Splits a **mp3** file in mp3 tracks using given timemarks in a **csv** file.

For this script to work as intended you need

- An input file in mp3 format.
- A csv file named `ProcList` with the following columns (see `exProcList.csv` for an example):
	- `Track Number`,`Start of track`, `End of track`, `Song name`, `Artist`

The input file and `ProcList` need to be in the same directory.

The script then splits the input file in tracks using the `ProcList` file. The tracks are put in a new folder (*Tracks*) created in the same directory as the input file and are named with the pattern 'Track Number - Artist - Song name.mp3'

While the script was obviously created to be used with music stuff it can be used to split, for example, a recorded interview in parts or an audiobook by chapters.

## ytDownloadAudio ##

Needs [youtube-dl](https://github.com/ytdl-org/youtube-dl)

Downloads the audio of your link in **mp3** format at the best quality possible in the current directory.

Download rate is limited at 196 kilobytes per second with the `--limit-rate` option from youtube-dl but this is not necessary and can be removed.
