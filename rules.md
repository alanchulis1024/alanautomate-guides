# Write the rule file your AI follows

*Keyword: RULES · Updated November 2026 · Needs: Claude Code (paid Claude plan, Pro or above)*

My whole video page runs from one text file. Every morning, my AI reads it first and follows it step by step. This guide shows you how to write your own.

## What you'll have at the end

A file called `CLAUDE.md` that tells Claude how to do one job you repeat every week, the same way every time.

## Why one file works

Claude Code reads a file called `CLAUDE.md` in your project folder at the start of every session. Anything you write there, it treats as your standing instructions. So instead of explaining your job again each time, you write it down once.

## Step 1: Make the folder and the file

Make a folder for your job (for example `weekly-report`). Inside it, create a plain text file named exactly `CLAUDE.md`.

## Step 2: Write the facts that never change

Start with what your AI must always know. Mine has things like posting times and the time zone.

```markdown
# Weekly report

## Facts
- Report goes out every Monday.
- Time zone: America/Los_Angeles.
- Sources: the sales sheet and the support inbox summary.
```

## Step 3: Write the rules, most important first

Rules near the top win. Put the "never do this" rules first.

```markdown
## Rules (top rule wins)
1. Never invent a number. If you can't find it, write "not found".
2. Keep it under one page.
3. Plain words. No jargon.
```

## Step 4: Write the job as numbered steps

This is the part that saves the most time. Write the steps in the order you'd do them yourself.

```markdown
## Steps
1. Read last week's report so you don't repeat it.
2. Collect this week's numbers from the sources.
3. Write three short sections: what went well, what didn't, what's next.
4. Save it as reports/<date>.md.
```

## Step 5 (optional): Turn a checklist into a "skill"

A skill is a reusable checklist your AI pulls in when it needs it. It lives at `.claude/skills/<name>/SKILL.md` and starts with a short description of when to use it:

```markdown
---
name: hook-writer
description: Use when writing the first line of a video or post.
---
Write 5 different opening lines. Keep each under 8 words. Pick one.
```

Then in `CLAUDE.md`, say which skill to use at which step: "At step 3, use the hook-writer skill."

## Do this today

Pick one thing you do every week. Write a 10-line `CLAUDE.md` for it: 3 facts, 3 rules, 4 steps.

---

[All guides](./) · Made by [@alanautomate](https://www.instagram.com/alanautomate/)
