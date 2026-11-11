---
layout: post
title: "RSS Feeds for (almost) every ARDSounds Podcast"
tags: [Podcasts, RSS, ARDSounds, ARD Audiothek, GitHub Actions, Python]
description: "A small project that turns all ~1,550 ARDSounds podcasts into plain RSS feeds for your podcast app, and how to fork it for your own needs."
---

## Why?

I like listening to podcasts from the German public broadcasters, but I like listening to them in *my* podcast app. ARDSounds (formerly the ARD Audiothek) has a huge catalogue, yet many shows don't come with a public RSS feed you could simply paste into your app of choice. When I checked, only about a quarter of the shows had one from their broadcaster.

So I wrote a little tool that builds those feeds myself. It started as a Python reimplementation of the PHP project [ARD-Audiothek-RSS](https://github.com/matztam/ARD-Audiothek-RSS) by matztam and slowly grew from "a feed for my favourite shows" into "a feed for every show".

👉 **The result lives here: [gboeer.github.io/ardsounds-feeds](https://gboeer.github.io/ardsounds-feeds/)**

## Using the feeds

No account, no app, no setup:

1. Open the [feed page](https://gboeer.github.io/ardsounds-feeds/) and search for a show (or a station like "Bayern 2" or "WDR 5").
2. Hit the copy button next to the feed URL.
3. Paste it into your podcast app's "add podcast by URL" dialog. Done.

A few extras:

* **Lots of shows at once:** every station has its own OPML file, and there's one with [all podcasts](https://gboeer.github.io/ardsounds-feeds/opml/all.opml). Most podcast apps can import OPML, so you can subscribe to a whole station in one go.
* **Official feeds:** if the broadcaster does offer its own feed, it's linked as "Offizieller Feed" next to the show, in case you prefer the original.
* **Fresh every morning:** all feeds are rebuilt daily and contain the 100 newest episodes of each show.

## How it works (the short version)

There's no server involved. A [GitHub Actions](https://docs.github.com/actions) workflow runs once a day and:

* asks the ARD's GraphQL API for every show with at least one episode,
* builds an RSS feed for each of them (episodes whose audio file has vanished are dropped, since your app couldn't play them anyway),
* renders the overview page and the OPML files,
* and publishes everything as static files on GitHub Pages.

Feeds from the previous run are cached, so a normal daily run only has to look at what's new and takes a few minutes. If ARD has a hiccup with one show, the last working version of its feed simply stays online. Everything is plain Python standard library, no dependencies.

## Make it your own

The code is open source (GPL-3.0) at [github.com/gboeer/ardsounds-feeds](https://github.com/gboeer/ardsounds-feeds), and you can run your own copy without ever leaving the browser.

### Fork it on GitHub

1. **Fork** the repository.
2. In your fork, go to **Settings → Pages** and set the source to **GitHub Actions**.
3. Open the **Actions** tab. GitHub disables workflows in fresh forks, so enable them there.
4. Start the workflow **"Fetch Podcast RSS Feeds"** with **Run workflow**. The very first run takes around a quarter of an hour, because it has to build every feed from scratch.

Your feeds then show up at `https://<your-username>.github.io/ardsounds-feeds/`, and they keep updating every day on their own.

### Tweak the settings

All settings live in `podcasts.json`, which you can edit right on GitHub (pencil icon, commit, done):

```json
{
  "default_latest": 100,
  "exclude": ["<show_id>"],
  "shows": [
    { "show_id": "8e6d4d6fa453e7f7", "name": "Kalk & Welk", "latest": 20 }
  ]
}
```

* `default_latest`: how many of the newest episodes go into each feed.
* `exclude`: shows you don't want a feed for.
* `shows`: your favourites. They appear in their own "Ausgewählt" section at the top of the page and can get their own name or episode count. `"latest": null` means *all* episodes.

The `show_id` is the last part of a show's URL on ARDSounds: for `https://www.ardsounds.de/sendung/kalk-und-welk/urn:ard:show:8e6d4d6fa453e7f7/` it's `8e6d4d6fa453e7f7`. A small check runs on every change to `podcasts.json`, so a typo or a stray comma gets caught before the daily run.

Only interested in your own handful of shows? In `.github/workflows/fetch-feeds.yml`, change `python fetch_feeds.py` to `python fetch_feeds.py --listed-only`, and the workflow only builds the feeds listed under `shows`. The page itself (texts, colours, layout) lives in `templates/`.

### Or run it locally

If you'd rather keep things on your own machine, clone the repo. All you need is Python 3:

```bash
git clone https://github.com/gboeer/ardsounds-feeds.git
cd ardsounds-feeds

# A single feed, printed to stdout (here: the 10 newest episodes of "Kalk & Welk")
python3 ardaudiothek_rss.py --show 8e6d4d6fa453e7f7 --latest 10

# A tiny local feed server: http://localhost:8000/?show=8e6d4d6fa453e7f7&latest=10
python3 ardaudiothek_rss.py --serve --port 8000

# The batch run for the shows in podcasts.json, plus the overview page
python3 fetch_feeds.py --listed-only
python3 build_pages_index.py
```

The local server is handy if you have a Raspberry Pi or a NAS at home: point your podcast app at it and you get feeds for any show, built on demand.

## Wrapping up

It's a small project, but it scratches an itch: all of ARDSounds in whatever podcast app I like. If you find a show that doesn't work or have an idea, feel free to open an issue on [GitHub](https://github.com/gboeer/ardsounds-feeds). Happy listening! 🎧
