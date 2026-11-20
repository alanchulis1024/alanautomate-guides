# Make your AI writing sound like you (Humanizer)

*Keyword: HUMAN · Updated November 2026 · Needs: an AI app that supports skills (Claude.ai, Claude Code, Codex and others). The skill is free.*

Wikipedia editors keep a guide called **Signs of AI writing**, which they use to catch AI-generated text. Humanizer is a free skill built on that guide: it rewrites AI-sounding text so it reads like a person wrote it, without changing what it says. It's made by blader. I didn't make it; I'm sharing it because it fixes the thing that makes so many posts sound like ChatGPT.

**Link:** https://github.com/blader/humanizer (MIT license, about 71,000 stars when I checked on November 19, 2026)
**Wikipedia's guide:** https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing

## The five strongest tells (from Humanizer's page)

1. **Not X but Y:** "It's not just a feature, it's a shift."
2. **One-line closers:** "Let that sink in."
3. **Sayings that sound deep:** "At its core, what really matters is..."
4. **A staged run-up:** "Here's the thing." "Honestly?"
5. **Arguing with no one:** "I'm not saying X, but..."

Humanizer checks for 26 patterns in all.

## The catch, plainly

- **It won't beat AI detectors.** Its own page says it edits for human readers, does not try to get past AI detectors, and detectors still flag most of its output.
- **You need an AI app that supports skills** (Claude.ai, Claude Desktop, Claude Code, Codex and others).

## Do it without installing anything

Read the five tells above, open your last post or email, and rewrite every sentence that uses one. That alone fixes most of it.

## Install it

**Claude.ai or Claude Desktop:** on the GitHub page, click **Code → Download ZIP**, then upload it as a skill in Settings.

**Claude Code:**

```text
/plugin marketplace add blader/humanizer
/plugin install humanizer@humanizer
```

Then type `/humanizer`, paste your text and press Enter.

## Do this today

Check your **last post** for the five tells. Rewrite the sentences that use them, and read it out loud: if it sounds like you talking, it's done.
