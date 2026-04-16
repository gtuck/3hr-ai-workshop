# 3hr AI Workshop Slides

Slide deck for the **Getting Started with AI** 3-hour workshop, built with [Slidev](https://sli.dev/).

## Tech Stack

- [Slidev](https://sli.dev/) (`@slidev/cli`)
- Vue 3 components in slides
- `apple-basic` theme

## Prerequisites

- Node.js 20+ (Netlify is configured for Node 20)
- npm

## Install

```bash
npm install
```

## Local Development

Start the slide dev server:

```bash
npm run dev
```

Slidev will open the presentation in your browser (default is typically `http://localhost:3030`).

Main slide entry:

- `slides.md`

## Build

```bash
npm run build
```

This project has `download: true` enabled in `slides.md`, so build/export requires Playwright Chromium.

If you see this error:

```text
The exporting for Slidev is powered by Playwright, please install it via `npm i -D playwright-chromium`
```

install Playwright Chromium once:

```bash
npm i -D playwright-chromium
```

Then run build again.

## Export Slides

Export to PDF/PPTX (depending on Slidev config and CLI options):

```bash
npm run export
```

## Deploy

This repo is configured for static deployment from `dist`:

- Netlify config: `netlify.toml`
- Vercel config: `vercel.json`

Typical deployment flow:

1. Install dependencies
2. Run `npm run build`
3. Publish `dist`

## Project Structure

```text
.
├─ slides.md
├─ components/
│  └─ Counter.vue
├─ pages/
│  └─ imported-slides.md
├─ snippets/
│  └─ external.ts
├─ netlify.toml
└─ vercel.json
```

## Useful Links

- Slidev docs: https://sli.dev/
- Slidev syntax guide: https://sli.dev/guide/syntax.html
