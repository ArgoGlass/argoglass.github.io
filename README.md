# API documentation site

This repository hosts a small static site (GitHub Pages) that serves API documentation using Swagger UI.

What I added:

- `index.html` — A simple Swagger UI page (CDN) that can load either of the two API specs in `/docs/`:
  - `/docs/employee_expenses_api.yaml`
  - `/docs/mobile_api.yaml`
- `.nojekyll` — present to avoid GitHub Pages ignoring files that begin with underscores (if any).

How to deploy (push to GitHub):

1. Commit the added files (if not already):

   git add index.html README.md .nojekyll
   git commit -m "Add Swagger UI index to serve API specs"

2. Push to the `main` branch on GitHub:

   git push origin main

3. Visit the site:

   https://carmy25.github.io/

Notes:

- The YAML specs already live under `/docs/` and will be loaded by the page. Because the files are on the same origin, no CORS configuration is needed.
- If you prefer Redoc or a different UI, I can switch the page to use that instead.

If you want me to also add versioning, separate pages per spec, or a nicer UI with per-spec landing pages, tell me which option you prefer and I’ll implement it.
