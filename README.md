# RamisoftSolutions website

Source of **https://www.ramisoftsolutions.com**, the company site of RamisoftSolutions, developer of specialized
structural engineering software. It introduces the company and its three products at a high level and sends visitors
to each product's own website:

| Product | Website | Its site's repository (and public issue tracker) |
|---|---|---|
| FoundaTrix Studio, analysis and design of rigid foundations | https://www.foundatrix.com | [CoolRamin/FoundaTrix-site](https://github.com/CoolRamin/FoundaTrix-site) |
| PileTrix Studio, lateral and axial analysis of piles and drilled shafts | https://www.piletrix.com | [CoolRamin/PileAxis-site](https://github.com/CoolRamin/PileAxis-site) |
| StruTrix Studio, 3D frame analysis and steel design | https://www.strutrix.com | [CoolRamin/Strutrix-site](https://github.com/CoolRamin/Strutrix-site) |

All three are on the Microsoft Store, and the page links each listing.

Until 2026-10-15 this repository was the one-page site of RPile, the program now called PileTrix Studio, and briefly held its
privacy policy and terms of use. Both moved to www.piletrix.com; `/privacy` and `/terms` here redirect to the
company page's list of each product's policies, and `/rpile` and `/rfoundation` to the product sites.

## What is here

Website code only, nothing from the programs. A static site with no build step:

- `src/index.html`, the one page: products, approach, standards, ideas, contact and the legal list; `src/404.html`.
- `src/styles.css` and `src/site.js`: FoundaTrix Studio's site's design system, shared with the PileTrix Studio and
  StruTrix Studio sites so the four read as one family, with a short "RamisoftSolutions additions" block at the end of the
  stylesheet. A change to the shared part belongs in all four repositories.
- `src/images/`: the company mark and the three product marks (the product marks are copies of each product site's own).
- `src/staticwebapp.config.json`: the strict Content Security Policy (no inline styles or scripts), the 404 page and the
  redirects above.

Every `href` and `src` is root-absolute (`/styles.css`). To preview, serve `src/` with any static file server (a
`file://` page cannot resolve root-absolute paths).

## Ideas for new software

This repository's Issues collect ideas for **new** software, through the "Idea for new software" form. A bug or a
feature request for an existing program goes to that program's own tracker (the form chooser links both). Write to
admin@ramisoftsolutions.com for anything private.

## Deployment

Azure Static Web App `swa-lateralpile-site` (resource group `rg-lateralpile`, Free tier), deployed by the workflow in
`.github/workflows/` on every push to `main`. A push deploys: push only what should be live.

## License

MIT (see [LICENSE](LICENSE)), covering the website content only. The programs are separate, closed-source software
under their own terms.
