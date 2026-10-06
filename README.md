# Strata Films - static export

Static mirror of strata-films.webflow.io, pulled 2026-09-22. HTML, CSS, JS, fonts, and images are all local. No dependency on Webflow hosting.

## What this is

This is a snapshot of the rendered site, not the Webflow Designer project file. Webflow doesn't support exporting a project to another platform's editor, so this is a byte-for-byte copy of what the browser actually loads. It looks and behaves identically to the live site. The one thing it won't have is Webflow's CMS backend or form-submission handling (see below).

Images were resized (max 2400px on the long edge) and recompressed (JPEG quality 82) to bring the package under upload limits. The originals from Webflow were full camera resolution, up to 8192x5464, far larger than any browser renders them at. Visually identical at every display size, just not archival-resolution files.

## Deploy to Vercel

1. Push this folder to a GitHub repo, or run from inside it:
   ```
   npx vercel --prod
   ```
2. No build step needed. It's a static site. Vercel serves it as-is.
3. `vercel.json` is already set up for clean URLs (`/about` instead of `/about.html`), matching the original site's URL structure.

## Known limitations

- Contact form: `contact.html` has a form that originally posted to Webflow's form handler. That backend doesn't exist here, so the form won't submit anywhere until it's rewired (Formspree, a Vercel serverless function, or similar).
- Google Analytics tag (`G-D1Q8NQS76L`) is still wired in. It will keep firing to Reagan's GA property unless swapped out or removed.
- Pages included: `index`, `about`, `contact`, `projects`, `upcoming-projects`, `crime-of-the-outman`, `waiting-below`, `blood-symmetry`, `perennial`, `fables-river`.

## Verified

All 10 pages and every CSS/JS/font/image asset were checked locally (`python3 -m http.server`) and returned 200 before this was packaged.
