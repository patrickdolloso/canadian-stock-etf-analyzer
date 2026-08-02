# Canadian Stock & ETF Analyzer

A 100% client-side web app that analyzes a Canadian/US ETF ticker and returns a
tax-optimized account recommendation, sample portfolio, and projected performance.

## Live app
https://patrickdolloso.github.io/canadian-stock-etf-analyzer/

## What it does
1. Enter a ticker (VOO, VFV, HXS, VCN, XIC, XAW, ZAG, HXT, VTI, XEQT).
2. Pick an account (TFSA / RRSP / Non-Reg) or "All Accounts" for comparison.
3. Set investment amount, time horizon, and monthly contribution.
4. Get:
   - **Tax Summary** — US withholding, foreign withholding, dividend tax credit, capital gains treatment.
   - **Account Recommendation** — optimal account + why, with per-account tax-drag table.
   - **Projected Performance** — Chart.js projection (optimized vs worst-fit vs contributions).
   - **Sample Portfolio** — illustrative allocation for the recommended account.
   - **Fee Analysis** — MER, tax drag, trading fee.

## Tech
Single `index.html` — Tailwind (CDN), Chart.js (CDN), Font Awesome (CDN), Inter,
vanilla JS. No backend; all math runs in the browser.

## Asset-location principles (from the Master Guide)
- US-listed US ETFs (VOO, VTI) → RRSP (0% US withholding via treaty)
- CAD-listed US ETFs (VFV) → TFSA (~0.17% drag)
- Swap-based (HXS, HXT) → TFSA / Non-Reg (0% withholding, capital gains)
- Canadian equity (VCN, XIC) → Non-Reg (dividend tax credit)
- Bonds (ZAG, VAB) → TFSA (avoid full taxation)

## Disclaimer
Educational estimates only — not financial advice. Returns and tax rates are
illustrative. Consult a cross-border tax professional.

**Full system:** https://northernnomad.gumroad.com/l/ftefkt ($19.99)
