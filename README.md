# Free Backlink Maker Tool

**Repository name:** `free-backlink-maker-tool`

**Short description (for GitHub repo):**
Free client-side Backlink Maker: generate, ping and submit backlinks via iframe, popup, tab or proxy-based ping. Blogger-ready, mobile-friendly, and privacy-friendly (client-side only).

---

## Overview

This repository contains a lightweight, client-side HTML/CSS/JS Backlink Maker Tool you can embed in Blogger or any static site. The tool helps you generate backlink URLs from templates and open/submit them using several modes: **IFrame**, **Popup**, **Tab**, and **Ping** (via CORS proxies).

It is intended for SEO testing, quick backlink submission, and indexing workflows. The project is intentionally serverless — everything runs inside the browser.

---

## Demo & Quick Install

1. Create a new page or gadget in Blogger (or an `index.html` on any static host).
2. Paste the HTML snippet from `ui/embed.html` (or `index.html`) into the page content area. If using Blogger, use the HTML view.
3. Add `styles.css` to your template or include the CSS inside a `<style>` block (the repo includes a ready-made CSS file).
4. Ensure `backlink-templates.json` and `cors-proxies.json` are available in the same repo or served via raw URLs (optional — defaults are embedded).

---

## Files & Structure

```
free-backlink-maker-tool/
├─ index.html           # Full UI (HTML only block ready for Blogger)
├─ styles.css           # CSS styling (mobile-friendly)
├─ backlink-generator.js# Main JS engine (slot pool, modes, ping etc.)
├─ backlink-templates.json
├─ youtube-backlink-templates.json
├─ cors-proxies.json
├─ README.md            # (this file)
└─ LICENSE
```

---

## Features

- Client-side only — no server needed
- IFrame, Popup, Tab, and Ping modes
- Concurrency control (number of parallel slots)
- Reuse or fresh-window behavior for Popup/Tab
- Shuffle templates and optional auto-repeat
- Download generated URLs as `.txt` or `.csv`
- Copy all successful URLs with one click
- Blogger embed friendly and responsive
- Popup-block detection and fallback messaging

---

## Usage (short)

1. Enter the target URL in the input.
2. Choose a Mode: `IFrame`, `Popup`, `Tab`, or `Ping`.
3. Configure concurrency, shuffle, and repeat settings in Advanced.
4. Click **Generate Backlinks**. The results list will populate with ✓/✗ statuses.
5. Use **Download URLs** or **Copy** to export results.

---

## Modes explained (SEO-friendly)

- **IFrame** — Loads each generated URL inside a hidden iframe. Good for invisible submissions and when you want minimal UI impact.
- **Popup** — Opens each URL in a small popup window. Useful for simulating user visits but may require user permission.
- **Tab** — Opens/reuses tabs to submit URLs. Best for desktop workflows and reusing windows/tabs to keep the number of open windows low.
- **Ping** — Uses a list of CORS proxy templates to fetch the target URL. Fast and invisible; useful when you can't rely on iframe/load events.

---

## SEO & Best Practices

- Use `Ping` for invisible checks and to test index signals quickly via CORS proxies.
- Rotate templates and shuffle to reduce predictability.
- Start with conservative concurrency (3-10) to avoid overwhelming target servers.
- Always check legal/terms-of-service of backlink platforms you use.

---

## How to contribute

- Fork the repo and submit a PR.
- Add new template sources to `backlink-templates.json` in the same format.
- Improve UI/UX and accessibility.
- Report issues using GitHub Issues and tag them `bug` or `enhancement`.

---

## Security & Privacy

- The tool runs entirely on the client — no user URLs are sent to a third-party server by default.
- If you enable remote `cors-proxies.json`, those proxies will receive proxy requests in Ping mode. Only use trusted proxies.

---

## License

MIT License — feel free to reuse and adapt for your own projects.

---

## Contact

Email: backlink.generator.tool@gmail.com

If you want, I can also generate a ready-made `index.html` and `backlink-generator.js` file to push into this repo. Copy/paste friendly and optimized for Blogger.
