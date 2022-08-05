# Aces

## What is this ?

This is a Bash script toolbox, aiming to transcode and organize music files.
- diamonds: transcode music files to _vorbis_ and _flac_.
- clubs: organize music file following a pattern.

## Requirements 

All scripts were developed using Bash 5 ; they require a Bash version at least superior to 3.2.75.

MacOS, notably, ships an outdated Bash version which will fail to run these scripts (unless preemptively modified).

[Ffmpeg](https://ffmpeg.org/download.html) (and Ffprobe) are required.

## Usage

### Diamonds

Invoke the script with the `input`, `output` and `codec` parameters (at least).

```bash
$ ./diamonds.bash --input ~/Musics/To/Transcode -output ~/Musics/Transcoded -codec vorbis
```

Other parameters and options are available ; use the `--help` to learn everything about it.

**WARNING**: during execution, some files will crash ffmpeg, thus crashing the script, which will stop execution.

## Clubs 

Invoke the script with the `input` and `output` parameters (at least).

```bash
$ ./clubs.bash --input ~/Musics/To/Organize -output ~/Musics/Organized 
```

# TODOs

- TODO pre-commit hook engine
- add dry run
- "rebuts" for `diamonds`
- redact proper Shellguide
- remove `eval`s
- extract `find` command
- try to add more modularity