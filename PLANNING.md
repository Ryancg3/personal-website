# Personal Website — Planning Doc

## 1. Goals & Scope

A personal website hosted locally. Typical sections:

- **Home / About** — who you are, what you do
- **Projects** — showcase of work
- **Blog / Writing** *(optional)* — posts, notes
- **Contact** — email, social links, resume/CV

Keep it simple. You can always add later.

---

## 2. Tech Stack Options

### Option A — Plain HTML/CSS/JS (Simplest)

| Aspect | Detail |
|---|---|
| Language | HTML, CSS, JavaScript (vanilla) |
| Build step | None |
| Hosting | Any static file server (`python -m http.server`, `npx serve`) |
| Pros | Zero dependencies, full control, fastest to start |
| Cons | No templating — copy-paste nav/footer on every page |
| Best for | A small site (3–5 pages) you want up in 30 minutes |

### Option B — Static Site Generator (Recommended)

| Tool | Language | Notes |
|---|---|---|
| **Astro** | JS/TS | Content-focused, great performance, easy Markdown |
| **Hugo** | Go (config in TOML/YAML) | Blazing fast builds, huge theme ecosystem |
| **Jekyll** | Ruby | GitHub Pages native, mature |
| **MkDocs Material** | Python | Docs-style, great for a blog/notes focus |
| **11ty (Eleventy)** | JS | Very flexible, minimal opinionation |

| Aspect | Detail |
|---|---|
| Build step | Yes — generates static files |
| Hosting | Same as Option A (output is just static files) |
| Pros | Templating, Markdown support, easy to add pages |
| Cons | One extra tool to learn |
| Best for | Anything with more than a handful of pages, or a blog |

### Option C — Full Framework (React/Vue/Svelte)

| Tool | Language |
|---|---|
| **Next.js** | JS/TS (React) |
| **Nuxt** | JS/TS (Vue) |
| **SvelteKit** | JS/TS (Svelte) |
| **Remix** | JS/TS (React) |

| Aspect | Detail |
|---|---|
| Build step | Yes — can export to static (`next export`, `nuxt generate`, etc.) |
| Hosting | Static export works with any file server |
| Pros | Component model, rich ecosystem, interactive UI |
| Cons | Heavier, more complex, overkill for a simple personal site |
| Best for | If you want to learn the framework or need rich interactivity |

### Option D — Python-Based

| Tool | Language |
|---|---|
| **Pelican** | Python |
| **Lektor** | Python |
| **Flask/FastAPI + Jinja** | Python |

| Aspect | Detail |
|---|---|
| Build step | Pelican/Lektor yes; Flask is a live server |
| Hosting | Static output or run a local server |
| Pros | Stay in Python if that's your language |
| Cons | Smaller community for personal sites vs. JS ecosystem |
| Best for | Python developers who want everything in one language |

---

## 3. Hosting Locally

All options produce (or are) static files. To serve locally:

```bash
# Python (always available on macOS)
python3 -m http.server 8000

# Node
npx serve .

# Or install a tiny server
brew install caddy   # then: caddy file-server --listen :8000
```

Open `http://localhost:8000` in your browser.

---

## 4. Recommendation

**Option B — Astro** is the sweet spot for most personal sites:

- Write content in Markdown
- Component-based layout (nav, footer, cards)
- Exports to pure static files
- Easy to deploy later if you change minds
- Great documentation and community

If you want the absolute simplest thing and don't mind some copy-paste, go **Option A**.

---

## 5. Suggested File Structure

```
personal_website/
├── PLANNING.md          # this file
├── src/
│   ├── layouts/         # page templates
│   ├── components/      # nav, footer, project card, etc.
│   ├── pages/           # actual pages (about, projects, blog)
│   └── styles/          # global CSS
├── public/              # static assets (images, resume.pdf)
└── dist/                # built output (generated)
```

---

## 6. Next Steps

1. **Pick a stack** — which option above feels right?
2. **Define content** — what pages do you want? what goes on them?
3. **Design** — any sites you like for reference? (minimal, brutalist, portfolio-style?)
4. **Build** — scaffold the site and get it running locally

---

## 7. Open Questions

- Do you want a blog, or just static pages?
- Any design inspiration / reference sites?
- What's your primary programming language (for choosing a stack)?
- Do you plan to put this on the internet eventually, or strictly local?
