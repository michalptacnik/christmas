# christmas.ll.land

Publishes the **Liberland Grand Christmas Gala** page at **https://christmas.ll.land**.

The page itself lives in [`liberland/site`](https://github.com/liberland/site) under `christmas-gala/`
(Vite + React, prerendered). This repository only holds `.github/workflows/deploy.yml`: every 5 minutes
it checks whether `christmas-gala/` changed on `master`, builds it with
`SITE_URL=https://christmas.ll.land/ BASE_PATH=/` and deploys it to GitHub Pages. The deployed commit is
at `/version.txt`.

## Languages

| Page | Address |
| --- | --- |
| English | https://christmas.ll.land/ |
| 简体中文 (Simplified Chinese) | https://christmas.ll.land/zh/ |

- `EN · 中文` in the header switches language; the choice is remembered.
- Visitors whose browser is set to a mainland China, Taiwan, Hong Kong or Macau time zone, or to Chinese
  as its first language, are taken to `/zh/` automatically (unless they chose English).
- Chinese text is edited in `liberland/site`: `christmas-gala/src/data/event.zh.ts` and
  `christmas-gala/src/i18n/ui.ts`. See `christmas-gala/README.md`.

## Settings (once)

Settings → Pages: Source **GitHub Actions**, custom domain **christmas.ll.land**, **Enforce HTTPS**.
