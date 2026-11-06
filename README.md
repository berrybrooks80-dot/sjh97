# SON JIHOO · Player File

PWA player profile for **Son Jihoo (손지후)** — Busan Marina U9–U10 (2023–24), Suwon Eagles U11–U12 (2025–26). Built on the same system as the Ko Dohyun player file.

## Files

| File | Purpose |
|---|---|
| `index.html` | The app — markup, CSS, JS and the 15-video data array |
| `plan.html` | Production brief (Korean) — goals, IA, data status, open items |
| `manifest.webmanifest` | Install metadata |
| `sw.js` | Offline cache (`sonjihu-v1`) |
| `icons/` | Home-screen icons |

## Deploy

1. Public repo `sonjihu` → upload everything, keeping `icons/` as a folder.
2. Create `.nojekyll` (drag-and-drop skips dotfiles) via *Add file → Create new file*.
3. **Settings → Pages → main / (root) → Save.**
4. `https://<user>.github.io/sonjihu/`

## Install

iPhone: Safari → Share → *Add to Home Screen*. Android: Chrome ⋮ → *Install app*. The ⤓ button in the top bar walks through it.

## Adding videos

Search `var DATA = [` in `index.html` and add a row:

```js
{"id":"YOUTUBE_ID","cat":"suwon","t":"Suwon Eagles vs X","s":"Tournament","v":0,"k":"FULL","y":"2026","d":"2026.11.14"}
```

`cat` is `marina` or `suwon`. Games sort newest-first automatically. Bump `sonjihu-v1` in `sw.js` after every edit or installed copies keep the old shell.

## Data honesty rule

Unverified values are shown as `—` / `pending`, never estimated. See `plan.html` §04 for what is sourced and what still needs the association record.
