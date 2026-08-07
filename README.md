# 🎨 Sketchbook — p5.js Showcase

A minimal, static gallery for showcasing p5.js sketches — live, running previews included, not just screenshots. Built with plain HTML, CSS, and JS. No frameworks, no build step, no dependencies to install. Just edit an array and push.

**[→ View Live Site](#)** hxrii.github.io/Sketchbook-p5Js/

---

## Features

- **Live embedded previews** — sketches actually run inside each card via iframe, not static screenshots
- **Zero build step** — one HTML file, open it and it works
- **Fully static** — deploys straight to GitHub Pages, no server, no config
- **Easy to extend** — add a new sketch by adding one object to an array
- **Responsive grid** — adapts from desktop down to mobile
- **Neobrutalist design** — thick borders, hard offset shadows, high-contrast palette

---

## Adding a Sketch

All sketches live in a single array near the bottom of `index.html`, inside the `<script>` tag:

```js
const SKETCHES = [
  {
    title: "Recursive Tree",
    file: "recursive-tree.js",
    description: "A branching structure drawn with recursion.",
    link: "https://editor.p5js.org/username/full/sketchID",
    tag: "INTERACTIVE",
    dims: "600×600",
    embed: "https://editor.p5js.org/username/embed/sketchID",
    thumb: ""
  },
  
];
```

| Field | What it does |
|---|---|
| `title` | Sketch name shown on the card |
| `file` | Fake filename shown in the card's titlebar, e.g. `"boids.js"` |
| `description` | One or two sentences about what it does |
| `link` | Where the card links to when clicked (full sketch page) |
| `tag` | Short label, e.g. `"GENERATIVE"`, `"WEBGL"`, `"SOUND"` |
| `dims` | Canvas size shown if there's no `embed`/`thumb` |
| `embed` | URL for a **live, running preview** inside the card (see below) |
| `thumb` | Static preview image, used only if `embed` is empty |


## Customizing the Theme

All colors live in one place at the top of the `<style>` block:

```css
:root{
  --cream: #296275;
  --ink: #C9F2C7;
  --panel: #000000;
  --yellow: #1b534f;
  --cyan: #3FE0D0;
  --orange: #2f793c;
  --border: 3px;
  --shadow-off: 7px;
  --open: #81FBB8;
  --minimise:#FCCF31;
  --close: #F55555;
}
```
Swap these five colors to reskin the entire site — nothing else needs to change.

---

## Tech Stack

- HTML5
- CSS3 (custom properties, `color-mix`, `aspect-ratio`, no preprocessor)
- Vanilla JavaScript (no dependencies, no bundler)


---

## Structure

```
.
├── index.html      
└── README.md
└── sketches.js
```

---

## License

MIT — do whatever you want with it.

---

Built with p5.js, no frameworks harmed in the making of this repo.