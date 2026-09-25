# MURDER//AI — The Monsoon Room

A replayable, browser-based AI-style murder mystery game set in a fictional Mumbai mansion.

## Features

- Procedural culprit selection: the killer can change each case.
- Free-text suspect interrogation with intent recognition.
- Dynamic suspect stress and credibility pressure.
- Scene inspection and unlockable evidence.
- Evidence graph that stays consistent with the selected culprit.
- AI-style Case Analyst hints that trade score for guidance.
- Editable detective notebook.
- Final accusation requires a suspect plus supporting evidence.
- Rookie, Detective and Mastermind difficulty modes.
- Responsive layout for laptop and mobile.
- No backend, login, API key or build step required.

## Run locally

Open `index.html` in a modern browser.

For a local web server:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## GitHub Pages

1. Put `index.html` at the repository root.
2. In GitHub, open **Settings → Pages**.
3. Set **Source** to **Deploy from a branch**.
4. Choose `main` and `/ (root)`.
5. Save.

## Optional “real LLM” upgrade

This version deliberately does **not** call an LLM directly from the browser, because embedding an API key in client-side JavaScript would expose it. A future version can route interrogation through a small serverless endpoint (for example Cloudflare Workers or Vercel Functions) while keeping this exact front-end structure.