# THE ZINE RACK

A terminal-aesthetic email newsletter for the DEEMS universe.

Hosted on GitHub Pages for image serving. Composed and sent via Apple Mail.

---

## REPO STRUCTURE

```
zine-rack/
├── template.html          ← master template (never edit directly)
├── issues/
│   ├── issue-001.html     ← each issue gets its own file
│   ├── issue-002.html
│   └── ...
├── images/
│   ├── issue-001/
│   │   ├── hero.jpg
│   │   ├── featured-1.jpg
│   │   └── featured-2.jpg
│   ├── issue-002/
│   │   └── ...
│   └── ...
└── README.md
```

---

## NEW ISSUE CHECKLIST

### 1. PREP

- [ ] Duplicate `template.html` → `issues/issue-XXX.html`
- [ ] Add your images to `images/issue-XXX/`
- [ ] Optimize images before adding (keep under 600px wide for hero, 300px for featured)

### 2. EDIT (in Phoenix Code)

Search for `✦` in the HTML to find every editable spot:

- [ ] **Date** — Update `2026.XX.XX` in the system status bar
- [ ] **Issue number** — Update `ISSUE XXX / TITLE` under the ASCII header
- [ ] **Intro text** — Write your editorial in the TRANSMISSION section
- [ ] **Hero image** — Update `src` to: `https://it-143.github.io/zine-rack/images/issue-XXX/hero.jpg`
- [ ] **Drop title + description** — Update the zine announcement copy
- [ ] **CTA link** — Point the READ NOW button to the right page
- [ ] **Featured images** — Update both `src` URLs and captions
- [ ] **Signal//Noise links** — Update all three curated link blocks (category, title, URL, description)
- [ ] **Footer links** — Update social/contact links if they've changed

### 3. PUBLISH IMAGES

```bash
git add .
git commit -m "issue XXX"
git push
```

Wait ~1 minute for GitHub Pages to deploy, then verify your images load at:
`https://it-143.github.io/zine-rack/images/issue-XXX/hero.jpg`

### 4. PREVIEW + SEND

- [ ] Open the issue HTML file in Safari
- [ ] Verify all images load (they should now pull from GitHub Pages)
- [ ] `Cmd+A` to select all → `Cmd+C` to copy
- [ ] Open Apple Mail → New Message
- [ ] Make sure you're in Rich Text mode (Format → Make Rich Text)
- [ ] `Cmd+V` to paste
- [ ] Send a test to yourself first
- [ ] Send to your list

---

## IMAGE GUIDELINES

- **Hero image**: 552px wide (will scale down on mobile)
- **Featured images**: 264px wide each
- **Format**: JPG or PNG, keep file sizes reasonable (~100-300kb each)
- **Naming**: Keep it simple — `hero.jpg`, `featured-1.jpg`, `featured-2.jpg`

All image URLs follow this pattern:
```
https://it-143.github.io/zine-rack/images/issue-XXX/filename.jpg
```

---

## SECURITY NOTE

This repo is public. Never commit:
- Email addresses or recipient lists
- Personal drafts or unpublished writing you want to keep private
- Anything you wouldn't want visible on the open web

Keep your mailing list in Apple Mail contacts — completely separate from this repo.

---

```
░▒▓█ DEEMS █▓▒░
```
