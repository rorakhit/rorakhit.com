# rorakhit.com

Personal site. Plain static HTML in `public/`, served by Cloudflare Workers static assets (Worker `portfolio-site`, no build step, no Worker script). Custom domains `rorakhit.com` and `www.rorakhit.com` are set in `wrangler.jsonc`.

## Local preview

```bash
npm install
npm run dev
```

## Deploy

Cloudflare Workers Builds is connected to this repo. Pushing to `main` runs `npx wrangler deploy` (production), and other branches get a preview version via `npx wrangler versions upload`.

To deploy by hand, use `npx wrangler login` or a `CLOUDFLARE_API_TOKEN` in `.env` (gitignored):

```bash
npm run deploy
```

Roll back with `npx wrangler deployments list` and `npx wrangler rollback <version-id>`.
