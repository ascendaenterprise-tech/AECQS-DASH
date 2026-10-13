# AEC-DASH

Ascenda Enterprise Capital internal dashboard and portals. Static HTML, no build step.

| File | What it is |
|---|---|
| `index.html` | Command Center (private ops dashboard: revenue, investors, mentorship, broker balances, TradeLocker live P&L, notes) |
| `aec-portal.html` | Investor Portal (sign-in against the `aec-portal-api` Worker; statements and documents) |
| `trading-portal.html` | Private-client trading portal prototype (signals, positions, statements, onboarding). **Sample data only.** |

Linked pages not in this repo yet: `aec-quant-system.html`, `aec-performance.html`.

## Run locally
Open `index.html` in a browser, or `python3 -m http.server` and visit `localhost:8000`.

## Secrets
- `index.html` stores only SHA-256 hashes of the access codes. This is a convenience lock, not security: the page code is readable by anyone who can load it.
- TradeLocker login goes in `config.js` (gitignored; copy `config.example.js`). Better long term: make the proxy Worker hold the credentials server-side.
- The earlier version of the dashboard had the TradeLocker email and password in the page code. If those ever sat in a public repo or were shared, change that password.
- Keep this repo **private**. The Command Center contains a hard-coded IBKR balance and business figures.

## Compliance note
`trading-portal.html` is a prototype. Real client accounts, performance display and signals licensing need a backend plus securities-counsel review before launch. All AECQS figures are hypothetical and unaudited.
