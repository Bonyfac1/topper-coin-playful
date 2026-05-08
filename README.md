# Topper Coin — Playful Edition (aces.name)

A second, more playful design for Topper Coin (TPC), running in parallel to the
original site at topperharleycoin.com. Same on-chain data, fresh visual brand.

## Stack

- Plain static HTML + vanilla JS + Chart.js (no build step)
- PHP proxies (`history.php`, `holders.php`) for CORS-blocked APIs
- Forpsi shared hosting, deployed via FTP

## Local preview

Just open `index.html` in a browser. The chart will fall back to a single live
data point when `/history.php` isn't reachable (i.e. when not running on the
server). To preview with the PHP proxies you can run:

```bash
php -S localhost:8000
# then open http://localhost:8000/
```

## Deploy

1. Copy `.ftp-credentials.example` to `.ftp-credentials` and fill in the password.
2. Tighten permissions: `chmod 600 .ftp-credentials`
3. Run: `./deploy.sh`

This uploads `index.html`, both PHP proxies, and the assets to Forpsi.

## Visual direction

- Palette: sunset orange (#FF6B35), sky blue (#5BC0EB), cream (#FFF8E7).
- Font: Fredoka (Google Fonts).
- Mascot: Topper Harley pilot illustration (`assets/mascot.webp`, ~82 KB),
  generated via the higgsfield AI MCP and converted from PNG to WebP.

## Sections

1. Nav
2. Hero (mascot + headline + CTAs)
3. Live chart (TPC/USD or TPC/SUPRA, 15M / 1H / 12H / 24H frames)
4. Stats (price, 24h change, market cap, holders)
5. Tokenomics (supply, mcap, holders, chain + feature pills)
6. How to Buy (4 steps)
7. Roadmap (4 phases)
8. FAQ (6 items)
9. Footer (contract address copy + socials)
