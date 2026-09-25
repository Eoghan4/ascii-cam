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
