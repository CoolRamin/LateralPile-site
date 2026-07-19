# LateralPile Marketing Website

Public source for the landing page at **https://www.ramisoftsolutions.com** (domain/DNS
cutover pending — see Deployment status below), the marketing site for the LateralPile
Windows desktop application.

## Scope of this repository

This repository contains **only the static marketing website** (`src/`): HTML, CSS, and
inline SVG assets, plus the GitHub configuration that makes this repo's Issues usable as a
public support channel.

**It does not contain, and will never contain, any LateralPile application source code.**
The WPF desktop app (analysis engine, UI, API) is developed in a separate, private
repository. Nothing in this repo requires or exposes that source — no engine code, no
project files, no Azure/cloud configuration, no build artifacts from the app.

## About LateralPile

LateralPile is a desktop tool for coupled axial + lateral analysis of laterally loaded piles
and drilled caissons in layered soil (Naik-Peyrot p-y method), with an ACI 318-25 capacity
check on a Mander-confined section and independent soil-mobilization and equilibrium audits.
Download the free public beta from the site above.

## Reporting bugs and requesting features

- **Bug reports and feature requests (public):** use this repo's
  [Issues](../../issues) — templates are provided for both.
- **Private questions** (confidential project data, plan-check questions, licensing):
  email `admin@ramisoftsolutions.com`.
- **In-app bug reports:** the app's `Help > Report a Bug` command pre-fills an email with
  your case number and current project file attached.

## Local development

There is no build step. Open `src/index.html` directly in a browser, or serve the `src/`
folder with any static file server, to preview changes.

## Deployment

Hosted on **Azure Static Web Apps** (Free tier), deployed automatically from this repo's
`main` branch via GitHub Actions. `staticwebapp.config.json` configures the SPA fallback and
baseline security headers. Custom domain and DNS cutover to `www.ramisoftsolutions.com` are a
separate, later step — see this repository's issues/roadmap for status.

## Contributing

Small typo fixes and copy improvements are welcome via pull request — see
[CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT (see [LICENSE](LICENSE)). This covers the **website content only**. The LateralPile
application itself is separate, closed-source software under different terms.
