# Stream GTA 6 with free, live AI subtitles (LocalVocal)

*Keyword: GTA · Updated November 2026 · Needs: a computer (Windows, Mac or Linux) with OBS Studio. Both are free.*

GTA 6 launches November 19, 2026. If you stream it, live subtitles help viewers who watch with the sound off, and viewers who speak another language. LocalVocal is a free add-on for OBS that listens to your voice and types what you say, live, on your screen. It runs on your own computer. It's made by Roy Shilkrot (Locaal). I didn't make it; I'm sharing it because it's the easiest free way I found to add live AI captions to a stream.

**Link:** https://github.com/locaal-ai/obs-localvocal (GPL-2.0 license, about 1,700 stars when I checked on November 18, 2026)

## What it does

- Turns your voice into **captions in real time**, in **100 languages**.
- Shows them **on screen** in OBS (as a text source), or saves them to a .txt or .srt file.
- Can **translate** your captions to major languages.
- Runs **on your computer**: its page says "No GPU required, no cloud costs".

## The catch, plainly

- **It only works inside OBS, on a computer.** There's no version for a console. If you stream straight from your PlayStation or Xbox, you'll need to stream through OBS on a computer instead.
- **It starts with an English-only model** (Tiny.en). For another language, pick a bigger model from its menu; it downloads by itself.
- **Small models make more mistakes.** Bigger models are more accurate but need a faster computer.

## Step 1: Install OBS (if you don't have it)

Download OBS Studio from https://obsproject.com (free) and set up your stream as usual.

## Step 2: Install LocalVocal

1. Go to https://github.com/locaal-ai/obs-localvocal/releases
2. Download the installer for your computer:
   - **Windows:** "generic" works on every PC ("NVidia" or "AMD" if you have that graphics card).
   - **Mac:** "ARM64" for Apple chips (M1, M2...), "Intel" for older Macs.
3. Run it, then restart OBS.

## Step 3: Turn on captions

1. In OBS, add a **Text** source to your scene (this is where captions appear).
2. Right-click your **microphone** in the Audio Mixer and choose **Filters**.
3. Add the **LocalVocal Transcription** filter and pick your Text source as the output.
4. Talk. Your words should appear on screen.

For another language or translation, change the model and the translation options in the same filter.

## Do this today

Install it and say **one test line** into your mic before you go live with GTA 6. If the words show up on screen, you're ready.
