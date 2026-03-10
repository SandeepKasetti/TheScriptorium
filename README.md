# 📖 The Scriptorium — Personal Study Vault

<p align="center">
  <img src="docs/preview.png" alt="The Scriptorium" width="800"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Deployed-GitHub%20Pages-brightgreen?style=for-the-badge&logo=github" />
  <img src="https://img.shields.io/badge/Built%20With-HTML%20%2F%20CSS%20%2F%20JS-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Animations-Anime.js-purple?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Active-gold?style=for-the-badge" />
</p>

<p align="center">
  <a href="https://sandeepkasetti.github.io/TheScriptorium">🌐 Live Site</a> &nbsp;·&nbsp;
  <a href="#-adding-a-new-volume">➕ Add a Volume</a> &nbsp;·&nbsp;
  <a href="#-structure">📁 Structure</a>
</p>

---

## ✨ What is The Scriptorium?

**The Scriptorium** is a personal, self-hosted knowledge compendium — a beautifully designed study vault where complex topics are broken down into focused flashcard decks. Each "Volume" is a curated set of flashcards on a specific subject, built for deep understanding rather than shallow memorization.

> *"Do not study to remember. Study until forgetting becomes impossible."*

---

## 🎨 Design Highlights

- **Dark, atmospheric UI** with a gold accent palette (`#e8a020`)
- **Custom spotlight cursor** that reacts to hover and click
- **Anime.js** powered modal transitions and scroll-reveal animations
- **Dot-grid background** with ambient glow orbs and scan-line effects
- **Fully responsive** — works on desktop and mobile
- **Syne + DM Mono** typeface pairing for a refined editorial feel
- **No frameworks, no build tools** — pure HTML, CSS, and vanilla JS

---

## 📚 Current Volumes

| # | Volume | Topic | Cards |
|---|---|---|---|
| Vol. I | Machine Intelligence | RAG — Retrieval Augmented Generation | 15 cards |
| Vol. II | *Coming Soon* | — | — |

---

## 🗂️ Structure

```
TheScriptorium/
├── index.html          ← Main vault homepage (deck browser)
├── RAG.html            ← Vol. I flashcard deck
├── docs/
│   └── preview.png     ← Screenshot for README
└── README.md
```

---

## ➕ Adding a New Volume

The homepage is designed to be easily extended. To add a new flashcard deck:

**Step 1 — Add a card in `index.html`**

Find the `deck-grid` div and copy this block:

```html
<div class="deck-card"
  style="--card-accent:#YOUR_HEX; --card-rgb:R,G,B;"
  data-vol="Vol. II · Your Subject"
  data-title="Your Topic Title"
  data-tagline="A one-line description."
  data-desc="A longer description of what this deck covers."
  data-count="X cards"
  data-href="your-deck.html">
  <div class="deck-glow"></div>
  <p class="card-vol">Vol. II · Your Subject</p>
  <h2 class="card-title-text">Your Topic Title</h2>
  <p class="card-tagline">A one-line description.</p>
  <p class="card-desc">Longer description here.</p>
  <div class="card-foot">
    <span class="card-count">X cards</span>
    <button class="enter-link" onclick="window.location='your-deck.html'">Open Flashcards →</button>
  </div>
</div>
```

**Step 2 — Update the tally**

```html
<span class="sec-tally" id="sec-tally">03 in collection</span>
```

**Step 3 — Create `your-deck.html`**

Model it after `RAG.html` — same card flip mechanics, same dark theme.

**Step 4 — Push to GitHub**

```bash
git add .
git commit -m "Add: Vol. II — Your Topic"
git push
```
GitHub Pages deploys automatically within ~60 seconds.

---

## 🚀 Running Locally

No build step needed — just open the file:

```bash
# Clone the repo
git clone https://github.com/SandeepKasetti/TheScriptorium.git
cd TheScriptorium

# Open in browser (any of these work)
open index.html           # macOS
start index.html          # Windows
xdg-open index.html       # Linux
```

Or use VS Code's **Live Server** extension for hot reload.

---

## 🌐 Deployment (GitHub Pages)

This site is deployed automatically via **GitHub Pages**:

1. Go to repo **Settings → Pages**
2. Source: `main` branch → `/ (root)` folder
3. Live at: `https://sandeepkasetti.github.io/TheScriptorium`

Every `git push` to `main` triggers an automatic re-deploy.

---

## 🛠️ Tech Stack

| Layer | Choice | Why |
|---|---|---|
| Markup | HTML5 | Semantic, no framework needed |
| Styling | CSS3 (custom properties) | Full control, zero overhead |
| Animations | [Anime.js v3](https://animejs.com) | Smooth spring physics |
| Fonts | [Syne](https://fonts.google.com/specimen/Syne) + [DM Mono](https://fonts.google.com/specimen/DM+Mono) | Editorial + technical pairing |
| Hosting | GitHub Pages | Free, fast, auto-deploy |

---

## 📄 License

MIT License — feel free to fork and build your own Scriptorium.

---

<p align="center">
  <em>Knowledge that compounds.</em>
</p>
