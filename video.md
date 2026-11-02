# Make a video with code, no editor

*Keyword: VIDEO · Updated November 2026 · Needs: nothing paid. Python, Pillow and ffmpeg (all free).*

There's no video editor behind my reels. Python draws every frame like a picture, and a free tool called ffmpeg stitches the pictures into a video. This guide gets you your first 3-second clip.

## What you'll have at the end

A 3-second vertical video (`square.mp4`) of a pink square sliding across the screen.

## Step 1: Install the tools

```bash
pip install pillow numpy soundfile
```

Then install ffmpeg: on a Mac, `brew install ffmpeg`. On Windows or Linux, use the download from the ffmpeg website.

## Step 2: Understand the idea

A video is just pictures shown fast. Mine are 1080 by 1920 pixels (phone-shaped), 30 pictures every second. Python draws each picture, then hands it straight to ffmpeg, which turns them into an MP4.

## Step 3: Draw and stitch

Save this as `square.py`:

```python
import subprocess
from PIL import Image, ImageDraw

W, H, FPS = 1080, 1920, 30
ff = subprocess.Popen(["ffmpeg", "-y", "-f", "rawvideo", "-pix_fmt", "rgb24", "-s", f"{W}x{H}",
                       "-r", str(FPS), "-i", "-", "-pix_fmt", "yuv420p", "-c:v", "libx264", "square.mp4"],
                      stdin=subprocess.PIPE)
for i in range(FPS * 3):                      # 3 seconds
    img = Image.new("RGB", (W, H), (23, 18, 58))
    d = ImageDraw.Draw(img)
    x = 100 + i * 8                           # move 8 pixels every frame
    d.rectangle((x, 900, x + 120, 1020), fill=(255, 79, 163))
    ff.stdin.write(img.tobytes())
ff.stdin.close()
ff.wait()
```

Run `python square.py` and open `square.mp4`.

## Step 4: Make a sound with no audio files

Every beep in my reels is made by code too. Save this as `beep.py`:

```python
import numpy as np
import soundfile as sf

SR = 24000
t = np.arange(int(SR * 0.15)) / SR           # 0.15 seconds
wave = np.sign(np.sin(2 * np.pi * 880 * t))   # square wave at 880 Hz
wave *= np.exp(-t * 20) * 0.3                 # fade out, keep it quiet
sf.write("beep.wav", wave.astype(np.float32), SR)
```

## Step 5: Build a library, not one-off edits

Once one visual works, make it reusable: a function that takes text and draws a "terminal", another that draws a "before and after". My reels reuse a small set of these scenes, so a new video is mostly choosing scenes and writing the words.

A few tricks from my host character, Bit:
- He's drawn on a tiny 24 by 30 pixel grid, then scaled up so the pixels stay sharp.
- His mouth opens when the voice gets loud and closes when it's quiet.
- He blinks at random times, every 2 to 3.4 seconds, so he feels alive.

## Fonts you can post with

Use fonts with an open licence, like many on Google Fonts (I use Press Start 2P and JetBrains Mono). Check each font's licence before using it.

## Do this today

Render the 3-second square clip.

---

[All guides](./) · Made by [@alanautomate](https://www.instagram.com/alanautomate/)
