# Make a free website for your guides

*Keyword: SITE · Updated November 2026 · Needs: a free GitHub account.*

Every guide people get in my DMs lives on a small website, one page per guide plus an index. It's hosted free by GitHub Pages, and each page is a plain text file. This page you're reading is one of them.

## What you'll have at the end

A website at `yourname.github.io/your-site/` with one page per guide.

## Step 1: Make a public repository

On GitHub, create a new repository (a project folder), set it to **Public**, and tick "Add a README file". GitHub Pages is free for public repositories. Only put things in it you're happy for anyone to read.

## Step 2: One file per page

Add a file for each page, ending in `.md`. Write in plain text: `#` makes a title, `##` makes a heading, a blank line starts a new paragraph. The README becomes your home page, so list your pages there with links.

## Step 3: Pick a look

Add a file called `_config.yml` with one line:

```yaml
theme: jekyll-theme-cayman
```

## Step 4: Turn it on

Go to the repository's Settings → Pages. Under "Build and deployment", choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then Save. After a minute or two, your site is live. A page called `video.md` shows up at `.../video`.

## Step 5: Scan before you publish

Everything here is public, so search your files for anything that looks like a key, a token or an email before you push. I scan every guide first, because keys have ended up in the wrong place before. A simple start, run in your site's folder:

```bash
grep -rnE "sk-|ghp_|AKIA|BEGIN PRIVATE KEY|@gmail\.com" .
```

No output is what you want.

## Do this today

Write your first page: one thing you know how to do, in five short steps.

---

[All guides](./) · Made by [@alanautomate](https://www.instagram.com/alanautomate/)
