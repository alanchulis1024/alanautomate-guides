# Let your AI schedule your posts

*Keyword: SCHEDULE · Updated November 2026 · Needs: a paid Claude plan, and a Metricool plan that allows its Claude connector (check your plan)*

My AI schedules every reel itself. It checks the calendar first, fills only empty slots, and stops if anything looks wrong. This guide shows you the setup.

## What you'll have at the end

Claude connected to your post scheduler, able to list what's scheduled and add new posts into free time slots.

## Step 1: Connect your scheduler to Claude

I use Metricool. In Claude, open the connectors settings, add Metricool, and sign in. Now Claude can use Metricool's tools, like "get scheduled posts" and "create scheduled post".

## Step 2: Ask what's already scheduled

Before adding anything, have Claude look at the calendar:

> "List my scheduled posts for today."

This is the habit that prevents double-posting.

## Step 3: Write down your slots and the rule for full ones

Put this in your `CLAUDE.md` (see the **RULES** guide):

```markdown
## Posting slots
- 09:00, 12:00, 15:00, 18:00 (America/Los_Angeles)
- Check scheduled posts first. Only fill empty slots.
- Never schedule a time that has already passed.
```

## Step 4: Get your video to a public link

A scheduler copies your video from a link, so the file has to be online first. I use a small script that tries one free upload site, then a second one if the first fails. If both fail, it prints `UPLOAD_FAILED`.

## Step 5: Never post on a failure

Add one more rule:

```markdown
- If the upload prints UPLOAD_FAILED, stop. Do not schedule that post.
```

A missed post is fine. A broken post is not.

## Step 6: Say exactly where to post

Tell it which account and which network, and nothing else:

```markdown
- Post to Instagram only, as a Reel.
- Never post to any other account or network.
```

The **SAFE** guide shows how I turn rules like this into a hard block, not just a request.

## Do this today

Connect one scheduler to Claude and ask it to list your scheduled posts.

---

[All guides](./) · Made by [@alanautomate](https://www.instagram.com/alanautomate/)
