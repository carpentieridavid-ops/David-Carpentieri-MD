# David F. Carpentieri, MD — Website

A single-page professional site for David F. Carpentieri, MD — pediatric and anatomic
pathologist, translational researcher in vascular anomalies and biorepository science,
and founder of Ven, LLC / Spectrum, LLC.

Built from his curriculum vitae (dated November 6, 2025) as a self-contained,
static HTML file — no build step, no dependencies beyond Google Fonts.

## Contents

- `index.html` — the entire site (structure, styles, and behavior in one file)
- `david-carpentieri.jpg` — portrait used in the About section
- `biobanking-infographic.png` — biobanking workflow figure used in the hero section
- `raman-spectroscopy-infographic.png` — Raman spectroscopy principle figure used in the hero section

## Running it locally

No build tools required. Either:

- Open `index.html` directly in a browser, or
- Serve it locally, e.g.:

  ```bash
  python3 -m http.server 8000
  ```

  then visit `http://localhost:8000`.

## Publishing with GitHub Pages

1. Create a new GitHub repository (e.g. `carpentieri-site`) and push these files
   to the `main` branch:

   ```bash
   git init
   git add index.html README.md david-carpentieri.jpg biobanking-infographic.png raman-spectroscopy-infographic.png
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```

2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Set **Branch** to `main` and the folder to `/ (root)`, then **Save**.
5. GitHub will publish the site at:

   ```
   https://<your-username>.github.io/<repo-name>/
   ```

   (It can take a minute or two for the first deployment to go live.)

### Using a custom domain (optional)

If you want the site at your own domain (e.g. `davidcarpentieri.com`):

1. In **Settings → Pages → Custom domain**, enter your domain and save — this
   creates a `CNAME` file in the repo automatically.
2. At your domain registrar, add a `CNAME` record pointing your subdomain
   (e.g. `www`) to `<your-username>.github.io`, or `A` records for an apex
   domain pointing to GitHub's IP addresses (listed in GitHub's Pages docs).
3. Wait for DNS to propagate, then enable **Enforce HTTPS** in the Pages settings.

## Updating content

All copy, dates, and links live directly in `index.html`, organized into clearly
commented sections (hero, about, focus areas, timeline, publications, grants &
honors, service, mentoring, contact). Edit the relevant section and push the
change — GitHub Pages redeploys automatically on every push to `main`.

## Credits

Design and content assembled from David F. Carpentieri's CV. Fonts via Google
Fonts (Source Serif 4, Inter, IBM Plex Mono).
