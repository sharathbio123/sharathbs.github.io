# AGENTS.md

## Cursor Cloud specific instructions

### Product

Single static portfolio site (Vite 6): `index.html`, `src/style.css`, assets in `public/`. Deploys to GitHub Pages on push to `main` via `.github/workflows/deploy.yml` → `gh-pages` branch.

### Services

| Service | Command | Port |
|---------|---------|------|
| Dev server | `npm run dev` | 5173 |
| Production preview | `npx vite preview --host 127.0.0.1 --port 4173` | 4173 |

No database, API, Docker, or backend. Google Fonts load from CDN (optional; degrades gracefully).

### Lint / test

No ESLint, Prettier, or test runner is configured. `package.json` only defines `dev` and `build`.

### Build

`npm run build` → `dist/`. CI uses Node 22 and `npm ci`.

### Key assets

- Profile photo: `public/My_Photo.jpg` (fallback: `public/profile.svg`)
- CV PDF: `public/CV.pdf` — nav **CV** opens `/CV.pdf` in a new tab

### Dev server note

Use tmux for long-running `npm run dev` (see cloud agent shell guidance). Vite binds `host: true` on port 5173 per `vite.config.js`.
