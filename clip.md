# Clip your streams with free AI (OpenShorts)

*Keyword: CLIP · Updated November 2026 · Needs: nothing to start (free online plan). For no watermark and no limit: a computer with Docker and 8 GB+ of memory.*

GTA 6 launches November 19, 2026. If you stream it, you'll have hours of footage and no time to cut it into TikToks, Reels and Shorts. OpenShorts is a free, open-source AI clipper: it watches a long video, picks the best moments and gives you vertical clips with captions. It's made by mutonby. I didn't make it; I'm sharing it because it does what the paid clip apps do.

**Link:** https://github.com/mutonby/openshorts (MIT license, about 9,000 stars when I checked on November 18, 2026)

## What it does

- You paste a **YouTube link** or upload a video file.
- The AI finds the strongest moments and turns each into a **9:16 clip**: cropped to the action or your face, with **captions** and a title.
- Paid clip apps do the same: Opus Clip's Starter plan is $15 a month (from the price table on the OpenShorts page).

## The catch, plainly

- **Free online plan:** your first video is clipped up to 60 minutes, then **20 minutes a month**, and the clips have a **watermark**. No credit card.
- **On your own computer:** free, **no watermark, no limit**, but you need Docker, 8 GB+ of memory and your own Gemini key (Google's AI Studio has a free tier), or a local model.
- **Twitch:** the page talks about YouTube links and file uploads. If you stream on Twitch, download your VOD and upload the file.
- **Clip only your own streams.** Don't clip other people's videos.

## Option A: The free online plan (2 minutes)

1. Open https://www.openshorts.app and sign in.
2. Paste the YouTube link of one of your streams (or upload the file).
3. Wait for the clips, then download the ones you like.

## Option B: On your own computer (no watermark, no limit)

1. Install **Docker Desktop** (free for personal use) and open it.
2. Open the Terminal app (Mac) or PowerShell (Windows), paste these lines one at a time and press Enter:

```bash
git clone https://github.com/mutonby/openshorts.git
cd openshorts
docker compose up --build
```

3. Open **http://localhost:5175** in your browser.
4. Go to **Settings** and paste your Gemini key (get one at https://aistudio.google.com/apikey).
5. Open **Clip Generator** and upload one stream.

The first start downloads a lot, so give it time. Without a graphics card it's slower (the page says an 8-minute video takes 5 to 8 minutes on a normal processor).

## Do this today

Clip **one old stream** before you go live with GTA 6. Then you'll know it works, and your launch-night clips are one paste away.
