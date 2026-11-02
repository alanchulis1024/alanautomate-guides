# Make a free voiceover on your laptop

*Keyword: VOICE · Updated November 2026 · Needs: nothing paid. Python and two free downloads.*

The voice in my reels costs nothing per video. It runs on my own computer with a free voice model called Kokoro. This guide gets you your first sentence.

## What you'll have at the end

A file called `hello.wav` with a natural voice reading your sentence.

## Step 1: Install it

You need Python 3. Then, in a terminal:

```bash
pip install kokoro-onnx soundfile
```

## Step 2: Download the two model files

From the kokoro-onnx project on GitHub (Releases, "model-files-v1.0"), download:

- `kokoro-v1.0.onnx` (the voice model)
- `voices-v1.0.bin` (the voices)

Put both in the same folder as your script.

## Step 3: Write five lines of Python

Save this as `hello.py`:

```python
import soundfile as sf
from kokoro_onnx import Kokoro

k = Kokoro("kokoro-v1.0.onnx", "voices-v1.0.bin")
samples, rate = k.create("Hi! This voice is free and runs on my laptop.",
                         voice="af_heart", speed=0.88, lang="en-us")
sf.write("hello.wav", samples, rate)
```

Run it with `python hello.py`, then play `hello.wav`.

`speed=0.88` is a little slower than normal. I use it because my videos are for people who are new to this.

## Step 4: Pick a voice with samples, not guesses

Render the same sentence in two voices (for example `af_heart` and `am_michael`), listen to both, and ask a friend which one they'd keep listening to. Then use that voice every time. A page that changes voices feels like a different page.

## Step 5: Fix words it says wrong

If it mispronounces a name, spell it the way it sounds in the spoken line only, and keep the correct spelling on screen. For example, a voice may need "Q A" instead of "QA".

## Licence note

Check the licence on the model's page before you use it for business. Rules can change.

## Do this today

Generate one sentence with Kokoro and listen to it.

---

[All guides](./) · Made by [@alanautomate](https://www.instagram.com/alanautomate/)
