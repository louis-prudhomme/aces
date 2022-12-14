# Aces

## What is this ?

This is a Bash script toolbox, aiming to help transcode, organize and split music files.
- diamonds: transcode music files to _vorbis_ and _flac_.
- clubs: organize music file following a pattern.
- spades: break down music files into smaller tracks.

## Requirements 

All scripts were developed using Bash 5 ; they require a Bash version at least superior to 3.2.75 and aim for `#!/usr/local/bin/bash` (to let you customize your shell).

MacOS, notably, ships an outdated Bash version which will fail to run these scripts (unless preemptively modified).

[Ffmpeg](https://ffmpeg.org/download.html) (and Ffprobe) are required (and made heavy use of). It is necessary to have a _libvorbis_-enabled ffmpeg.

## Usage

This section presents base usage of each script. 

Other parameters and options are available ; use the `--help` to learn everything about it.

### Diamonds

Helps you transcode music files from various formats to either OGG (Vorbis) or Flac. 

Invoke the script with the `input`, `output` and `codec` parameters (at least).

```bash
$ ./diamonds.bash --input "~/Musics/To/Transcode" --output "~/Musics/Transcoded" --codec vorbis
```

**WARNING**: during execution, some files **will** crash ffmpeg, thus crashing the script, which will stop execution.

### Clubs

Helps you sort OGG and Flac music files in your filesystem, according to their music tags.

Invoke the script with the `input` and `output` parameters (at least).

```bash
$ ./clubs.bash --input "~/Musics/To/Organize" --output "~/Musics/Organized" 
```

### Spades

Helps you split music (or video) files into smaller pieces. No attempt will be made to transcode anything; running the script will result in small pieces of the same media container.

Invoke the script with the `input` and `output` parameters, as well as at least one track specification.

```bash
$ ./spades.bash --input "~/File/To.Split" --output "~/Musics/Splited" --track "Title" --start "00:00" --end "50s"  
```

# TODOs

- pre-commit hook TODO engine
- "rebuts" for `diamonds`
- redact proper Shellguide
- add read csv from stdin to spades
- wrapper around youtube-dl ?