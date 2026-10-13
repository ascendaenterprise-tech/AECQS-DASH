# AECQS-DASH

Ascenda Enterprise Capital internal dashboard and portals. Static HTML, no build step.

| File | What it is |
|---|---|
| `index.html` | **Client portal** (front page): personal welcome, account value chart, signals, statements, documents, messages, onboarding. Demo mode with sample data. |
| `aec-portal.html` | Investor Portal (sign-in against the `aec-portal-api` Worker; statements and documents) |
| `trading-portal.html` | Private-client trading portal prototype (signals, positions, statements, onboarding). **Sample data only.** |



## Run locally
Open `index.html` in a browser, or `python3 -m http.server` and visit `localhost:8000`.

## Secrets
- This repo is public. Never commit real client names, balances, credentials or sales records here.
- Real client data must come from an authenticated API after sign-in, never from files in this repo.
- `config.example.js` is a template. A real `config.js` is gitignored.

## Compliance note
`trading-portal.html` is a prototype. Real client accounts, performance display and signals licensing need a backend plus securities-counsel review before launch. All AECQS figures are hypothetical and unaudited.
