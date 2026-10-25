# NEXUS Playground

A responsive, Material 3 Expressive-inspired playground for AI experiments, mini-games, and UI tinkering. Built as a dependency-light static site with vanilla HTML, CSS, and JavaScript.

## Features

- Responsive desktop sidebar and mobile bottom navigation
- Light/dark theme
- Local demo assistant (rule-based; no external AI API is called)
- Three mini-games: reaction test, click rush, and tic-tac-toe
- Interactive color / radius / spacing laboratory with CSS token export
- Prompt builder and local library for saved prompts/themes
- Local activity and score persistence using `localStorage`
- JSON export for saved data
- Reduced-motion preference support and keyboard focus styles
- GitHub Pages deployment workflow
- Expressive design tokens, responsive quick-action dock, shape-reactive states, and variable typography

## Run locally

Open `index.html` in a modern browser, or serve this directory with any static HTTP server.

## Deploy to GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Set the build and deployment source to **GitHub Actions**.
3. Push to the `main` branch. The workflow in `.github/workflows/pages.yml` publishes the site.
4. Open the Pages URL shown in the repository settings.

## Important notes

- The AI Lab is a front-end demo that uses simple local rules, not a real LLM. It does not search the web.
- Do not put private API keys in `index.html`. To connect a real model, use a backend/serverless function that keeps secrets server-side.
- Saved items and game scores are stored in the current browser only. Use the export button to download a JSON snapshot.
- This is an original implementation inspired by Material 3 Expressive design principles; it is not an official Google product.

- See [DESIGN_SYSTEM.md](DESIGN_SYSTEM.md) for the design rationale and a transparent validation checklist.

## License

MIT
