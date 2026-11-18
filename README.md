# Ahmedabad 2047 – Scenario Game

A single-page quiz (`index.html`). After the player answers the questions, the page shows one of three scenarios and plays that scenario's film.

## Files

- `index.html` – the whole app (no build step, no `videos/` folder needed)
- `README.md` – this file

## Scenario videos

Films are hosted on YouTube (unlisted) and embedded on the results screen. Each scenario plays only its own video.

| Scenario | Key | YouTube link |
|---|---|---|
| Manufacturing-led | `A` | https://youtu.be/fhHgNJSf31s |
| Productivity-led | `B` | https://youtu.be/daosXmIEFks |
| Globally Connected | `C` | https://youtu.be/NNNCnxGrcPo |

### Changing a video

Open `index.html`, find the `PATHWAYS` list near the top of the script, and replace the video ID (the part after `youtu.be/`):

```js
A: { ..., video: "fhHgNJSf31s" },
B: { ..., video: "daosXmIEFks" },
C: { ..., video: "NNNCnxGrcPo" }
```

The embed uses `youtube-nocookie.com`, so no other change is needed.

## Deploy on GitHub Pages

1. Put `index.html` (and this README) in the repo root.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then Save.
4. Open the URL GitHub shows after a minute or two.

## Notes

- Works on mobile and desktop; the video keeps a 16:9 shape and scales to the screen.
- Videos are unlisted: anyone with the link can watch, but they won't appear in YouTube search.
- Each YouTube video must have **Allow embedding** turned on (YouTube Studio → video → Show more), or it will show as unavailable.
- The page needs an internet connection to play the videos.
