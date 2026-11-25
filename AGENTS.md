# AGENTS.md: agigx-website

Static marketing site for AGIGx (plain HTML, CSS, JS; no build step): `index.html`, `services.html`, `products.html`, `contact.html`, and the privacy questionnaire audit (`audit.html`, `audit.js`, `audit.css`).

## Working here

- Open the HTML files directly or serve the folder (`npx serve .`). There is no test suite; check pages in a browser at desktop and phone width.
- Shared styles live in `styles.css`, shared behaviour in `script.js`. Keep pages self-contained and dependency free.
- Copy rules below apply in full: this is customer-facing text.

## Conventions shared by all AGIGX repos

- Repos are checked out side by side under one parent folder. Local wiring (Postgres, ports, seed data) lives in `../dev-orchestration` (`make start`); cloud deploys live in `../gcp-deploy` and `../dpdp-infra`.
- Commit messages are one plain sentence that says what changed and why (for example "Return a coded 403 so the dashboard does not treat it as an expired session."). No conventional-commit prefixes.
- Work on a branch and open a PR against `main`. Run the tests listed above and keep them green before pushing.
- Never commit secrets: `.env*`, `credentials.txt`, `token.txt`, service-account keys, real customer data. Stage files by name rather than `git add -A`.
- Customer-facing text (UI, emails, website, PDFs) never uses em dashes or en dashes. Use a period, comma or colon; ranges use a plain hyphen.
- Product names: **Privacy Auto Pilot** (overall), **Consent Cockpit**, **Privacy Runway**, **Cloud Guardrail**, powered by DPDP Consultancy. Backend product codes (`CONSENT_MANAGEMENT`, `INFRA_POSTURE`) and URLs are unchanged on purpose.
