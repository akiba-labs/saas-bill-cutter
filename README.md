# SaaS Bill Cutter

Free calculator: enter what you pay for business software (Mixpanel, Semrush, FreshBooks, Calendly, Chargebee, Typeform, Pipedrive, GoHighLevel, Intercom) and see the open-source swap, savings after servers and setup time, and the catches (licenses, upkeep, paid data).

- Full app and API (Vercel): https://saas-bill-cutter.vercel.app
- Calculator (GitHub Pages): https://akiba-labs.github.io/saas-bill-cutter/
- API: `GET /api/calculate`, `GET /api/tools`
- Agent docs: `/llms.txt`, `/openapi.json`, `/.well-known/ai-plugin.json`

Educational estimate only. Not financial, legal, or licensing advice. No affiliate links, no tracking.

```bash
npm install
npm test
npm run build
npm run build:pages
```

`npm run build` is the Vercel app (calculator, JSON API, share pages). `npm run build:pages` writes a static `out/` for GitHub Pages and checks that internal links and assets resolve under `/saas-bill-cutter`. Server routes stay in the repo; the Pages script only moves them aside for that build.

GitHub settings: **Settings → Pages → Build and deployment → Source: GitHub Actions**. Pushes to `main` deploy with `.github/workflows/pages.yml`. The copy-paste steps for the other tool repos are at the top of `scripts/build-pages.mjs`.
