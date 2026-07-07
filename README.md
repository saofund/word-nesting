# Nested

**Learn a language by diving through its own words.**

Look up a word, read its definition — then tap any word *inside* that definition to dive into *its* definition, and keep going. Every word is a door. It's the monolingual-immersion method turned into something you can actually play with: you stay inside the target language the whole way down.

🔗 A single static HTML file. No build, no backend, no tracking. Open `index.html` and it just works.

## Core features

- **Infinite dive** — every word in a definition, example, or synonym list is clickable; tapping it opens that word's own definition.
- **Dive trail** — a breadcrumb of the path you've taken; tap any step to jump back.
- **Pronunciation** — real human audio when available, browser speech synthesis as fallback.
- **Save words** — star a word to keep it; saved words live in your browser (`localStorage`, capped at 500 words). Nothing leaves your device.

## Language support

The concept is language-agnostic. **v1 ships with English**, because the underlying [Free Dictionary API](https://dictionaryapi.dev) currently only serves reliable data for English. Other languages arrive once a multilingual data source is wired in (see roadmap).

## Roadmap / TODO

- [ ] **More languages** — swap in [Wiktionary's REST API](https://en.wiktionary.org/api/rest_v1/) to genuinely support any language (needs HTML parsing; bigger lift).
- [ ] **AI assist** — optional per-word "explain simply / examples / etymology" via an LLM, behind a backend proxy (no API keys in the browser).
- [ ] **Sign in with Google** — sync saved words across devices (needs a backend / Firebase / Supabase). Local-only for now.
- [ ] Export saved words (CSV / Anki).

## Run locally

Just open `index.html` in a browser. Or serve it:

```
python -m http.server 8000   # then open http://localhost:8000
```

## Deploy

It's a static site — any static host works.

- **Vercel**: import this repo at [vercel.com/new](https://vercel.com/new) and deploy. `vercel.json` is included.
- **GitHub Pages**: enable Pages on the `main` branch (root) in repo Settings.

## License

MIT
