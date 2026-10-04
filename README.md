# personal-website

Ryan Gumsheimer's personal website, built with [Astro](https://astro.build).

## Development

Requires Node.js 22.12 or newer.

```bash
npm install      # install dependencies
npm run dev      # start the dev server at http://localhost:4321
npm run build    # build the static site into dist/
npm run preview  # serve the built site locally
```

## Structure

```
src/
├── layouts/Base.astro   # shared <head>, fonts, global styles
├── pages/index.astro    # homepage
└── styles/global.css    # colours and base styles
public/                  # static files copied as-is (favicon, images, CV)
```

## Deployment

Hosted on Cloudflare Pages, which rebuilds the site on every push to `main`.

| Setting          | Value           |
| ---------------- | --------------- |
| Framework preset | Astro           |
| Build command    | `npm run build` |
| Output directory | `dist`          |
