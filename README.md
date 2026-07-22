# trevero-card-assets

Public image hosting for finished Trevero social cards.

## Why this repo is public

Buffer does not store uploaded images. When a scheduled post publishes, Buffer
fetches the image from a URL at that moment. That URL must therefore be public,
permanent, and serve the image file itself. This repo provides it.

Every image here is a finished card that is already bound for a public social
feed. Nothing is exposed that was not already going to be published.

## What belongs here

**Only rendered PNG cards**, written by `scripts/publish_cards.py` in the
private `trevero-marketing` repo. Nothing else — no transcripts, no drafts,
no notes, no client material. `.gitignore` blocks everything by default and
re-admits `cards/**/*.png` only.

Do not add files here by hand.

## Layout

```
cards/<batch>/<slug>.png
```

Served at:

```
https://raw.githubusercontent.com/calebgrimes/trevero-card-assets/main/cards/<batch>/<slug>.png
```

These URLs are permanent. Do not rename or delete a file once a calendar row
references it — a scheduled post would publish without its image.
