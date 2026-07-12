# SRT Player

**Local audio player with waveform visualization and SRT subtitle synchronization**

Lightweight, offline-capable audio player built for subtitle editors, content creators, and video professionals. No server required. No internet needed. No API dependencies.

---

## Overview

SRT Player is a browser-based audio player that combines waveform visualization with real-time SRT subtitle synchronization. Built as a single HTML file with all dependencies bundled locally.

Perfect for:
- Video editors reviewing subtitle timing
- Podcasters syncing transcripts
- YouTube creators checking caption accuracy
- Researchers working with audio datasets

---

## Features

| Feature | Description |
|---------|-------------|
| **Waveform Visualization** | Interactive audio waveform rendered with wavesurfer.js |
| **SRT Sync** | Real-time subtitle display synchronized with audio playback |
| **Click-to-Seek** | Click any subtitle segment or waveform position to jump to timestamp |
| **Speed Control** | Playback speed adjustment (0.5x to 2x) |
| **Per-Input Clear** | Individual `[x]` buttons to clear audio or SRT without resetting player |
| **Waveform Hover** | Time tooltip on waveform hover for precise seeking |
| **Offline Ready** | Fully functional without internet connection |
| **No Build Step** | Single HTML file — edit and run immediately |
| **Multi-Format** | Supports MP3, M4A, WAV, FLAC, OGG, WebM |

---

## Quick Start

```bash
# Run the server (starts on port 8765)
/home/dev/srt/srt-player/run.sh
```

Then open: **http://localhost:8765**

Or simply open `index.html` directly in your browser.

---

## Usage

1. Launch the server with `run.sh`
2. Upload an audio file (MP3, M4A, WAV, etc.)
3. Upload an SRT subtitle file
4. Use playback controls: play/pause, stop, speed dropdown
5. Click any subtitle segment to jump to that timestamp
6. Click the waveform to seek to a specific position
7. Use `[x]` buttons to clear individual inputs without resetting

---

## Project Structure

```
srt-player/
├── index.html              # Main application (CSS + HTML + JS in one file)
├── wavesurfer.min.js       # Bundled wavesurfer.js v7 (~40KB)
├── fonts/
│   └── GeistMono.woff2     # Bundled Geist Mono font (~71KB)
├── run.sh                  # Local server launcher (port 8765)
└── README.md
```

---

## Architecture

- **Frontend**: Vanilla JavaScript (strict mode), HTML5, CSS3
- **Audio Engine**: [wavesurfer.js v7](https://wavesurfer-js.org/)
- **Font**: Geist Mono (bundled, no external CDN)
- **No Build Step**: Single file architecture — edit and run immediately
- **Offline Capable**: All dependencies bundled locally

### Waveform Config

Monochrome theme matching the terminal aesthetic:
- `waveColor: '#ccc'`
- `progressColor: '#000'`
- `cursorColor: '#000'`

### File Support

| Format | Extension |
|--------|-----------|
| MP3 | .mp3 |
| M4A | .m4a |
| WAV | .wav |
| FLAC | .flac |
| OGG | .ogg |
| WebM | .webm |

### SRT Compatibility

- Standard SubRip (.srt) format
- UTF-8 encoded files
- Multi-line subtitle support
- Up to 10,000 segments per file

---

## Power of 10

Code follows adapted NASA/JPL Power of 10 rules for safety-critical software:

| Rule | Implementation |
|------|----------------|
| **Strict mode** | `'use strict'` across all functions |
| **Assertions** | 13 `assert()` calls validating all DOM queries and function inputs |
| **Guard functions** | 7 `guardWaveSurfer()` calls preventing null reference errors |
| **Loop bounds** | `MAX_SRT_BLOCKS = 10000` upper bound on all iteration |
| **Scope reduction** | Centralized `state` object, `initDOM()` for all element refs |
| **Return value checks** | All `querySelector` results validated with assertions |
| **Function length** | All functions under 60 lines |
| **Named handlers** | All event listeners use named functions (no anonymous closures) |
| **XSS prevention** | `escapeHTML()` on all user-supplied subtitle content |

---

## Installation

```bash
git clone https://github.com/arthiccc/srtplayer.git
cd srtplayer
./run.sh
```

### Optional: Add Alias

```bash
echo 'alias srtplayer="/home/dev/srt/srt-player/run.sh"' >> ~/.zshrc
source ~/.zshrc
```

---

## System Requirements

| Requirement | Specification |
|-------------|---------------|
| **Browser** | Chrome 80+, Firefox 75+, Safari 14+, Edge 80+ |
| **OS** | Windows 10+, macOS 10.15+, Linux |
| **Dependencies** | None — pure HTML/CSS/JS |
| **Internet** | Not required |

---

## Credits

- [wavesurfer.js](https://wavesurfer-js.org/) — Audio visualization engine
- [JFK/voicesrt](https://github.com/JFK/voicesrt) — Full-featured SRT editor. The GOAT. Transcription, waveform, speaker management, YouTube tools, AI suggestions. Inspired this project.

---

## License

MIT License — see [LICENSE](LICENSE) for details.

---

## Support

https://github.com/arthiccc/srtplayer/issues
