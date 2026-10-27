# Competitive Pricing Intelligence Dashboard

A static, responsive dashboard built from Mission 1 competitive pricing research for the concert streaming venture. It separates the source data (`data/competitor_data.json`) from the interface and requires no backend, API key, or database.

## Run locally

Because the page loads its JSON with `fetch`, serve this directory over HTTP. For example:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000/Phase_1_Pricing_Dashboard/` when run from the parent directory, or `http://localhost:8000/` from this directory.

## Data and calculation notes

- Data source: `competitor_data.json`, cross-checked against `competitor_analysis.docx`.
- Research date: October 27, 2026.
- Four competitors and nine offer records are included. Seven offers have numeric USD prices; two are unavailable.
- Representative monthly subscription comparison uses VEEPS at $19.99/month and nugs at its promotional $12.99/month. Mean and median are both $16.49. The nugs subsequent rate is $14.99/month.
- Annual, monthly, and event amounts are not combined into one price statistic. No separately priced add-on is counted as a product offer.
- The recommended $7.99–$12.99 range is preliminary and applies to a proposed single-event pass. It is not an optimal price and remains subject to cost, rights, and demand analysis.
- Prices are research snapshots and may have changed. Unavailable prices are not imputed.

## Deployment

The project is static and can be hosted on GitHub Pages. The Pages workflow publishes this directory; no client-side routing is used, so page refreshes work at the repository path.

## GitHub Pages

A GitHub Actions workflow at `.github/workflows/pages.yml` deploys the repository root on pushes to `main` and manual workflow dispatch. After pushing, ensure the repository's Pages source is set to **GitHub Actions** in Settings → Pages. Expected URL: `https://marleygrandizio.github.io/pricing-dashboard/`.
