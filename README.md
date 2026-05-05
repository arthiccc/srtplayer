<!-- SRT Player - Professional Audio Player with Waveform Visualization -->

<div align="center">

# SRT Player

![SRT Player](https://raw.githubusercontent.com/arthiccc/srtplayer/main/logo.svg)

**Local audio player with waveform visualization and SRT subtitle synchronization**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-blue.svg)](https://github.com/arthiccc/srtplayer)
[![Tech](https://img.shields.io/badge/Tech-HTML5%20%7C%20wavesurfer.js%20%7C%20Vanilla%20JS-green.svg)](https://github.com/arthiccc/srtplayer)

*A lightweight, offline-capable audio player designed for subtitle editors, content creators, and video professionals.*

</div>

---

## Overview

SRT Player is a browser-based audio player that combines waveform visualization with real-time SRT subtitle synchronization. Built for local use—no server required, no internet needed, no API dependencies.

Perfect for:
- 🎬 Video editors reviewing subtitle timing
- 🎙️ Podcasters syncing transcripts
- 📺 YouTube creators checking caption accuracy
- 🧪 Researchers working with audio datasets

---

## Features

| Feature | Description |
|---------|-------------|
| **Waveform Visualization** | Interactive audio waveform rendered with wavesurfer.js |
| **SRT Sync** | Real-time subtitle display synchronized with audio playback |
| **Click-to-Seek** | Click any subtitle segment to jump to that timestamp |
| **Speed Control** | Playback speed adjustment (0.5x to 2x) |
| **Offline Ready** | Fully functional without internet connection |
| **No Dependencies** | Single HTML file—drop and run anywhere |
| **Multi-Format** | Supports MP3, M4A, WAV, FLAC, OGG, WebM |

---

## Quick Start

### Option 1: Command Line (Recommended)

```bash
# Run the server (starts on port 8765)
/home/dev/srt/srt-player/run.sh
```

Then open: **http://localhost:8765**

### Option 2: Direct Open

Simply open `index.html` directly in your browser—no server needed.

---

## Usage Guide

### Step 1: Launch Application

```bash
srtplayer
# Or: /home/dev/srt/srt-player/run.sh
```

### Step 2: Load Files

1. Click **Upload Audio File** → Select your audio (MP3, M4A, WAV, etc.)
2. Click **Upload SRT File** → Select your subtitle file

### Step 3: Playback Controls

| Control | Function |
|---------|----------|
| ▶ Play / ⏸ Pause | Toggle audio playback |
| ⏹ Stop | Stop and reset to beginning |
| Speed dropdown | Adjust playback rate (0.5x–2x) |
| Click waveform | Seek to specific position |
| Click subtitle | Jump to timestamp |

---

## System Requirements

| Requirement | Specification |
|-------------|---------------|
| **Browser** | Chrome 80+, Firefox 75+, Safari 14+, Edge 80+ |
| **Operating System** | Windows 10+, macOS 10.15+, Linux (any modern distro) |
| **Dependencies** | None—pure HTML/CSS/JS |
| **Internet** | Not required (offline capable) |

---

## Project Structure

```
srt-player/
├── index.html           # Main application (open directly in browser)
├── wavesurfer.min.js    # Bundled waveform library (~40KB)
├── run.sh               # Local server launcher (port 8765)
└── README.md            # This documentation
```

---

## Technical Details

### Architecture

- **Frontend**: Vanilla JavaScript (ES6+), HTML5, CSS3
- **Audio Engine**: [wavesurfer.js v7](https://wavesurfer-js.org/)
- **No Build Step**: Single file architecture—edit and run immediately
- **Offline Capable**: All dependencies bundled locally

### File Support

| Format | Extension | Status |
|--------|-----------|--------|
| MP3 | .mp3 | ✅ Supported |
| M4A | .m4a | ✅ Supported |
| WAV | .wav | ✅ Supported |
| FLAC | .flac | ✅ Supported |
| OGG | .ogg | ✅ Supported |
| WebM | .webm | ✅ Supported |

### SRT Compatibility

- Standard SubRip (.srt) format
- UTF-8 encoded files
- Handles multi-line subtitles

---

## Installation

### Clone Repository

```bash
git clone https://github.com/arthiccc/srtplayer.git
cd srtplayer
```

### Optional: Add Alias (Zsh)

```bash
echo 'alias srtplayer="/home/dev/srt/srt-player/run.sh"' >> ~/.zshrc
source ~/.zshrc

# Now just type:
srtplayer
```

---

## License

This project is licensed under the **MIT License**—see [LICENSE](LICENSE) for details.

---

## Acknowledgments

- [wavesurfer.js](https://wavesurfer-js.org/) — Audio visualization powerhouse
- [JFK/voicesrt](https://github.com/JFK/voicesrt) — The GOAT. Full-featured SRT editor with transcription, waveform, speaker management, YouTube tools, and AI suggestions. This project was inspired by their amazing work.
- Built for subtitle editors who need precision timing tools

---

## Support

For issues, feature requests, or contributions, please open an issue at:
https://github.com/arthiccc/srtplayer/issues

---

<div align="center">

*Built with ♡ for the subtitle community*

</div>