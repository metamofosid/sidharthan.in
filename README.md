# sidharthan.in — static rebuild

A plain HTML/CSS static rebuild of the Cargo-hosted portfolio, ready for GitHub Pages.

## What's here
- `index.html` — the whole site (single scrolling page, matching the original's anchor-link navigation)
- `styles.css` — all styling
- `fonts/` — Monument Grotesk (Regular, Italic, Medium, Medium Italic, Bold, Bold Italic, Mono, Semi-Mono), converted from your `.otf` files to `.woff2` and loaded via `@font-face`. This is the real typeface from the original site, licensed to you — don't redistribute the font files outside this project.
- `images/` — photos from your saved image set, matched to each project: worldmap collage, the Hello World! render sequence + tiled pattern, t minus's diagram/photo/QR code, the ganga archive (viewable with the arrow buttons), the in-between travel photos, an 12-photo DHN-BKSC-TATA train-journey gallery, and the real Instagram grid image on the instagram page.
- The 10 commission/architecture project pages embed live Behance project cards (same as the original site).
- The `info` page includes the full bio, exhibitions, awards & grants, experience, and education sections.

## Publish to GitHub Pages
1. Create a new GitHub repository (e.g. `sidharthan.in`).
2. Push these files to the repo root (or to a `docs/` folder — your choice):
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. In the repo on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, then pick branch `main` and folder `/ (root)` (or `/docs` if you used that folder). Save.
4. Your site will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.
5. To use your custom domain `sidharthan.in`: in the same Pages settings, enter it under **Custom domain**, then at your domain registrar add a CNAME record pointing `sidharthan.in` (or `www`) to `<your-username>.github.io`. GitHub will add a `CNAME` file to your repo automatically once you save.

## Notes
- The `in-between` gallery is missing two spots from the original captions (Mannheim, Germany and Marstrand, Sweden) — those two photos weren't in your saved image set. Drop them into `images/` and add an extra `<figure>` in `index.html` if you find them.
- If you'd rather have real photo galleries instead of Behance embeds on the 10 commission pages, replace the `<div class="behance-embed">...</div>` block on that page's section with `<img>` tags once you have the images.
- The `info` page's profile photo wasn't in your saved image set, so that section is text-only — drop in a photo and add an `<img>` to `.info-intro` if you have one.
- The `contact` section's LinkedIn link is a placeholder (`linkedin.com`) since your actual profile URL wasn't available — update the `href` in `index.html` if you want it to point somewhere specific.
