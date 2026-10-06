# Strata Films website

Live at https://www.stratafilmsfl.com. Hosted on Vercel; every change pushed to `main` goes live automatically in about 30 seconds.

## How to edit

**Easiest (in the browser):**
1. Open the page's file in this repo (e.g. `about.html`, `upcoming-projects.html`).
2. Click the pencil icon, make your change.
3. Click **Commit changes**. That's it, it's live in ~30 seconds.

**Adding an image:** go into the `699341e069cf31d9ef4f588f` folder, click **Add file → Upload files**, then reference it in the HTML as `699341e069cf31d9ef4f588f/your-image.jpg`.

## Page files

| Page | File |
|---|---|
| Home | `index.html` |
| Projects | `projects.html` |
| Current / Upcoming | `upcoming-projects.html` |
| About | `about.html` |
| Contact | `contact.html` |
| Film pages | `crime-of-the-outman.html`, `waiting-below.html`, `blood-symmetry.html`, `perennial.html`, `fables-river.html` |

URLs drop the `.html` (e.g. `/about`). That's set in `vercel.json`.

## Notes
- No build step. It's plain HTML/CSS, served as-is.
- If something breaks, open the commit history, find the last good version, and revert.
