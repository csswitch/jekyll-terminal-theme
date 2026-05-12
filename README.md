# jekyll-terminal-theme

[![License: csswitch Commercial](https://img.shields.io/badge/license-csswitch%20commercial-blue.svg)](./LICENSE)
[![Buy on Gumroad](https://img.shields.io/badge/Buy-%2449-brightgreen.svg)](https://csswitch.gumroad.com/l/csswitch-terminal)
[![Live Demo](https://img.shields.io/badge/demo-live-orange.svg)](https://csswitch.github.io/jekyll-terminal-theme/)

> **⚠️ License notice:** This theme is source-available but **not free to use**.  
> Viewing and learning from the code is welcome. Deploying it on any live site requires a [paid license](https://csswitch.gumroad.com/l/csswitch-terminal).  
> See [LICENSE](./LICENSE) for full terms.

> A retro terminal-style Jekyll theme for developer blogs and portfolios. Green phosphor on black, `ls -la` post listings, CRT scanlines — zero paid competition in this aesthetic.

**[Live Demo](https://devshelf.github.io/jekyll-terminal-theme)** · **[Buy on jekyllthemes.io](#)** · **[Buy on Gumroad](#)**

---

![Terminal theme screenshot — green phosphor on black, ls -la post list](./screenshots/terminal-green-desktop.png)

---

## Features

- 🟢 **4 color schemes** — green (default), amber, blue, white — switch in `_config.yml`
- 📺 **CRT scanlines + phosphor glow** — toggleable visual effects
- ⚡ **Boot sequence animation** — shows once per browser session
- ⌨️ **`ls -la` post listing** — date | title | tags in a monospace grid
- 🔤 **Blinking cursor** in the header prompt
- 🌑 **True dark background** — `#0a0a0a` base (not fake dark gray)
- 📱 **Responsive** — works on mobile, adapts the terminal aesthetic
- 🚫 **No jQuery** — 100% vanilla JS (~4 KB)
- ✅ **GitHub Pages compatible** — only whitelisted plugins
- 🔍 **SEO ready** — `jekyll-seo-tag`, Open Graph, canonical URLs
- 📡 **RSS feed** via `jekyll-feed`
- 📋 **Copy buttons** on all code blocks
- ⌨️ **Keyboard shortcuts** — `/` for search, `Alt+H` for home
- 📄 **4 layouts** — home, post, page, default
- 🏷️ **Tags page** — grouped tag index
- 📅 **Archive page** — posts grouped by year

---

## Screenshots

| Desktop — Green | Desktop — Amber |
|-----------------|-----------------|
| ![Green scheme desktop](./screenshots/terminal-green-desktop.png) | ![Amber scheme desktop](./screenshots/terminal-amber-desktop.png) |

| Mobile | Post view |
|--------|-----------|
| ![Mobile view](./screenshots/terminal-mobile.png) | ![Post layout](./screenshots/terminal-post.png) |

---

## Installation

### Quick start (copy & use)

1. **Download** the ZIP from [Gumroad](#) or [jekyllthemes.io](#)
2. Unzip into your project folder
3. Edit `_config.yml` with your details
4. Run locally:

```bash
bundle install
bundle exec jekyll serve
```

5. Push to GitHub — enable Pages under repo Settings → Pages → `main` branch → `/root`

### Use as a remote theme

Add to your `_config.yml`:

```yaml
remote_theme: devshelf/jekyll-terminal-theme
```

And to your `Gemfile`:

```ruby
gem "jekyll-remote-theme"
```

---

## Configuration

All options live in `_config.yml` under the `terminal:` key:

```yaml
terminal:
  username: "user"          # shown in header prompt: user@hostname:~ $
  hostname: "blog"
  prompt_char: "$"          # or ">" or "❯"
  color_scheme: "green"     # green | amber | blue | white
  show_boot_sequence: true  # false to skip the boot animation entirely
  scanlines: true           # CRT scanline overlay
  crt_glow: true            # phosphor glow on text
  cursor_blink: true        # blinking cursor in header
```

### Color schemes

| `color_scheme` | Primary | Background | Look |
|----------------|---------|------------|------|
| `green` | `#00ff41` | `#0a0a0a` | Classic Matrix / VT100 |
| `amber` | `#ffb000` | `#0a0a0a` | Warm vintage terminal |
| `blue` | `#00aaff` | `#0a0a0a` | IBM 3270 |
| `white` | `#e0e0e0` | `#1a1a1a` | Soft light mode |

### Navigation

```yaml
nav:
  - title: "home"
    url: "/"
  - title: "about"
    url: "/about/"
  - title: "archive"
    url: "/archive/"
  - title: "tags"
    url: "/tags/"
```

---

## Writing Posts

```
_posts/YYYY-MM-DD-post-title.md
```

```yaml
---
layout: post
title: "Your Post Title"
date: 2024-01-15 09:00:00 +0000
tags: [tag1, tag2]
description: "Short summary for SEO and card previews."
---
```

---

## File Structure

```
jekyll-terminal-theme/
├── _config.yml
├── Gemfile
├── LICENSE
├── index.html
├── about.md
├── archive.md
├── tags.md
├── _layouts/
│   ├── default.html
│   ├── home.html
│   ├── post.html
│   └── page.html
├── _includes/
│   ├── header.html
│   └── footer.html
├── _sass/
│   ├── _variables.scss
│   ├── _base.scss
│   ├── _layout.scss
│   ├── _components.scss
│   └── _terminal-fx.scss
├── assets/
│   ├── css/main.scss
│   └── js/terminal.js
└── _posts/
    ├── 2024-01-15-welcome-to-jekyll-terminal-theme.md
    └── 2024-01-22-making-a-jekyll-theme-that-sells.md
```

---

## Browser Support

Chrome 90+, Firefox 88+, Safari 14+, Edge 90+. No IE support.

---

## License

MIT License — see [LICENSE](./LICENSE).

You may use this theme for personal and commercial projects. You may not resell or redistribute the theme files themselves.

---

## Credits

Built by [devshelf](https://github.com/devshelf) — premium Jekyll themes & developer guides.

---

## Changelog

### v1.0.0 — Initial release
- 4 color schemes (green, amber, blue, white)
- Boot sequence animation (sessionStorage-based, once per session)
- CRT scanlines + phosphor glow effects
- `ls -la` post listing
- Copy buttons on code blocks
- Keyboard shortcuts
- Fully responsive
