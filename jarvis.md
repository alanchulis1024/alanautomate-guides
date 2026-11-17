# OpenJarvis: your own Jarvis, on your own computer

*Keyword: JARVIS · Updated November 2026 · Needs: a computer with enough memory. The software is free. The spoken briefing needs a voice service key (Cartesia has a free plan).*

OpenJarvis is a free, open-source personal AI that runs on your own computer. It's developed at Hazy Research and the Scaling Intelligence Lab at Stanford SAIL. I didn't make it; I'm sharing it because it's the closest thing to a real Jarvis you can try today.

**Link:** https://github.com/open-jarvis/OpenJarvis (Apache 2.0 license, 16.0k stars when I checked on November 16, 2026)

## What it does

- Chat with an AI that runs on your machine. Cloud services are optional; its own page says it calls the cloud "only when truly necessary".
- A **morning briefing**: it can read the sections you choose (your Gmail, Google Calendar, news feeds, weather and more) and sum up your day.
- It can read that briefing **out loud**. That part uses a voice service (Cartesia or OpenAI), so it needs a key.

## The catch, plainly

- **The AI itself is a download.** The model files run from about 1 GB to about 15 GB. How big a model you can run depends on your computer's memory. The docs say that with 4 GB of memory or less and no graphics card, you shouldn't run a local model at all.
- **The talking part needs a voice key.** Cartesia has a free plan (20K credits a month when I checked). Whether that covers a daily briefing depends on how long yours is.
- **The briefing reads your inbox.** Only connect the accounts you're comfortable with. You choose the sections.

## Step 1: Install it (about 3 minutes on fast internet)

On a Mac or Linux, open the **Terminal** app, paste this line and press Enter:

```bash
curl -fsSL https://open-jarvis.github.io/OpenJarvis/install.sh | bash
```

On Windows, open PowerShell and paste:

```powershell
irm https://open-jarvis.github.io/OpenJarvis/install.ps1 | iex
```

The installer sets up everything it needs, including Ollama (the program that runs the AI) and a small starter model.

There's also a desktop app on the project's Releases page. It needs the part above running in the background.

## Step 2: Ask it one question

Open the chat and ask something simple, like "What can you help me with?". If it answers, it works.

## Step 3 (optional): The morning briefing

The project's Morning Digest guide walks you through it: https://open-jarvis.github.io/OpenJarvis/user-guide/morning-digest/

You'll connect Google (one sign-in covers Gmail and Calendar), add a voice key, and pick a time. Use `--text-only` if you want the briefing as text with no voice key.

## Do this today

Run the install line and ask it one question.
