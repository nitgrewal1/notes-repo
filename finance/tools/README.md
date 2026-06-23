# Tools (HTML)

Self-contained single-file HTML finance tools.

| File | Description |
|---|---|
| `z-dashboard.html` | Multi-account Zerodha Kite Connect dashboard (holdings, positions, trades, GTT, SIPs, CAS parsing) — note: needs the Flask proxy server running locally |
| `mf-central-cas-dashboard.html` | Standalone CAS PDF extraction dashboard (PDF.js + Claude API) |
| `swp-scenario-builder.html` | SWP simulator — sequence-of-returns risk, protection strategies, LTCG tax calc |
| `mf-portfolio-xirr.html` | Local-first MF portfolio app with XIRR/analytics (IndexedDB/Dexie.js) |

> Note: tools relying on a local Flask proxy (like Z.Dashboard) won't fully function on GitHub Pages by themselves — Pages only serves static files. Document any local setup steps needed in a comment block at the top of the relevant HTML file.
