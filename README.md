## Resonus

A free, browser-based music player for discovering and streaming tracks and internet radio — no installs, no downloads.

🔗 **Live site:** [resonus-five.vercel.app](https://resonus-five.vercel.app)

## Features

- 🔍 **Search & discover** — search for songs and browse recommendations pulled from the Jamendo catalog.
- 📻 **Internet radio** — tune into live stations sourced from the Radio Browser API.
- 💾 **Personal library** — save tracks to a library that's kept in your browser, so your saved songs are there when you come back.
- 👤 **Accounts** — sign in to link providers, set a display name, and manage your library from a dedicated account page.
- 📋 **Live changelog** — release history and recent commits, pulled straight from GitHub.

## Tech stack

Resonus is built as static, dependency-light HTML/CSS/JavaScript pages with no custom backend:

- **[Jamendo API](https://developer.jamendo.com/)** — track search, recommendations, and streaming audio.
- **[Radio Browser API](https://www.radio-browser.info/)** — internet radio station discovery.
- **[Supabase](https://supabase.com/)** — authentication and identity linking (`@supabase/supabase-js`, loaded via CDN).
- **`localStorage`** — persists the user's saved track library and UI preferences client-side.
- **GitHub REST API** — powers the live changelog page.

## Project structure

```
resonus/
├── code/
│   ├── index.html       # Main player: search, browse, radio, saved library
│   ├── account.html     # Account management (auth, linked providers, library actions)
│   └── changelog.html   # Auto-generated changelog (GitHub API)
└── vercel.json          # Vercel config (outputDirectory: code)
```

## Deployment

The site is deployed on **Vercel** (see [`vercel.json`](vercel.json), which points to `code/` as the output directory), with pushes to `main` deploying automatically.

## License

No license has been specified yet.
