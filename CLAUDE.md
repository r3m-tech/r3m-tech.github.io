# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static landing page for **R3M Tech** (r3m.tech), a Brazilian software development company. The site is a single-page HTML file with no build system, no dependencies, and no JavaScript framework.

## Architecture

- **`index.html`** — The entire site: markup, CSS (inline `<style>`), and JS (inline `<script>`)
- **`assets/`** — Logo images (light/dark variants) and favicon files
- **`favicon.ico`** — Root favicon

There is no package.json, no build step, no test suite, and no linter. To preview, open `index.html` in a browser or use any static file server.

## Key Design Details

- **Dark/light theme**: Controlled via `data-theme` attribute on `<html>`, with CSS custom properties in `:root` and `[data-theme="dark"]`. Theme preference is saved to `localStorage` and falls back to `prefers-color-scheme`.
- **Logo swap**: Light and dark logo variants are both in the DOM; CSS toggles visibility based on theme.
- **Font**: Montserrat (loaded from Google Fonts).
- **No external JS or CSS frameworks** — everything is self-contained in the single HTML file.
