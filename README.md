# 🧱 Blocktopia

A Roblox-style blocky hub world with minigames, built with plain JavaScript and [Three.js](https://threejs.org/). No build step, no ads, no paywalls. Everything runs offline once loaded.

## Play

Open `index.html` in a browser (double-click works, since Three.js is bundled in `lib/`), or serve the folder:

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

**Controls:** WASD / arrows to move · Space to jump · drag to look · **F** smack · **E** sell · Esc returns to the hub.
On phones you get an on-screen joystick plus Jump / Smack / Sell buttons.

## Games

Walk into a portal in the hub:

| Portal | What it is |
| --- | --- |
| **Coin Grab** | Collect the most coins in 30 seconds against 3 rival bots. |
| **Obby** | Race 3 bots up an obstacle course to the gold platform. |
| **Tag Run** | Survive 30 seconds against 3 chasers. Jump over them. |
| **Brainrot** | Buy brainrots from the conveyor, earn passive income, steal from rival bases, upgrade, and sell. Step on the green pad to collect your earnings. |
| **Shop** | Spend coins on shirts, hats, faces, and trails. |

Coins and cosmetics are saved in `localStorage`.

## Install as an app (PWA)

Host the folder over HTTPS, open it once, then use your browser's **Install** / **Add to Home Screen**. A service worker caches the game so it works fully offline afterward.

### Host on GitHub Pages

1. Push this repo to GitHub.
2. **Settings → Pages → Deploy from a branch → `main` / root.**
3. Open `https://<your-user>.github.io/<repo>/`.

> If you change any file, bump `V` in `sw.js` so installed copies pick up the update.

## Project layout

```
index.html            the whole game (HTML + CSS + JS)
lib/three.min.js      Three.js r128 (MIT, see lib/THREE-LICENSE.txt)
sw.js                 offline cache
manifest.webmanifest  install metadata
icons/                app icons
```

## Ideas / roadmap

- Base shield, rebirths, and gear for Brainrot
- More minigames and cosmetics
- Desktop (Electron/Tauri) and phone (Capacitor) wrappers

## License

MIT, see [LICENSE](LICENSE). Three.js is MIT-licensed by its authors.
