<a id="top"></a>

<p align="center">
  <img src="Logo.png" alt="AudioAuditor Logo" width="120"/>
</p>

<h1 align="center">AudioAuditor</h1>

<p align="center">
  <b>Audit Your Audio with Confidence</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/.NET-8.0-512BD5?style=round" alt=".NET 8"/>
  <img src="https://img.shields.io/badge/License-Apache%202.0-89276f?style=round" alt="Apache 2.0 License"/>
  <br/>
  <a href="https://github.com/Angel2mp3/AudioAuditor/releases"><img src="https://img.shields.io/github/downloads/Angel2mp3/AudioAuditor/total?style=round&color=4F50C6" alt="Downloads"/></a>
  <a href="https://ko-fi.com/angelsoftware"><img src="https://img.shields.io/badge/Support-Ko--fi-f26b2e?style=round&logo=ko-fi&logoColor=white" alt="Support on Ko-fi"/></a>
  <a href="https://github.com/Angel2mp3/AudioAuditor"><img src="https://img.shields.io/badge/GUI-Windows-0060BF?style=round" alt="GUI: Windows"/></a>
  <a href="https://github.com/Angel2mp3/AudioAuditor/tree/main/AudioAuditorCLI"><img src="https://img.shields.io/badge/CLI-Windows%20%2B%20Linux-1B1C31?style=round" alt="CLI: Windows + Linux"/></a>
</p>

<br/>

<p align="center">
  <b>⭐ Featured & Reviewed By</b>
</p>

<p align="center">
  <a href="https://www.softpedia.com/get/Multimedia/Audio/AudioAuditor.shtml" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/Softpedia-5%2F5%20editorial%20review-00205C?style=round" alt="Softpedia — 5/5 Editorial Review"/></a>
  <a href="https://bedroomproducersblog.com/2026/07/28/audioauditor/" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/BPB-Featured%20article-33373A?style=round" alt="Bedroom Producers Blog — Featured Article"/></a>
  <a href="https://fmhy.net/audio#spectrum-analyzers" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/FMHY-Curated%20listing-6B65AE?style=round" alt="FMHY — Curated Listing"/></a>
</p>

<p align="center">
  <a href="https://trendshift.io/repositories/22767?utm_source=trendshift-badge&utm_medium=badge&utm_campaign=badge-trendshift-22767" target="_blank" rel="noopener noreferrer">
    <img src="assets/trendshift-badge-dark.svg" alt="Angel2mp3/AudioAuditor | Trendshift" width="250" height="55"/>
  </a>
</p>

---

> 🛡️ **Official downloads only:** [audioauditor.org](https://audioauditor.org/) and [GitHub](https://github.com/Angel2mp3/AudioAuditor). Any other source is unofficial and may contain malware.

---

## 📑 Table of Contents

<p align="center">
  <a href="#overview"><kbd>Overview</kbd></a>
  <a href="#screenshots"><kbd>Screenshots</kbd></a>
  <a href="#features"><kbd>Features</kbd></a>
  <a href="#getting-started"><kbd>Getting Started</kbd></a>
  <a href="#usage"><kbd>Usage</kbd></a>
  <a href="#settings-overview"><kbd>Settings</kbd></a>
  <a href="#data--privacy"><kbd>Data & Privacy</kbd></a>
  <a href="#project-structure"><kbd>Project Structure</kbd></a>
  <a href="#interactive-code-tour"><kbd>Code Tour</kbd></a>
  <a href="#technology"><kbd>Technology</kbd></a>
  <a href="#faq"><kbd>FAQ</kbd></a>
  <a href="#support--supporters"><kbd>Support</kbd></a>
  <a href="#contributing"><kbd>Contributing</kbd></a>
  <a href="#credits--acknowledgments"><kbd>Credits</kbd></a>
  <a href="#license"><kbd>License</kbd></a>
</p>

---

## Overview

**AudioAuditor** is a feature-rich audio analysis app for Windows that analyzes your audio files to detect **fake lossless**, verify **true quality**, identify **clipping**, detect **MQA encoding**, detect **AI-generated audio**, estimate **effective frequency cutoffs**, and much more — all wrapped in a sleek, themeable interface with a built-in audio player, equalizer, spatial audio, spectrogram viewer, and real-time visualizer.

Whether you're an audiophile verifying your FLAC collection, a music producer checking masters, or just curious about the true quality of your library, AudioAuditor gives you the data you need at a glance.

---

## Screenshots

<p align="center">
  <img width="1599" height="867" alt="AudioAuditor main window using the blurple theme" src="https://github.com/user-attachments/assets/f3ff6ceb-bea6-483f-8d38-53395e0dbfe0" />
  <br/>
  <img width="1599" height="867" alt="AudioAuditor main window using the amethyst theme" src="https://github.com/user-attachments/assets/ae5a5a01-ebad-453d-9bed-a105de3be576" />
  <img width="1483" height="762" alt="AudioAuditor CLI running a scan" src="https://github.com/user-attachments/assets/4efa884a-0e9e-4ed6-a90e-4505baa33c50" />

</p>

---

## Features

### Core Analysis
- **Fake Lossless Detection** — Identifies files that claim to be high-quality but are actually upsampled from lower bitrate sources by analyzing spectral content and effective frequency cutoff
- **Spectral Frequency Analysis** — FFT-based spectral analysis (4096-point, Hanning-windowed) determines the true effective frequency ceiling of your audio
- **Clipping Detection** — Digital clipping scan with percentage and sample-count reporting; thorough mode detects clipping even when audio has been scaled down by up to 0.5 dB, reported as "SCALED (dB, %)"
- **MQA Detection** — Identifies MQA and MQA Studio encoded files, reports original sample rate and encoder info
- **AI-Generated Audio Detection** — Scans metadata tags, raw byte patterns, and content provenance markers (C2PA) to identify AI-generated music from 20 named services including Suno, Udio, AIVA, Boomy, Stable Audio, Riffusion, ElevenLabs, and Google Lyria. Features confidence scoring weighted by evidence strength, false-positive filtering against known DAWs/encoders, AI watermark detection (AudioSeal, SynthID, WavMark), experimental spectral analysis (7 checks), and SH Labs API integration. The AI column reflects results from **all** enabled detection sources — standard, experimental, and SH Labs — and names which tier of evidence the verdict rests on
- **Optimizer Detection** — Detects files that have been processed through audio "optimizers"
- **BPM Detection** — Algorithmic beat detection with tag-based BPM fallback
- **Replay Gain** — Extracts and displays Replay Gain metadata from tags
- **Comprehensive Metadata** — Artist, title, sample rate, bit depth, channels, duration, file size, and bitrate (reported vs. actual)
- **Fake Stereo Detection** — Detects mono-duplicated or artificially widened stereo files incorrectly labeled as stereo
- **True Peak Measurement** — Inter-sample true peak level (dBTP) using 4× oversampling, displayed in a dedicated column
- **LUFS Measurement** — Integrated loudness (LUFS / LKFS) per ITU-R BS.1770 with K-weighting
- **Rip/Encode Quality Detection** — Detects bad rips by analyzing zero-sector gaps, clicks/pops, stuck samples, and bit truncation. Opt-in via Settings → Analysis
- **Silence Detection** — Detects excessive silence gaps with configurable threshold (default 500 ms) and edge skip zone to avoid false positives on intros/outros
- **Frequency Cutoff Allow** — Files whose cutoff meets or exceeds a configurable Hz threshold (default 19,600 Hz) are not flagged as low-quality upconverts
- **Always Full Analysis** — Force a complete sample pass even when individual detectors are disabled
- **AcoustID Fingerprinting** — Identify unknown tracks via audio fingerprint against the AcoustID/MusicBrainz database; auto-downloads fpcalc
- **Improved Bitrate Analysis** — Avoids simplistic "320 kbps" labeling for files with steep lowpass filters using a band-energy-drop method; lossless formats (FLAC/WAV/AIFF/APE/WV) report their actual file data rate instead of a lossy-equivalent estimate
- **Custom FLAC Decoder** — Managed FLAC decoder handles files that NAudio cannot decode natively, ensuring full analysis and playback coverage
- **Full Metadata Editor** - Full menu for editing, adding, or removing metadata in an audio file, including search buttons to auto-search for the metadata for you
- **Update Checker** — Optionally silently checks for updates in the background each time the program starts

### Supported Formats

| Lossless | Lossy | Other |
|----------|-------|-------|
| FLAC | MP3 | DSF (DSD) |
| WAV | MP2 | DFF (DSD) |
| AIFF / AIF | AAC | AU / SND |
| APE | OGG | MKA (Matroska) |
| WV (WavPack) | OPUS | WEBM |
| ALAC | WMA | 3GP / 3G2 |
| TTA | M4A / M4B / M4R | AMR |
| TAK | MP4 | AC3 |
| | Musepack (MPC / MP+) | |
| | Speex (SPX) | |

> **Cross-platform note (CLI):** **FLAC, WAV, AIFF, OGG/Vorbis, Opus, MP3/MP2 and DSD** use fully-managed decoders and analyze everywhere with no setup. Every other format in the table is decoded through **ffmpeg**, which AudioAuditor runs as a separate process — so install it to get full coverage on Linux and macOS:
>
> ```
> sudo apt install ffmpeg      # Debian/Ubuntu
> brew install ffmpeg          # macOS
> ```
>
> On **Windows**, grab a build from **<https://ffmpeg.org/download.html>** (pick one whose name contains `lgpl`) and either put it on your `PATH` or drop `ffmpeg.exe` into a `third-party\ffmpeg\` folder next to `AudioAuditor.exe`. The Batch Editor's Convert tab has a **"Get ffmpeg…"** button that opens that same page and an **"Open folder"** button that opens the exact folder to drop it in.
>
> Run `audioauditorcli --version` to confirm it was found. Without ffmpeg, the managed formats still analyze normally and the rest are read for metadata but skipped for quality analysis. On Windows, AAC/M4A, ALAC, WMA and friends also decode through the built-in Media Foundation codecs, so ffmpeg is only needed there for the formats Windows has no codec for (**APE, WavPack, TAK, Musepack, Speex**).

### Built-in Audio Player
- Full playback controls — Shuffle, Previous, Rewind 5s, Play/Pause, Forward 5s, Next
- **Shuffle mode** — Toggle shuffle to play tracks in random order; works with auto-play next, manual next/prev, and queue
- Animated waveform progress bar with smooth edges
- Volume control with mute toggle (click speaker icon)
- Click-to-seek slider with drag support
- Auto-play next track and queue system
- **Crossfade** with configurable duration (1–30 seconds) and **4 curve types** — Equal Power, Linear, Natural, and Sequential (no overlap). Optional **Crossfade on Manual Skip** toggle
- **Gapless Playback** — Seamless track transitions with zero silence gap between consecutive tracks
- Audio normalization toggle (peak-based, targets −1 dB)
- **Hi-res audio support** — Native playback of high sample-rate audio (96 kHz, 192 kHz, etc.) with automatic fallback resampling if the device can't handle the native rate
- **Spatial Audio** — Headphone-optimized soundstage widening using crossfeed, HRTF-like interaural time delay, head shadow simulation, and early reflections
- **10-band Parametric Equalizer** — 32 Hz to 16 kHz with ±12 dB per band, soft clipping protection, collapsible panel, per-band reset, built-in presets, and custom profile save/delete
- **Seek Safety Protection** — Multi-layered audio safety system prevents loud pops or static when seeking
- **Loop Modes** — Cycle between Loop Off, Loop All, and Loop One with a single button
- **Seek Tooltip** — Hovering over the seek slider shows a live time preview that follows your cursor
- **Favorites** — Star any file to mark it as a favorite; favorites always sort to the top and persist across sessions
- **Main Window Color Match** — Optionally tint the entire UI dynamically from the currently playing track's album art
- **Offline Mode** — Disable all network calls with a single toggle
- **Lyrics Save & Auto-Save** — One-click export of fetched timed lyrics as `.lrc` files, or enable auto-save
- **Mini Player** — A compact, draggable, **always-on-top** floating window (toolbar button) with cover art, title/artist, transport, seek, volume/mute, and shuffle. It has its own optional inline **Circles** visualizer that runs independently of the main window, and it remembers its style, ColorMatch toggle, and size/position across restarts

### Now Playing Panel
- **Immersive full-panel view** — Click the album cover or press the expand button on the playbar to open a two-column Now Playing panel: album art with color-matched glows on the left, synced lyrics on the right
- **Configurable background effects** — Choose Off, Color Drift, Stars, Rain, Snow, **Leaves**, or **Underwater**. Stars include independent per-star twinkle/parallax and occasional shooting stars; Rain has wind-blown streaks with optional lightning; Snow uses soft drifting flakes; Leaves tumble and sway on the wind; Underwater is a calm deep-sea scene with rising bubbles, drifting light shafts, swaying seaweed, and occasional fish. Effect density, lightning frequency, flake/leaf size, and a global animation speed are all adjustable with theme-matched sliders
- **Album Color-Match Theming** — Dominant colors extracted from the album art are applied to the panel background, glows, visualizer accent colors, and even the **Windows title bar** (via DWM) for a fully cohesive look
- **Color Cache** — Cached extracted album-art colors keep skipping and scrolling through Now Playing with **Color Match** enabled smooth and snappy. The cache is always on and always saved to `%APPDATA%\AudioAuditor\`, so the smoothness survives app restarts. It stores a very small amount of color data (a few bytes of RGB per track, with hashed keys — no file paths), and you can clear it any time from Settings → Cache & Files
- **ColorMatch eyedropper** — Pick up to three colors directly from the album cover to override the extracted palette for the current track; right-click the eyedropper to reset
- **Synced Lyrics** — Automatic time-synced lyrics from multiple sources: embedded tags, local `.lrc` files, LrcLib, Netease Music, and Musixmatch. Lyrics auto-scroll and highlight the current line; click any line to seek directly to that timestamp. Cycle through providers with the source button. Drag-and-drop `.lrc` files onto the panel to load them instantly
- **Explicit vs Clean detection** — Reads a version hint from tags (title markers like `(Explicit)`/`[Clean]`/`(Radio Edit)`, ID3v2 `iTunesAdvisory`, MP4 `rtng`) and ranks lyric search candidates so explicit tracks don't get clean lyrics (and vice-versa). A **"Wrong version?"** button in the lyrics header toggles Explicit↔Clean and re-fetches
- **Censored-lyrics auto-fallback** *(opt-in)* — When a provider returns lyrics with profanity masked by `*****`/`#####`, AudioAuditor automatically tries the next provider for a clean copy
- **Look Up This Song** — The Now Playing magnifier has its **own** configurable search-service list (up to 6, with custom URLs/icons), separate from the main window's toolbar buttons; one button seeds it from your main-window setup
- **Focused Lyrics mode** — Keep the active synced lyric line clear while inactive lines are softly blurred for easier reading during playback
- **Lyrics Off Mode** — Hide lyrics completely to show only album art + visualizer
- **Lyrics Translation (beta)** — Real-time translation into any supported language; auto-detects the source language or lets you set it manually
- **Karaoke Mode (beta)** — Word-by-word highlighting that illuminates each word as it's sung with smooth color transitions
- **Next Track / Artist Preview** — Displays the upcoming track or current artist below the album cover; click to toggle between the two
- **Dedicated Seek Bar** — Full drag-and-seek slider inside the Now Playing panel with no position jumping while dragging
- **Visualizer Placement** — Choose between a full-width visualizer bar above the playbar or a compact strip under the album cover
- **Visualizer Drag-Resize** — Grab the handle between the album art and lyrics to resize the visualizer strip from 40–400 px
- **Layout Customization** — Adjust album cover size and position, title and artist text size and position, lyrics panel size and position, and visualizer size and position via a live-preview popup organized into collapsible sections. All layout preferences persist across sessions
- **Layout Profiles** — Save named layouts; profiles are **visualizer-aware**, capturing separate windowed/fullscreen × visualizer-on/off arrangements (sizes, offsets, visualizer height & placement) so one saved look adapts to every mode
- **Album Cover Glow slider** — Size the halo around the cover from off (`0`) through the default soft glow up to a large bloom (`2.0`); the breathing pulse respects the scale and the setting persists
- **Auto-Scaling Layout** — The cover, visualizer, and surrounding layout scale proportionally when the visualizer is toggled on or off, so a single slider setting looks right in both modes without needing separate profiles
- **NP Control Bar** — Shuffle, Loop, Auto-Play, Visualizer, Visualizer Placement, Lyrics Off, Translate, Karaoke, Color Match, Queue, and Settings buttons — all directly accessible from the panel
- **Queue Button & Popup** — Opens the full Queue window with drag-and-drop reordering, plus an **Up Next** preview showing the next track

### Spectrogram Viewer
- Full-resolution spectrogram generation with logarithmic frequency scaling (20 Hz – Nyquist)
- **Linear frequency scale** — Toggle between logarithmic and linear frequency axis
- **L-R difference channel** — View Left minus Right channel spectrogram to reveal stereo differences; persists across sessions
- **Jump to end** — Zoom into the last 10 seconds of a recording to inspect fade-outs and tail content
- **Mouse wheel zoom** — Scroll to zoom in up to 20x on the spectrogram for detailed inspection; horizontal scrollbar for panning; click the zoom indicator to reset
- Hanning-windowed FFT with 4096-point resolution; optional **Hi-Fi mode** uses Blackman-Harris windowing with 16384-point FFT for enhanced detail
- Deep **−130 dB analysis floor** for visibility into low-level content
- Two color gradients: classic (black → blue → purple → red → orange → yellow → white) and **Scientific Magma** perceptual colormap
- Frequency axis labels (50 Hz → 20 kHz)
- **In-memory LRU cache** — Up to 30 spectrograms cached for instant re-opening
- Export individual spectrograms as labeled PNG files
- Batch export all spectrograms to a folder
- Double-click spectrogram to save
- **View Spectrogram** — Right-click any file to open a dedicated fullscreen spectrogram window with Log/Linear, Mono/L-R, Full/End toggles, and a Save button
- **Compare Spectrograms** — Select two files and open a side-by-side full-resolution spectrogram view with:
  - **Stacked** — Top/bottom layout with Fit/Full zoom toggle
  - **Overlay** — Vertical slide-to-merge with a red-channel **diff heatmap** showing pixel-level differences in the overlap region; includes horizontal Offset slider for alignment and Merge slider for blend control
  - **Wipe** — Draggable vertical splitter revealing one file on the left and the other on the right

### Real-time Audio Visualizer
- 64-band FFT frequency visualizer running at 60 FPS
- **6 visualizer modes** — Bars, Mirror, Particles, Circles, Scope, VU Meter
- Smooth attack/decay animation with per-mode rendering
- Log-frequency bar distribution matching human hearing
- **Independent visualizer theme** — Choose a separate color theme for the visualizer, follow the playbar, or set the playbar to **Follow Theme** and match the app color theme automatically
- **Auto-cycle mode** — Automatically rotate between selected visualizer modes on a configurable timer (5–60 seconds)
- **Full volume rendering** — Optional mode that renders the visualizer at full intensity regardless of the current volume level
- Theme-aware accent colors across all modes
- Toggle between spectrogram and visualizer views

### Batch Editor

The Batch Editor is one window with five tabs, opened from the grid's right-click menu with any number of files selected. Every tab previews its changes before anything is written, and per-file backups are optional throughout.

- **Manual Edit** — Set any tag field (title, artist, album, album artist, year, genre, com