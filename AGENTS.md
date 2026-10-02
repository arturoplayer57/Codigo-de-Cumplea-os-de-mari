# AGENTS.md

## Project Overview
A static HTML/CSS/JS birthday card website (Spanish). No build tools, no backend, no dependencies.

## Setup
- The repo files were renamed to match the HTML references: `index` → `index.html`, `style` → `style.css`, `script` → `script.js`.
- Served via nginx:alpine in `docker-compose.base44.yml` on port 3000.
- No credentials or external services required (CDN-loaded fonts and confetti library are fetched client-side).

## Verification
- `curl -s http://localhost:3000/` should return the HTML page with "¡Feliz Cumpleaños!".
- Clicking an envelope opens a modal with a message and triggers confetti.

## Editing
- This is a static site with no live-reload dev server. After editing files, call `reload_preview` so the user sees changes.
