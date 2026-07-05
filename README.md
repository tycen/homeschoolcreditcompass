# Homeschool Credit Compass

A two-page reference site for homeschool families:

- **index.html** — The Affordable College Track: Modern States, CLEP, the Iowa
  Last-Dollar Scholarship, dual enrollment at Faith Baptist Bible College, and
  Christian Leaders Institute (including the Liberty University transfer path).
- **transcripts.html** — Homeschool Transcripts: anatomy of a transcript,
  counting credits, translating real-life activities into course credit,
  subject-based vs. year-based formats, and the CLT exam.

Live at: https://homeschoolcreditcompass.com

## How it's built

Plain HTML + CSS with a few lines of JavaScript. No frameworks, no build step.

- Collapsible `<details>/<summary>` sections — present from the headlines,
  readers expand the depth later.
- "Expand all / Collapse all" presenter controls on each page.
- Print stylesheet + a `beforeprint` hook that opens every section and prints
  link URLs, so Ctrl+P produces a complete handout.

## Deploying (GitHub Pages)

1. Push these files to the repo root on `main`.
2. Settings → Pages → Deploy from a branch → `main` / root.
3. DNS: four A records on the apex to GitHub Pages IPs
   (185.199.108.153 / .109.153 / .110.153 / .111.153) and a `www` CNAME to
   `<username>.github.io`.
4. Settings → Pages → Custom domain: `homeschoolcreditcompass.com` → wait for
   the DNS check → Enforce HTTPS.

The `CNAME` file keeps the custom domain pinned across deploys; `.nojekyll`
skips the Jekyll build.

## License

Site content is CC BY-NC 4.0 — free to share for noncommercial use with
attribution. See `LICENSE`.
