# Garrison Housing Solutions

Marketing site for Garrison Housing Solutions: bilingual (English/Polish) rental-finding and tenant support in Poznań, Poland.

**Live:** https://garrisonhousingsolutions.com

## How it's hosted

- **GitHub Pages**, deployed from the `main` branch, repo root (`/`). It uses the "legacy" build: no GitHub Actions workflow, and Pages serves the files as they are.
- **Custom domain** is set by the `CNAME` file (`garrisonhousingsolutions.com`). Don't delete it, or the site falls back to `tennyv.github.io/GarrisonHousingSolutions`.
- **HTTPS certificate** is issued by GitHub (covers the apex and `www`). "Enforce HTTPS" can be switched on in *Settings → Pages*.
- **DNS** is managed at **Namecheap** (the domain registrar). The apex should point to GitHub Pages' A records (`185.199.108.153`, `.109.153`, `.110.153`, `.111.153`), and `www` should be a CNAME to `tennyv.github.io`.

Check the Pages status from the terminal:

```bash
gh api repos/TennyV/GarrisonHousingSolutions/pages
```

## Files

| File | What it is |
|---|---|
| `index.html` | The whole site: one page with inline CSS and no build step |
| `CNAME` | Custom domain for GitHub Pages |
| `landing` | Old draft of the page (placeholder contact details). It isn't linked and is safe to delete |

## Making changes

1. Edit `index.html`.
2. Preview it locally by opening the file in a browser, or run:
   ```bash
   python3 -m http.server 8000
   ```
   and visit http://localhost:8000.
3. Commit and push to `main`. Pages redeploys automatically, usually within a minute or two.

## Business details on the site

Keep these in sync if anything changes:

- Email: poznan.mieszkania@wp.pl
- Phone / Signal: +48 722 338 040 (Signal: serealwhat.55)
- Packages: **Find & Settle** (one-time) and **Stay Covered** (ongoing). Prices are deliberately **not** on the site; quote them by email.
- The site is written so that everything can be done remotely (message/phone/video). Avoid promising in-person viewings, inspections, or errands.
- Military clause and Housing Office paperwork support are included in both packages, not sold as an add-on.
- Do **not** claim Housing Office approval or endorsement unless that's confirmed in writing.
