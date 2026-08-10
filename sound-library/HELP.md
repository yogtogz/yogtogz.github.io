# Sound Library of Babel - Help & Reference Guide

| Element / Symbol | Name / Concept | Description & Behavior |
| :--- | :--- | :--- |
| **62-Character Block** | Frame Architecture | The fundamental building block of audio. Each single frame lasts **0.1 seconds** and consists of exactly 62 characters corresponding to different simultaneous pitch channels. |
| **`|` (Pipe)** | Frame Separator | Used in search or custom input fields to separate sequential frames/blocks. For example, typing `frame1|frame2` creates a multi-frame sequence where each part plays in consecutive 0.1-second intervals. |
| **`0` (Zero)** | Silence / Inactive Slot | Represents silence or an inactive pitch channel. A block filled entirely with zeros (`000...00`) produces no sound for that frame. |
| **Base62 Characters (`a-z`, `A-Z`, `0-9`)** | Pitch Activators | When placed at indices `1` through `61` within a block, any non-zero character activates its corresponding frequency channel (ranging from 200Hz to 4000Hz) to play polyphonic beeps. |
| **Nicknamed Sounds** | Curated Audio Signals | Specific, meaningful sound sequences mapped to human-readable names via `nicknames.json`. Displayed randomly on the home screen and grouped in their own dedicated playlist tab. |
| **"Some" Playlists** | Generated Signal Groups | Automatically generated collections of signals categorized by random 1-to-5 character prefixes (e.g., *Some a7 Signals*). |
| **Download (.wav)** | Client-Side Audio Export | Renders the entire ID sequence in-browser using an `OfflineAudioContext`, packaging it into a clean, uncompressed `.wav` file instantly without needing a backend server. |
| **Oscilloscope Visualizer** | Real-Time Waveform Display | A live canvas visualizer that maps out the mathematical superposition of all active sine wave frequencies playing during playback. |
