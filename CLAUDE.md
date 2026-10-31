# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Universals** is a collection of single-page HTML multi-tools that execute simultaneous actions in new browser tabs. It currently hosts two solutions:
1. **Universal Search** (`search/index.html`): Multi-engine simultaneous search.
2. **Universal Paywalls** (`paywalls/index.html`): Multi-provider paywall bypass and archive runner.
3. **Universals Hub** (`index.html`): Main landing page directing users to `/search/` or `/paywalls/`.

## Architecture

- **Zero dependencies**: Pure HTML, CSS, and vanilla JS across all pages.
- **Independent pages**: Each HTML file (`index.html`, `search/index.html`, `paywalls/index.html`) is completely standalone and functional offline or served via GitHub Pages.
- **Theming**: Shared CSS variables for dark and light modes, synchronized via `localStorage.getItem('theme')`.

## Key Data Structures

### Universal Search (`search/index.html`)
- `categories[]`: Category objects with `name` and `engines[]`
- `searchEngines`: Flattened array of all search engines
- `defaultEngines[]`: Default checked engine IDs

### Universal Paywalls (`paywalls/index.html`)
- `categories[]`: Category objects with `name` and `providers[]`
  - Each provider has `id`, `name`, and `buildUrl(targetUrl)`
- `paywallProviders`: Flattened array of all providers
- `defaultProviders[]`: Default checked provider IDs

## LocalStorage Keys

- `theme`: `'light'` or `'dark'` (shared across all pages)
- `selectedEngines`: JSON array of selected engine IDs
- `selectedPaywalls`: JSON array of selected paywall provider IDs

## URL Parameters

- `?url=` (or `?link=`): Pre-fills article URL in Universal Paywalls (`/paywalls/`).
- `?q=` (or `?query=`): Pre-fills search query in Universal Search (`/search/`).
