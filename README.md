# ASCII Webcam (Terminal)

This script captures webcam video and renders each frame as ASCII art directly in your terminal.
It uses an expanded character ramp for smoother grayscale shading.

## Setup

```bash
pip install -r requirements.txt
```

## Run

```bash
python ascii_cam.py
```

Optional arguments:

- `--camera 0` webcam index (try 1, 2, ... if needed)
- `--fps 20` target terminal refresh rate
- `--scale 1.0` terminal width scale from 0.2 to 1.0
- `--backend auto` camera backend: auto, dshow, msmf, any

Examples:

```bash
python ascii_cam.py --camera 0 --fps 24 --scale 0.8
python ascii_cam.py --backend dshow
```

Stop with `Ctrl+C`.

If you get frame-grab issues on Windows, close other apps using the camera
(Teams, Zoom, browser tabs), then run with `--backend dshow` or `--backend msmf`.

## Interactive Matrix Rain (Webcam Motion)

This script renders Matrix-style falling characters in the terminal.
When motion is detected from your webcam (for example, moving your hand),
nearby rain streams are pushed sideways.

Run:

```bash
python ascii_matrix_rain.py
```

Useful options:

- `--fps 24` render refresh rate
- `--scale 1.0` terminal width scale from 0.4 to 1.0
- `--density 0.82` stream density from 0.1 to 1.0
- `--motion-threshold 28` motion sensitivity threshold (lower = more sensitive)
- `--backend auto` camera backend: auto, dshow, msmf, any

Example:

```bash
python ascii_matrix_rain.py --backend dshow --fps 30 --density 0.7 --motion-threshold 22
```

## ASCII Mic Visualizer

This project also includes a live microphone-based ASCII audio visualizer.

Run:

```bash
python ascii_audio_viz.py
```

Useful options:

- `--fps 30` render refresh rate
- `--samplerate 44100` audio sample rate
- `--blocksize 2048` audio frame size
- `--bars 64` number of spectrum bars
- `--gain 8.0` input gain before compression
- `--device "Microphone Name"` choose a specific input device

Stop with `Ctrl+C`.
