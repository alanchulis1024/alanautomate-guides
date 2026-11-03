# Run an AI task every morning, laptop closed

*Keyword: CLOUD · Updated November 2026 · Needs: Claude Code, which needs a paid Claude plan.*

Two of my Instagram pages make and schedule their own posts every morning, around 5 AM, while my laptop is closed. Each one is a Claude Code cloud task (a "routine"). This is the setup.

## What you'll have at the end

A task that runs every day at a time you pick, follows your rules, and tells you if anything goes wrong.

## Step 1: One rule file

Put the job in a folder with one file the AI reads first, called `CLAUDE.md`. Write down what to do, where the results go, and what it must never do. Mine starts with rules like "Instagram only. Never post to any other account."

## Step 2: One setup script

The cloud computer starts empty every time. Write one script that installs everything the job needs and prints a single word, like `SETUP_OK`, when it's done. My first cloud run failed because the cloud computer had an older version of Python. The fix went into this one script.

## Step 3: Give it only what it needs

When you create the routine (claude.ai/code/routines), attach only the tools the job uses. Mine gets one outside tool, for scheduling posts, and nothing else.

## Step 4: Test it where it can't do damage

Before the first real run, do a test run that can't post anything: set up, do the work, report back. I did several before letting it post.

## Step 5: Fail means stop and tell me

Decide what happens when something breaks. Mine stops, posts nothing and sends me a notification saying why. That's exactly what happened on its first morning, and it's the reason nothing wrong went out.

## Step 6: Pick the time

Set the schedule (mine is about 5:30 AM). Then check its first few reports yourself.

## Do this today

Write down one task you do every morning, step by step. That list is the start of your rule file.

---

[All guides](./) · Made by [@alanautomate](https://www.instagram.com/alanautomate/)
