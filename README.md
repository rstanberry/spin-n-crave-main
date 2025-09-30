# Spin & Crave

Spin & Crave is a small Vite + React + TypeScript demo app that lets users spin a wheel to pick a food category, then shows nearby restaurants and ordering links. It uses Tailwind CSS and a shadcn-style component set.

This README follows common GitHub conventions and explains how to get the project running locally, how to build and preview a production bundle, and how to contribute.

---

## Table of contents

- [Requirements](#requirements)
- [Quick start](#quick-start)
- [Available scripts](#available-scripts)
- [Development notes](#development-notes)
- [Deploying / Previewing production build](#deploying--previewing-production-build)
- [Architecture & key files](#architecture--key-files)
- [Contributing](#contributing)
- [License](#license)

---

## Requirements

- Node.js 18+ (recommended via nvm)
- npm (bundled with Node) or pnpm if you prefer
- A modern browser (Chrome, Firefox, Safari)

---

## Quick start

Clone the repository and install dependencies:

```bash
# clone the repo
git clone <YOUR_REPO_URL>
cd spin-n-crave-main

# install dependencies
npm install
# or, if you prefer pnpm
# pnpm install
```

Start the development server (Vite):

```bash
npm run dev
```

Open http://localhost:8080/ (or the URL printed in your terminal) to view the app with hot reload.

---

## Available scripts

Run these from the project root.

- `npm run dev` - Start Vite dev server with hot reload for local development.
- `npm run build` - Create an optimized production build in the `dist/` folder.
- `npm run preview` - Serve the production build locally using Vite preview.
- `npm run lint` - Run ESLint across the repository.

Example:

```bash
# build and preview the production bundle
npm run build
npm run preview
# then open the URL printed by the preview command
```

---

## Development notes

- This project uses:
  - React + TypeScript
  - Vite for fast development and production builds
  - Tailwind CSS for styling
  - shadcn-style UI components in `src/components/ui`

- Key developer entry points:
  - `src/main.tsx` — App bootstrap
  - `src/pages/Index.tsx` — Main page and layout
  - `src/components/SpinWheel.tsx` — The spin wheel component
  - `src/components/RestaurantResults.tsx` — Restaurant list, pagination, and provider links

- Toasts: `src/hooks/use-toast.ts` exposes `useToast()` and `toast()` helpers used across the UI.

- Icons: `lucide-react` is used for lightweight SVG icons.

---

## Deploying / Previewing production build

1. Build the app:

```bash
npm run build
```

2. Preview the build locally:

```bash
npm run preview
```

3. Deploy the `dist/` folder to any static host (Netlify, Vercel, GitHub Pages, or your preferred CDN). The `index.html` is self-contained and references assets in `dist/`.

---

## Architecture & key files

A short map of important files/folders:

- `index.html` — App HTML template
- `src/main.tsx` — React entry
- `src/pages/Index.tsx` — Main page with header and layout
- `src/components/SpinWheel.tsx` — Wheel UI and spin logic
- `src/components/RestaurantResults.tsx` — Restaurants UI, pagination, provider links, geolocation
- `src/hooks/use-toast.ts` — Toast helper used by components
- `src/index.css` — Tailwind + custom CSS tokens
- `tailwind.config.ts` — Tailwind configuration
- `vite.config.ts` — Vite configuration

---

## Contributing

Contributions are welcome. Suggested workflow:

1. Fork the repository on GitHub.
2. Create a feature branch: `git checkout -b feat/your-feature`.
3. Make changes and commit with clear messages.
4. Open a pull request against the `main` branch.

Please run linting and the dev server before opening a PR.

---

## License

This project does not include a license file by default. Add a `LICENSE` file to make the licensing explicit.

---
