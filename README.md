# Corporate Intelligence Lab

A financial statement analysis tool I built for my MBA Tech coursework. Pick a company, read its ratios, compare it with peers, and stress-test how close it is to financial distress.

**Live:** https://kanishksaini-007.github.io/Corporate-Intelligence-Lab/

## What it does

- Eleven companies (Apple, Microsoft, Alphabet, Meta, NVIDIA, Amazon, Tesla, Walmart, Coca-Cola, Boeing, Intel), five fiscal years each, taken from their 10-K filings via the SEC's XBRL data
- 21 ratios plus peer medians across liquidity, profitability, leverage, efficiency, cash flow and growth. Each one shows its formula and the numbers used
- DuPont breakdown of return on equity
- Peer scorecard, head-to-head radar, bubble chart and indexed growth chart
- Market & valuation tab: price, market cap, P/E, P/S, P/B, FCF yield. Live quotes from Twelve Data when reachable (Apple works without a key, others need a free key kept in your browser), otherwise a saved 15 Oct 2026 close snapshot
- Risk models: Altman Z''-score (1995 non-manufacturer version) and an 8-test Piotroski-style checklist
- What-if lab: change revenue, margin, debt-funded buybacks and short-term debt, and watch the Z'' score move. It also shows how far the margin can fall before the company leaves the safe zone
- One-page analyst brief per company, printable as PDF
- CSV download of the underlying numbers

## Honest limits

- The Altman model was built on older manufacturing firms. It can misread asset-light companies (Apple's retained earnings are negative because of buybacks, so it lands in the grey zone)
- Debt means bonds, notes and commercial paper. Finance leases are included only where the company reports them in the same line, operating leases are left out
- Fiscal years end on different dates
- Commentary is rule-based (fixed thresholds in the code), not a forecast
- Educational project, not investment advice

## Tech

Plain HTML, CSS and JavaScript in one file. Chart.js is inlined so it works offline. No build step, no server.

## Data

Pulled from `data.sec.gov` XBRL company facts (annual 10-K values). Filing links are in the app.

Kanishk Saini, Roll N099, MBA Tech, NMIMS Mumbai
