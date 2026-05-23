# Video Editor Portfolio — Deploy Guide

## Quick Start (local)
Open `index.html` directly in your browser. No build step needed.

---

## Before deploying — replace all placeholders

Search for `[REPLACE:` in `index.html` and fill in every occurrence:

| Placeholder | What to put |
|---|---|
| `[REPLACE: your name]` | Your full name |
| `[REPLACE: your city]` | Your city |
| `[REPLACE: YouTube video ID]` | The ID from a YouTube URL (e.g. `dQw4w9WgXcQ`) |
| `[REPLACE: video title]` | Title of the project |
| `[REPLACE: client name]` | Client or brand name |
| `[REPLACE: short title]` | Reel/short title |
| `[REPLACE: Formspree ID]` | Get it at formspree.io — create a free form |
| `[REPLACE: Instagram URL]` | Full Instagram profile URL |
| `[REPLACE: LinkedIn URL]` | Full LinkedIn URL |
| `[REPLACE: Behance URL]` | Full Behance URL |
| `[REPLACE: YouTube channel URL]` | Full YouTube channel URL |
| `[REPLACE: site domain]` | Your domain, e.g. `yourname.com` |
| `[REPLACE: client logo N]` | Path to client logo image |

### Adding YouTube thumbnails
For each video card, uncomment the `<img>` tag and replace the video ID:
```html
<img src="https://img.youtube.com/vi/YOUR_VIDEO_ID/maxresdefault.jpg"
     alt="Project Title" loading="lazy" width="1280" height="720">
```
Then remove the `<div class="video-placeholder">` below it.

### Adding your photo
Replace the `<div class="photo-placeholder">` block in the About section with:
```html
<img src="assets/photo.jpg" alt="Your Name" loading="lazy" width="600" height="800">
```

### Adding client logos
Replace each `<div class="client-slot">` placeholder with:
```html
<div class="client-slot">
  <img src="assets/clients/client1.png" alt="Client Name" loading="lazy" width="100" height="40">
</div>
```

---

## Deploy to GitHub Pages (free)

1. Create a new repo on github.com (e.g. `yourname.github.io`)
2. Push your files:
```bash
git init
git add .
git commit -m "Initial portfolio"
git remote add origin https://github.com/YOUR_USERNAME/yourname.github.io.git
git push -u origin main
```
3. Go to repo Settings → Pages → Source: `main` branch → Save
4. Your site will be live at `https://yourname.github.io` in ~1 minute

---

## Deploy to Netlify (free, custom domain)

1. Go to [netlify.com](https://netlify.com) → Add new site → Deploy manually
2. Drag and drop the entire `portfolio-ed` folder
3. Your site is live instantly with a random `.netlify.app` URL
4. To add a custom domain: Site settings → Domain management → Add domain

---

## Deploy to Vercel (free, fastest CDN)

```bash
npm i -g vercel
vercel
```
Follow the prompts. Done.

---

## Setting up the contact form (Formspree)

1. Go to [formspree.io](https://formspree.io) → Create account (free)
2. New Form → give it a name → copy the form ID (looks like `xpzgkwbn`)
3. In `index.html`, replace `[REPLACE: Formspree ID]` with that ID
4. Done — submissions go straight to your email, no backend needed

---

## File structure

```
portfolio-ed/
├── index.html          ← entire site (single file)
├── assets/
│   ├── photo.jpg       ← your portrait photo
│   ├── og-cover.jpg    ← social share image (1200×630px)
│   └── clients/
│       ├── client1.png
│       └── ...
└── README.md
```
