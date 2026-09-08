# TryOn Engine

AI-powered virtual try-on for ecommerce.

Upload a photo, choose a garment and size, and generate a personalised preview. Optional body measurements help suggest a size from the product's size chart.

## Features

- Photo upload and garment selection
- AI-generated previews for the selected size
- Optional measurements and sample size guidance
- Before-and-after comparison and image download

## Stack

TypeScript · React · Fastify · OpenAI

## Run locally

From the complete project's root directory, with npm installed (no nvm required):

```sh
npm exec --yes --package=node@24.20.0 -- npm ci
cp -n apps/api/.env.example apps/api/.env
```

For real generation, set `OPENAI_API_KEY` and `ENABLE_LIVE_GENERATION=true` in `apps/api/.env`. API usage is billable; keep this file private. The catalogue can be explored without a key.

```sh
npm exec --yes --package=node@24.20.0 -- npm run dev
```

Open [http://127.0.0.1:4173](http://127.0.0.1:4173) and click **Explore the preview**. The command starts both the website and API. Restart it after changing `.env`; stop it with Ctrl+C.

## Status

In development. Application source is currently local and will be committed incrementally. Until then, a fresh GitHub clone contains only the overview and repository setup and cannot run these commands.

Generated previews illustrate appearance; they do not guarantee physical fit.
