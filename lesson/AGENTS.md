# AGENTS.md

## Project
Static HTML/CSS class portfolio site. No build system, no dependencies, no tests. Open `index.html` in a browser to view.

## Files
- `index.html` — Portfolio landing page linking to all exercise pages
- `*.html` — Individual lesson practice pages (1.html through 11-2.html)
- `css.css` — Shared stylesheet

## Editing
- All pages use **native HTML / CSS / JavaScript** only. No framework, no build step, no bundler.
- **Do NOT use any third-party libraries or CDN resources** (no Bootstrap, no jQuery, no Vue/React, no CDN fonts, no external icon libraries).
- **Icons must use the local iconfont** at `../font/font_5244707_88sf48z3ehl/iconfont.css`. Include it with `<link rel="stylesheet" href="../font/font_5244707_88sf48z3ehl/iconfont.css">` and use class `<i class="iconfont icon-xxx"></i>`.
- **Fetch server data using native `fetch()` API** — no axios, no $.ajax, no other HTTP libraries.
- Some filenames contain Chinese characters — ensure UTF-8 encoding when editing.
- Each HTML page is an independent exercise; changes rarely need to sync across files.
- Update `index.html` when adding or renaming exercise pages.
- All CSS class names, id names, and JS variables must start with `gzh_`.
- Every HTML page must include an HTML comment at the top with format: `<!-- 姓名：郭兹寒，日期：YYYY-MM-DD，功能：页面功能描述 -->`.
- Every prompt must be appended to `guo_prompt.md` before execution (include timestamp, model, prompt content).
