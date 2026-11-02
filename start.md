# Run your whole task with one command

*Keyword: START · Updated November 2026 · Needs: Claude Code (paid Claude plan, Pro or above)*

My daily batch starts with one line. Claude reads my rule file, does the work, and saves everything it did to a log. This guide shows you how to do the same.

## What you'll have at the end

One command that runs a job from start to finish, with a dated log file so you can see what happened.

## Step 1: Have a rule file

The command tells Claude to follow your `CLAUDE.md`. If you don't have one yet, start with the **RULES** guide.

## Step 2: Run Claude without the chat window

`claude -p "..."` runs one task and exits. No back-and-forth.

```bash
claude -p "Run this week's report, following CLAUDE.md exactly."
```

## Step 3: Only give it the tools it needs

You can list exactly which tools the AI may use. Anything not on the list, it can't touch.

```bash
claude -p "Run this week's report, following CLAUDE.md exactly." \
  --permission-mode acceptEdits \
  --allowedTools "Read,Write,Edit,Bash"
```

`acceptEdits` lets it save files without stopping to ask you each time. Keep the tools list as short as you can.

## Step 4: Save what it did to a log

Send everything it prints to a file named with today's date:

```bash
DAY=$(date +%Y-%m-%d)
claude -p "Run this week's report, following CLAUDE.md exactly." \
  --permission-mode acceptEdits \
  --allowedTools "Read,Write,Edit,Bash" \
  > "logs/$DAY.log" 2>&1
```

Put those lines in a file called `run.sh`, and starting your job is now `bash run.sh`.

## Step 5: Give it a memory

Ask it to add one line to a file like `logs/done.csv` every time it finishes something, and to read that file before starting. That's how mine never repeats a topic within two weeks.

## Bonus: run it while your laptop is closed

Claude Code can also run a saved task on a schedule in the cloud, so it doesn't need your computer to be on. Set it up once, pick a time, and it runs every day.

## Do this today

Run one small task with `claude -p` and save the output to a log file.

---

[All guides](./) · Made by [@alanautomate](https://www.instagram.com/alanautomate/)
