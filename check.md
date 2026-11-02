# Catch a bad video before it posts

*Keyword: CHECK · Updated November 2026 · Needs: nothing paid. ffmpeg (free).*

Every one of my reels has to pass a set of automatic checks before it's allowed to post. If one check fails, the video doesn't go out. This guide shows you the two easiest checks and the rules behind the rest.

## What you'll have at the end

Two commands that find frozen screens and dead air in any video, plus a short list of your own "never post this" rules.

## Step 1: Write down what you never want posted

Before any code, list three mistakes. Mine include a frozen screen, silence, and a fact with no source.

## Step 2: Catch a frozen screen

This prints `freeze_start` whenever the picture stays still for 1.5 seconds or more:

```bash
ffmpeg -i video.mp4 -vf freezedetect=n=0.003:d=1.5 -map 0:v -f null - 2>&1 | grep freeze_
```

No output means no frozen stretch.

## Step 3: Catch dead air

This prints `silence_start` whenever the sound is quiet (below -40 dB) for 0.6 seconds or more:

```bash
ffmpeg -i video.mp4 -af silencedetect=noise=-40dB:d=0.6 -f null - 2>&1 | grep silence_
```

## The limits I use

| Check | Fails when |
|---|---|
| Length | under 30 or over 45 seconds |
| Frozen screen | nothing changes for over 1.5 seconds |
| Dead air | silence over 0.6 seconds |
| Talking pace | faster than 2.7 words a second |
| Host | the character's mouth is open with no voice for over 0.2 seconds |

Pick your own numbers. The point is to write them down so a machine can say yes or no.

## A trap I fell into

A moving background can hide a dead screen. My stars kept drifting, so the "frozen" check passed, but the actual content hadn't changed for seconds. Now my checker looks at the content area only and ignores the background.

## Step 4: Every claim needs a receipt

For every fact or number in a video, write down where it came from. If you can't point to a source, cut it.

## Step 5: Run the checks every time

Run them after every render, not just when you remember. My checker rejected my own test video more than once before it passed. That's it working.

## Do this today

Run the silence check on your last video and find the longest pause.

---

[All guides](./) · Made by [@alanautomate](https://www.instagram.com/alanautomate/)
