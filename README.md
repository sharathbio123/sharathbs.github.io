# sharathbs.github.io

Personal portfolio site for **Sharath B S** — Computational Chemist specializing in AI drug
discovery, cheminformatics, and molecular modeling.

## Development

This site is a static portfolio built with [Vite](https://vitejs.dev/).

### Prerequisites

- Node.js 18+ (Node 22 is available in the Cloud Agent VM)

### Setup

```bash
npm install
```

### Run locally

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser. Vite provides hot module
replacement for fast iteration while editing `index.html`, `src/`, and styles.

### Build for production

```bash
npm run build
npm run preview
```

The production build is written to `dist/`. For GitHub Pages deployment from this user-site repo,
publish the contents of `dist/` to the repository root (or configure a GitHub Actions workflow).

## Project structure

```
index.html          # Main portfolio page (CV content)
src/
  main.js           # Navigation and small UI helpers
  styles/main.css   # Site styles
vite.config.js      # Vite dev/build configuration
```

## Cursor Cloud specific instructions

- **Install / refresh deps:** `npm install` (also used as the VM update script on startup).
- **Dev server:** `npm run dev` — listens on port **5173** with `host: true` for container access.
- **Production check:** `npm run build` then `npm run preview` on port **4173**.
- There are no automated tests or linters configured yet; validation is manual via dev server and
  production build.
- Content lives in `index.html`; update sections there when the CV changes.
