# DUSTBOUND: Mutant Tamers of the Ash

A self-contained, Game Boy-style monster-taming RPG set in a post-apocalyptic wasteland.
Pick a starter mutant (Glowpup, Rustling or Sludgeling), roam the Ash, tame wild mutants,
battle rival tamers, talk your way through stat checks and dice rolls, and keep a journal
of your journey. Everything (graphics, sound, music) is generated in code in a single
HTML file; there are no external assets. Progress is saved in the browser (localStorage).

This folder is a ready-to-deploy **Progressive Web App**: it installs to your home screen,
runs full-screen in portrait, and works offline after the first visit.

## Controls

| Action      | Touch (on-screen)   | Keyboard                   |
|-------------|---------------------|----------------------------|
| Move        | D-pad               | Arrow keys / WASD          |
| A (confirm) | A button            | Z / Enter / Space          |
| B (back)    | B button            | X / Backspace / Esc        |
| Menu        | START               | Shift                      |
| Mute        | -                   | M                          |

## Install on a phone

**iPhone / iPad (Safari):** open the game's URL in Safari, tap the **Share** button,
choose **Add to Home Screen**, then tap **Add**. Launch it from the new "Dustbound" icon.

**Android (Chrome):** open the URL in Chrome, tap the **three-dot menu**, then
**Install app** (or **Add to Home screen**). Chrome may also show an install banner.

After the first launch the game is cached and plays without a connection.

## Deploy to GitHub Pages

1. Put the contents of this folder at the root of a repository (or in `/docs`).
2. Repository **Settings > Pages**: deploy from the branch (root or `/docs`).
3. Open `https://<user>.github.io/<repo>/`. All paths are relative, so a project subpath works.

`.nojekyll` disables Jekyll processing. When you change any file, bump `CACHE_VERSION`
in `sw.js` so installed copies pick up the update (it takes effect on the next launch).

## Files

- `index.html`: the game plus PWA meta tags and service-worker registration
- `manifest.webmanifest`: app name, colours, icons, display mode
- `sw.js`: cache-first offline service worker
- `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png`: pixel-art Glowpup icons
