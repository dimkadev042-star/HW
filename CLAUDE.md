# CLAUDE.md

This file provides guidance to Claude Code when working in this repository.

## Overview

A minimal static "Hello, World!" website: a single `index.html` with inline CSS. No build step, no dependencies, no JavaScript, no tests.

## Run locally

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000. This server is also defined in `.claude/launch.json` (configuration `site`).

## Deployment

GitHub Pages serves the site from the `main` branch root:
https://dimkadev042-star.github.io/HW/

Pushing to `main` publishes changes (usually live within a minute or two). There is no staging branch, so check changes locally before pushing.

## Conventions

- Keep it dependency-free: plain HTML with styles inline in `<style>` unless the site grows enough to justify separate files.
- `index.html` must stay at the repo root, because Pages serves from `/`.
- Asset paths must be relative (e.g. `style.css`, not `/style.css`), because the site is served under the `/HW/` subpath.
