# vite-project

A Vite + React 19 + TypeScript 6 single-page starter application.

## What it is

A standard Vite scaffolded welcome page customized with the official Vite
hero artwork, a working counter demo, and responsive light/dark styling.

## Stack

- React 19
- TypeScript 6
- Vite 8 (Rolldown-powered)
- ESLint 10 with React Hooks + React Refresh rules

## Run

```bash
npm install
npm run dev
```

For a production build:

```bash
npm run build
```

`npm run build` runs `tsc -b` (TypeScript project build) followed by
`vite build` (optimized production bundle output to `dist/`).

## Application flow

1. `index.html` provides the root `<div id="root">`.
2. `src/main.tsx` mounts React into that element using `createRoot`,
   wrapped in `StrictMode`.
3. `src/App.tsx` renders the page and contains the only interactive
   behavior: a counter stored in React state using `useState`. Clicking
   the button increments the displayed count.
4. `src/App.css` and `src/index.css` define the responsive page design:
   centered hero area, layered Vite/React artwork, documentation and
   community-link sections, responsive behavior below 1024px, and an
   automatic dark mode via `prefers-color-scheme`.

## Key files

| File | Role |
| --- | --- |
| `src/main.tsx` | React bootstrap / entry point |
| `src/App.tsx` | Main UI component and counter interaction |
| `src/App.css`, `src/index.css` | Styling and responsive layout |
| `vite.config.ts` | Enables Vite's React plugin |
| `eslint.config.js` | Linting configuration |
| `tsconfig*.json` | TypeScript project/build configuration |

## Pushing from a corporate network

If `git push` fails with an HTTP 403 from Zscaler (see `PUSH-README.md`),
your network blocks GitHub's `git-receive-pack` endpoint. Use a network
or VPN that allows GitHub git-HTTP write operations.
