# Sweeps Vault

A static, SEO-optimized affiliate directory of US social & sweepstakes casinos. No build step, no dependencies — plain HTML/CSS/JS that runs anywhere and deploys straight to GitHub Pages.

## What's here

| Path | Purpose |
|------|---------|
| `index.html` | Homepage — filterable list of all 44 casinos (Cards + Table views) |
| `<slug>.html` | 44 individual SEO review pages (e.g. `crown-coins.html`, `mcluck.html`) |
| `about.html`, `responsible-gambling.html`, `terms.html`, `privacy.html`, `contact.html` | Static content pages |
| `assets/style.css` | Single shared stylesheet for every page |
| `sitemap.xml`, `robots.txt` | Search-engine files |
| `data/casinos.json` | Source data: each casino's ratings, operator, and **affiliate link** |
| `data/research/*.json` | Researched review content used to build the casino pages |

Every "Join" / "Claim Bonus" button uses your affiliate link, opens in a new tab, and is tagged `rel="sponsored nofollow noopener"`. Each review page includes meta titles/descriptions, Open Graph tags, a canonical URL, and JSON-LD structured data (Review, FAQPage, BreadcrumbList).

## Deploy to GitHub Pages

1. Create a repo and push these files to the `main` branch.
2. In the repo: **Settings → Pages → Source → Deploy from a branch**, pick `main` / `/ (root)`, Save.
3. Your site goes live at `https://<username>.github.io/<repo>/` in a minute or two.

### Before you go live
- **Set your real domain.** Canonical URLs and the sitemap currently use `https://sweepsvault.com/`. Find-and-replace that with your actual domain across the `.html` files and `sitemap.xml`. (If you use a custom domain, add a `CNAME` file with the domain in it.)
- **Double-check restricted-state lists** on the review pages — these change often. The affiliate offer figures reflect what was advertised when the pages were written; verify before relying on them.

## Editing the list later

The casino data lives in `data/casinos.json`. To change a rating, operator, or affiliate link, edit that file — then update the matching `<slug>.html` page (and the homepage card text) to match. Adding a new casino means adding a record there and creating a new `<slug>.html` from any existing review page as a template.

---
18+ only (21+ where required). Affiliate links may earn a commission. Sweepstakes casinos are not legal in every US state. Play responsibly — 1-800-GAMBLER.
