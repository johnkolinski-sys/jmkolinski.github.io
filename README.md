# John M. Kolinski — personal research site

A static website (plain HTML + one CSS file). No build step, no dependencies. Open `index.html`
in a browser to preview locally.

## Pages
- `index.html` — landing: bio, news & announcements, research highlights
- `research.html` — research thrusts (cracks, wetting, methods)
- `publications.html` — selected publications by topic
- `team.html` — lab members
- `openings.html` — hiring announcements (PhD positions, internships)
- `cv.html` — curriculum vitae
- `styles.css` — shared styling

## Posting new announcements
Open `index.html`, find the `<div class="news">` block, and copy one `news-item` block. Set the
date, pick a tag (`Paper`, `Hiring`, `Award`, etc.), and write the text. Newest goes on top.

## A note on images
Photos currently load from the EPFL/EMSI server by URL. They'll display as-is. To make the site
fully self-contained (recommended for a permanent move off WordPress), download each image into an
`images/` folder here and replace the `https://www.epfl.ch/...` `src` values with `images/yourfile.jpg`.

## Hosting free on GitHub Pages

1. Create a free account at https://github.com if you don't have one.
2. Create a new **public** repository. For a personal site at `https://<username>.github.io`,
   name it exactly `<username>.github.io`. (Any other name gives you
   `https://<username>.github.io/<repo>/` instead — also fine.)
3. Upload these files to the repository root: click **Add file → Upload files**, drag in
   `index.html`, the other `.html` files, and `styles.css`, then **Commit changes**.
   (Or use git: `git init`, `git add .`, `git commit -m "site"`, `git remote add origin <url>`, `git push -u origin main`.)
4. In the repo, go to **Settings → Pages**. Under **Build and deployment → Source**, choose
   **Deploy from a branch**, select branch `main` and folder `/ (root)`, then **Save**.
5. Wait ~1 minute. Your site is live at the URL shown on that Pages settings screen.

### Custom domain (optional)
In **Settings → Pages → Custom domain**, enter your domain (e.g. `kolinski.science`) and save.
Then at your domain registrar add a CNAME record pointing to `<username>.github.io` (or the four
GitHub A records for an apex domain — GitHub's Pages docs list the current IPs). Tick
**Enforce HTTPS** once the certificate provisions. A custom domain is the only paid part — the
domain registration itself (~$10–15/yr); GitHub Pages hosting stays free.

## Alternatives (also free)
- **Netlify** — drag the folder onto https://app.netlify.com/drop for an instant live URL.
- **Cloudflare Pages** — connect the GitHub repo at https://pages.cloudflare.com.

Both work with these exact files, no changes needed.
