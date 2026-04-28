# ✦ experimentalCutStar — Lyric Dissector

A browser-based MP3 lyric dissection tool. Drop an MP3 file, and it automatically extracts the embedded lyrics (ID3 `USLT` tag) and gives you a rich analysis view.

## Features

- **Drag & Drop MP3 upload** — no server required, runs entirely in your browser
- **Auto-extract lyrics** from embedded ID3 tags (USLT / USLT:XXX frames)
- **Manual paste fallback** — if no lyrics are embedded, paste them in manually
- **Section detection** — auto-labels `[Verse]`, `[Chorus]`, `[Bridge]`, `[Outro]`, etc.
- **Line view** — numbered lines with clean lyric display
- **Word view** — hover any word to see syllable count + how many times it appears
- **Annotations mode** — shows syllable count + rhyme fingerprint per line
- **Word frequency chart** — top 20 most-used non-stop words in the sidebar
- **Live search** — highlights matching words across the full lyrics
- **Copy to clipboard**
- **Album art + metadata** — displays title, artist, album, year from ID3 tags

## Usage

Just open `index.html` in any modern browser — no install, no dependencies, no build step.

```bash
open index.html
```

Then drop an MP3 onto the page.

### Embedding lyrics in an MP3

Use a tag editor like **Kid3**, **MP3Tag**, or **MusicBrainz Picard** to add `USLT` (Unsynchronized Lyrics) to your MP3 before loading it here.

### Manual section labels

If you're pasting lyrics manually, wrap section names in brackets:

```
[Verse 1]
Your lyrics here…

[Chorus]
Repeat the hook…

[Bridge]
Something different…
```

## Tech

Pure HTML + CSS + vanilla JS. Uses [`jsmediatags`](https://github.com/nickwebh/jsmediatags) (CDN) for ID3 tag parsing.

---

*experimentalCutStar — cut every line apart.*
