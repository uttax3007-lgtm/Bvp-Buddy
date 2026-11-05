# BVP Buddy — Frontend starter

A responsive, frontend-only first-semester engineering study companion.

## Run locally
1. Extract the ZIP.
2. Open the `bvp-buddy` folder in VS Code.
3. Recommended: install the **Live Server** VS Code extension.
4. Right-click `index.html` → **Open with Live Server**.

You can also open `index.html` directly in a modern browser. A local server is recommended for consistent browser behaviour.

## What's included
- Responsive navy-and-white interface with supplied BVP logo.
- Overview dashboard and subject progress.
- Broad first-semester topic outline with locally saved checkboxes.
- AI study room with selectable explanation modes.
- OpenRouter connection configured by the user in Settings.
- Curated YouTube search links for the requested channels.
- Book references and legitimate Google Books search links.
- 15 learning platforms and documentation/course links.
- Study planner, saved resources, dark mode and local persistence.

## AI setup and API-key safety
This project makes a direct browser request to OpenRouter because it is a frontend-only prototype. In **Settings → AI tutor connection**, paste your own OpenRouter API key and choose a model (default: `openrouter/auto`). The key is stored in `sessionStorage` for the current browser session and is not included in the source files.

**Important:** A browser-only app cannot keep an API key secret. A user can inspect network requests and browser storage. Do not deploy this version publicly with a valuable API key. For public release, put the OpenRouter request behind a server-side API route, add rate limiting and usage controls, and keep the key in server environment variables. Revoke any key that has been pasted into a chat, source code, or public repository and create a new one.

## Data and limitations
- Planner tasks, bookmarks, display name, theme and syllabus progress are stored in the current browser using `localStorage`.
- This is not account authentication or cloud sync. Data does not automatically move between devices.
- AI requests need an internet connection and a valid OpenRouter key.
- YouTube buttons open YouTube search results for the requested channel and subject, rather than assuming a particular playlist URL.
- Book buttons open Google Books search results. Use a library, publisher or legitimate retailer for full texts.
- Subject topics are a broad starter outline, **not a verified official BVDU syllabus**. Replace them with the current college-issued syllabus before relying on them for exams.

## Project structure
```
bvp-buddy/
├── assets/
│   └── bvp-logo.png
├── index.html
├── styles.css
├── app.js
└── README.md
```
