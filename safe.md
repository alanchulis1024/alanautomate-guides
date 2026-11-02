# Keep your automation from leaking or misposting

*Keyword: SAFE · Updated November 2026 · Needs: nothing paid.*

When an AI posts for you, the scary mistakes aren't ugly videos. They're a password showing on screen, or a post going to the wrong account. These are the guardrails I use.

## What you'll have at the end

A short list of what your automation must never touch, a quick way to scan for secrets, and one manual switch that keeps you in control.

## Step 1: Show the code, hide the key

Never show a real password or key, not in a video, a screenshot or a shared file. Use a placeholder instead:

```python
API_KEY = "<your-api-key>"
```

Type example code by hand. Don't paste it from your real project.

## Step 2: Scan for secrets before you share

Before you post or publish anything, search it for things that look like keys or emails. A simple start, run in the folder you're about to share:

```bash
grep -rnE "sk-|ghp_|AKIA|BEGIN PRIVATE KEY|@gmail\.com" .
```

No output is what you want. My videos go further: every word drawn on screen is scanned automatically, and any hit fails the video.

## Step 3: Write down what it must never touch

List the accounts and networks your automation may use, and the ones it must never use:

```markdown
## Allowed
- Instagram, my one account.

## Never
- My other accounts.
- Any other network.
```

## Step 4: Turn the rule into a block

A rule in a text file is a request. A check that runs right before posting is a block. Mine compares the post against the list and stops if:
- it targets any network other than the allowed one,
- it targets the wrong account,
- the account name shown in the video doesn't match the account it's posting to.

I added that last one after I almost posted under a slightly different account name.

## Step 5: Only approved media

Keep a list of the clips and images you've approved. If something isn't on the list, it doesn't go in a video.

## Step 6: Keep one human switch

Fully automated, except one switch. Mine is a single setting that starts as "off". Until I watch the first videos and turn it on, nothing can post, no matter what the AI does.

## Do this today

Write down which accounts your automation must never touch.

---

[All guides](./) · Made by [@alanautomate](https://www.instagram.com/alanautomate/)
