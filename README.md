# GPCMoQ

Static site for [gpcmoq.com](https://gpcmoq.com) — Global MoQ Relay Network for Low Latency CMAF.

## Layout

- `gpcmoq-worker/` — Cloudflare Worker serving the static site (Workers Static Assets, no script).
- `.github/workflows/deploy.yml` — auto-deploys on push to `main` via the `CLOUDFLARE_API_TOKEN` repo secret.

## Local dev

```sh
cd gpcmoq-worker
npm install
npx wrangler dev
```

## Deploy

Pushing to `main` triggers GitHub Actions to run `wrangler deploy`. To deploy manually:

```sh
cd gpcmoq-worker
npx wrangler deploy
```
