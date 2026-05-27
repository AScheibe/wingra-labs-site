# Wingra Labs — landing page

Single-file static site. No build step, no dependencies (fonts load from Google Fonts CDN).

## Structure
```
index.html        the whole page
assets/           favicon, apple-touch icon, OG image, monogram
```

## Deploy to GitHub Pages

**Option A — project site (`username.github.io/wingra-site`)**
```bash
git init
git add .
git commit -m "Landing page"
git branch -M main
git remote add origin git@github.com:USERNAME/wingra-site.git
git push -u origin main
```
Then: repo → Settings → Pages → Source = `Deploy from a branch` → Branch = `main` / `/ (root)` → Save.
Live at `https://USERNAME.github.io/wingra-site/` in ~1 min.

**Option B — user/org site (`username.github.io`)**
Name the repo exactly `USERNAME.github.io`, push the same files, done.

**Custom domain (wingralabs.com)**
1. Add a file named `CNAME` containing just `wingralabs.com`.
2. At your DNS provider, point an `A`/`ALIAS` record to GitHub Pages IPs
   (185.199.108–111.153) and a `CNAME` for `www` → `USERNAME.github.io`.
3. Settings → Pages → Custom domain → enter `wingralabs.com`, enable HTTPS.

## Before you ship — replace placeholders
- `Your Name` (in the About card) → your name
- `Founder & Principal` → your final title
- `hello@wingralabs.com` → real address (appears 3×: hero CTA via #contact, contact section, footer)
- `https://www.linkedin.com/` (footer) → your LinkedIn URL
- Copy in the hero/about is a starting draft — make it yours.

## Notes
- Fonts: Archivo (display) + Newsreader (serif accent), loaded from Google Fonts.
  If you want zero external requests, download the .woff2 files, drop them in
  assets/, and swap the <link> for a local @font-face block.
- Colors are CSS variables at the top of the <style> block (matches the brand:
  ink #161616, cardinal #C5302E, bone #F2F0EA).
- Fully responsive; nav collapses on mobile (links remain reachable by scroll).
