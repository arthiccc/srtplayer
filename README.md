## srtplayer:
browser-based audio player with synced srt subtitles.

## features
- waveform visualization (wavesurfer.js v7).
- real-time subtitle sync with click-to-seek.
- speed control (0.5x to 2x).
- per-input clear buttons.
- waveform hover tooltip for precise seeking.
- fully offline — single html file, no uploads, no cloud.
- nasa power of 10 applied: 13 assertions, 7 guard functions, strict mode.

## usage
- `./run.sh` → opens on localhost:8765.
- upload audio file (mp3, m4a, wav, flac, ogg, webm).
- upload srt file.
- click subtitle segment to jump to timestamp.
- click waveform to seek.
- `[x]` button to clear individual inputs without resetting player.

## project structure
```
srt-player/
├── index.html              # css + html + js in one file
├── wavesurfer.min.js       # bundled wavesurfer.js v7 (~40kb)
├── fonts/
│   └── GeistMono.woff2     # bundled geist mono (~71kb)
└── run.sh                  # local server launcher
```

## credits

inspired by and builds upon the work of:

- [wavesurfer.js](https://wavesurfer-js.org/) — audio visualization engine
- [JFK/voicesrt](https://github.com/JFK/voicesrt) — the goat. full-featured srt editor with transcription, waveform, speaker management, youtube tools, ai suggestions
