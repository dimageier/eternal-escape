# THE ETERNAL ESCAPE
**Dimitri Geier — Immersive Cinematic Artist Website**

A production-ready, single-file HTML experience replicating the luxurious "Escape Room" narrative format of high-end artist sites (inspired by Teyana Taylor's visual album portal) but completely rethemed around Dimitri Geier's Urantia-inspired cosmology, music, and AI-generated visions.

**Live concept**: [dimitrigeier.com/eternal-escape](https://dimitrigeier.com/eternal-escape) (deploy your own copy instantly)

---

## Features

- **Cinematic Dark Cosmic Design**: Deep void blacks, ethereal gold (#E8D5A3), cosmic violet, subtle cyan accents
- **6 Narrative Chambers**: The Finite Self → Nature of God → The Eternal Son → Overcontrol of Supremacy → The Trinity Beyond the Finite → The Light Beyond
- **Interactive "Keys" System**: Click sacred geometry hotspots and "Receive Key" buttons. Progress persisted in localStorage. Full collection unlocks a special transcendence animation.
- **Web Audio Eternal Tones**: Beautiful generative drones when unlocking memories (no external audio files required)
- **AI-Generated Visuals**: Custom hero, album art, chamber backgrounds, and portrait created with Grok Imagine
- **Real Dimitri Media**: Embedded "Endless Fall" music video, dance film DOP work (@dima.tarantino), and three original ComfyUI AI films
- **Prompt Portal**: Fun interactive tool that generates poetic prompts in Dimitri's exact style
- **Schema.org markup** for Artist + MusicAlbum (SEO perfect)
- **Fully Responsive** + excellent mobile experience
- **Zero dependencies** except Tailwind CDN + Google Fonts (instant deploy)

---

## Quick Deploy

### Vercel (Recommended)
1. Drag the entire `the-eternal-escape` folder onto [vercel.com](https://vercel.com)
2. Done. Your site is live in seconds.

### Netlify Drop
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag the folder (or just `index.html` + `assets/`)

### GitHub Pages / Cloudflare Pages
Push the folder to a repo and connect the service.

---

## Customization Guide

### Replacing Images & Videos (Critical)
All media lives in `/assets/`:
- `hero-cosmic.jpg` — Hero background
- `album-eternal-son.jpg` — Main album cover (1:1)
- `chamber-temple.jpg`, `portal-divine.jpg`, `awakening-figure.jpg` — Room backgrounds
- `artist-portrait.jpg` — About section
- `vision-cosmic-*.mp4` — Three AI films used in the Visions grid and modals

**To regenerate better/final assets**:
Use Grok Imagine (or Midjourney/Flux) with prompts like:
> "ethereal cosmic divine album cover, golden light rays, sacred geometry, infinite space, transcendent atmosphere, cinematic, 8k"

For videos, keep using ComfyUI workflows or Runway/Kling. Compress final videos with:
```bash
ffmpeg -i input.mp4 -vcodec libx264 -crf 28 -preset slow -movflags +faststart output.mp4
```

### Adding Real Audio Previews
Currently the site uses the Web Audio API for "Eternal Tones". For authentic previews:

1. Export 12–20 second stems or track excerpts (192kbps)
2. Place in `assets/audio/`
3. In `showMemoryModal()`, replace the `playEternalTone()` button with an `<audio>` element pointing to your file
4. Or embed Spotify track players inside the memory modals (recommended)

### Updating Links
Search the file for:
- Spotify artist/album/track URLs
- SoundCloud
- YouTube (VEVO + dance films)
- Instagram @dima.tarantino
- GitHub

Update any that change.

### The 6 Chambers Content
All chamber titles, quotes (sourced from The Urantia Book), insights, and associated tracks are in the `rooms` object inside `showMemoryModal()` (around line 1206).

### Prompt Portal Templates
Edit the `eternalTemplates` array (around line 1420) to add or refine the poetic outputs.

---

## File Structure

```
the-eternal-escape/
├── index.html          ← Everything lives here (single file)
├── README.md
└── assets/
    ├── hero-cosmic.jpg
    ├── album-eternal-son.jpg
    ├── awakening-figure.jpg
    ├── chamber-temple.jpg
    ├── portal-divine.jpg
    ├── artist-portrait.jpg
    ├── vision-cosmic-1.mp4
    ├── vision-cosmic-2.mp4
    └── vision-cosmic-3.mp4
```

---

## Browser Support
Modern evergreen browsers (Chrome, Safari, Firefox, Edge). The Web Audio API requires a user gesture (click) to start — handled correctly.

---

## Credits & Philosophy

Created for Dimitri Geier by Grok (xAI) — April 2026.

The site embodies the core message of his work: **the finite self awakening to its divine origin through sound, vision, and sacred remembrance.**

> "Escape the Finite. Enter the Infinite."

---

## License
Personal / portfolio use for Dimitri Geier. Feel free to fork and adapt for other artists following the same immersive narrative format.

---

**Need help iterating?**  
Tell Grok: "Improve the room unlock animations" or "Add a real audio player using my hosted MP3s" or "Create a second version with horizontal scroll rooms".

The Eternal Escape is ready. Now go live.