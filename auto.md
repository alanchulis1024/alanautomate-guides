# Send a DM when someone comments a word

*Keyword: AUTO · Updated November 2026 · Needs: an Instagram professional account. The tool is free and open source; hosting depends on your plan.*

When someone comments one word on my posts, they get a public reply and a DM with the guide they asked for, in about two seconds. I didn't write the tool. I set up a free, open-source one called InstaAuto and changed a few things. This is how.

## What you'll have at the end

One word, one link. Someone comments the word, and your link lands in their DMs automatically.

## Step 1: Pick one word and one link

Before any setup, decide the word (short, easy to spell) and the one thing it sends. Mine: comment VIDEO, get the guide to making a video with code.

## Step 2: Set up the tool

InstaAuto is open source (MIT license): [github.com/ayuuxh2/insta-p8](https://github.com/ayuuxh2/insta-p8). Its README walks you through it. It needs a web host and a database. I used Vercel and Supabase. Then connect your Instagram account in its dashboard.

## Step 3: Lock it down first

Free templates are built for everyone, so check what's public before you go live. I made the dashboard accept only my account, and I removed a storage folder that let anyone upload or delete files.

## Step 4: Add the automation

Make a new automation: when a comment says your word, reply publicly ("Check your DMs!") and send a DM with your link. Add a second one for people who type the word in a DM instead.

## Step 5: Match the whole comment only

My first version had a bug waiting to happen. A normal comment like "Great video!" contains the word *video*, so it would have sent the guide to someone who never asked. Now the word has to be the whole comment.

## Step 6: Test with a second account

Comment the word and DM the word from another account. Also comment normal sentences that *contain* the word and check nothing fires. If nothing arrives at all, check your Instagram settings: Settings → Messages and story replies → Message controls → Connected tools → Allow access to messages. My app was ready long before Instagram was actually sending it anything.

## Do this today

Write down your one word and the one link it should send.

---

[All guides](./) · Made by [@alanautomate](https://www.instagram.com/alanautomate/)
