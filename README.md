# WAHA Render Config

This repository deploys WAHA to Render using Docker.

## Deploy on Render

1. Create a new **Web Service** in Render from this GitHub repo.
2. Render should detect `render.yaml` automatically.
3. Set these required environment variables in Render:
   - `WAHA_API_KEY` (your API key)
   - `WAHA_HMAC_SECRET` (your webhook signature secret)
4. Deploy and copy the Render service URL.

## Test endpoint

After deploy, test:

```bash
curl -H "X-Api-Key: YOUR_API_KEY" https://YOUR-RENDER-URL/
```

## Connect to Laravel app

Set in your Laravel `.env`:

```env
WAHA_BASE_URL=https://YOUR-RENDER-URL
WAHA_API_KEY=YOUR_API_KEY
WAHA_HMAC_SECRET=YOUR_HMAC_SECRET
```
