# SRT Audio Player

Local audio player with waveform visualization and SRT subtitle support.

## Quick Start

### One-liner (after adding alias)
```bash
srtplayer
```

### Or manually
```bash
/home/dev/srt/srt-player/run.sh
```

Open: **http://localhost:8765**

## Usage

1. Upload Audio File (MP3, M4A, WAV, FLAC, OGG, WebM)
2. Upload SRT File
3. Click Play

## Features

- Waveform visualization (wavesurfer.js)
- Real-time subtitle sync
- Click subtitle to seek
- Playback speed (0.5x - 2x)
- Stop/Pause controls

## Requirements

- None! Pure HTML/JS
- Works offline (after first load)

## Tech

- wavesurfer.js v7
- Vanilla JS, no build needed

## Files

```
srt-player/
├── index.html    # Main app
├── run.sh        # Start server (port 8765)
└── README.md     # This file
```