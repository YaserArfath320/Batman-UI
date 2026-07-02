# The Dark Knight — Batman Fan Page

A cinematic, interactive Batman-themed landing page built with React, Vite, and Framer Motion. Features a custom HTML5 canvas spotlight effect that follows the user's cursor, revealing a hidden image beneath as they move across the hero section.

---

## Live Demo

🔗 [https://comfy-granita-16a97c.netlify.app/](https://comfy-granita-16a97c.netlify.app/)

---

## Preview

> Move your cursor across the hero section to reveal the Batman image through a glowing, animated spotlight trail.

---

## Features

- **Interactive Canvas Spotlight** — a smooth, glowing cursor trail built with the HTML5 Canvas API. The trail reveals a top image over a background image using compositing techniques.
- **Framer Motion Animations** — staggered entrance animations for the navbar, headings, description text, and CTA button.
- **Cinematic Typography** — Google Fonts including *Bebas Neue*, *Cinzel*, and *Cormorant Garamond* for a dark, editorial feel.
- **Gotham-themed Navbar** — fixed, glassmorphism-style navbar with gold hover underline effects.
- **Dark aesthetic** — deep blacks, crimson reds, and gold accents throughout.

---

## Tech Stack

| Tool | Purpose |
|---|---|
| [React 19](https://react.dev/) | UI framework |
| [Vite 8](https://vitejs.dev/) | Build tool & dev server |
| [Framer Motion](https://www.framer.com/motion/) | Animations |
| HTML5 Canvas API | Cursor spotlight effect |
| Google Fonts | Cinematic typography |

---

## Project Structure

```
vite-project/
├── public/
│   ├── images/
│   │   ├── twoo.jpg          # Background image (bottom layer)
│   │   └── 1199261.jpg       # Reveal image (top layer, shown through spotlight)
│   ├── favicon.svg
│   └── icons.svg
├── src/
│   ├── assets/
│   │   └── hero.png
│   ├── components/
│   │   ├── Hero.jsx          # Main hero section with canvas spotlight
│   │   ├── Hero.css          # Hero styles
│   │   ├── Navbar.jsx        # Top navigation bar
│   │   └── Navbar.css        # Navbar styles
│   ├── App.jsx
│   ├── App.css
│   ├── index.css
│   └── main.jsx
├── index.html
├── package.json
└── vite.config.js
```

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v18 or higher
- npm

### Installation

```bash
# Clone the repository
git clone <your-repo-url>
cd vite-project

# Install dependencies
npm install

# Start the development server
npm run dev
```

Then open [http://localhost:5173](http://localhost:5173) in your browser.

### Build for Production

```bash
npm run build
```

The output will be in the `dist/` folder.

### Preview Production Build

```bash
npm run preview
```

---

## How the Spotlight Effect Works

1. Two images are loaded — a background (`twoo.jpg`) and a reveal image (`1199261.jpg`).
2. On every animation frame, the canvas draws the background image first.
3. An offscreen canvas renders a trail of circles following the smoothed cursor position, each fading out toward the tail.
4. Using `source-in` compositing, the reveal image is masked to only show through those circles.
5. The masked result is drawn on top of the background.
6. A radial golden glow is painted at the cursor head for a bat-signal effect.

---

## License

This is a fan-made project for personal/educational use. Batman and all related characters are property of DC Comics / Warner Bros.
