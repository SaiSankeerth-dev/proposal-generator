# Client Proposal Generator

A single-page tool for freelance marketers that turns a few project details into a client-ready proposal, written by Claude in one of three tones: consultative, direct, or ROI-focused.

![Static](https://img.shields.io/badge/stack-HTML%2FCSS%2FJS-blue) ![No backend](https://img.shields.io/badge/backend-none-lightgrey) ![License](https://img.shields.io/badge/license-MIT-green)

## How it works

Fill in client name, business, service type, budget, timeline, goal, and pain point. Pick a tone. The page builds a structured prompt and calls the Anthropic Messages API directly from the browser using **your own API key**, then renders the proposal for copy-paste.

## Getting started

1. Open `index.html` in any browser — no build step, no server.
2. Get an API key at [console.anthropic.com](https://console.anthropic.com).
3. Paste it into the "Your Anthropic API key" field.

Your key is kept in `sessionStorage` for that browser tab only — it is never written to disk, never committed to this repo, and is cleared when the tab closes.

> This is a client-only demo. Because the API call is made straight from the browser, your key is visible in that tab's network requests (to api.anthropic.com only). For production use, proxy the request through a small backend so the key never reaches the browser at all.

## Tech stack

Plain HTML, CSS, and JavaScript. No dependencies, no build tooling, no backend.

## License

MIT
