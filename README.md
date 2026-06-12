# Pal Systems — Marketing Website

## Overview
Public marketing site for Pal Systems. Static HTML/CSS/JS, no build step.

- **Project path** (local): `C:\wamp64\www\pal-systems.com`
- **Live site**: https://pal-systems.com
- **Server path**: `/home/pal-systems.com/public_html`
- **GitHub**: `https://github.com/fadihanna89/pal-systems.com`
- **Stack**: Static HTML, Bootstrap 5, plain JS — no PHP, no Node, no build tools.

## Sister projects
| Project | Role |
|---|---|
| [finexa](https://github.com/fadihanna89/finexa) | Laravel multi-tenant SaaS backend — powers Hesabi (https://hesabi.pal-systems.com) |
| [hesabi-app](https://github.com/fadihanna89/hesabi-app) | Flutter mobile app for end users of Hesabi |
| **pal-systems.com** (this repo) | Public marketing site that links to Hesabi + the mobile app |

## Brand colors (CSS variables)
- `--navy`   = `#1e2d4e`
- `--green`  = `#1a9a57`
- `--orange` = `#e8722a`

## Structure
```
pal-systems.com/
├── index.html          # single-page site
├── images/             # logos and assets
│   ├── pal-systems-logo-h.png   # horizontal logo (navbar, displayed at 54px height)
│   └── ...
└── README.md
```

Logo wrapper in `index.html`:
```html
<a href="/" style="display:block;line-height:0">
  <img src="images/pal-systems-logo-h.png" height="54" alt="Pal Systems" style="display:block">
</a>
```
The `display:block;line-height:0` is intentional — it removes the inline-image bottom whitespace.

## Deployment
After pushing to GitHub, SSH and pull:
```bash
cd /home/pal-systems.com/public_html
git pull origin main
```
No artisan / npm / build step. Static files only.

## Common pitfall
- **Linux filesystem is case-sensitive**: `Logo.png` ≠ `logo.png`. If you rename a logo on Windows, use a two-step `git mv` (intermediate temp name) so git tracks the case change properly.
