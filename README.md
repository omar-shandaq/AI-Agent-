# HRSD AI Executive Office - Netlify Deployment

## Quick Start

1. Install Netlify CLI (optional):
   ```bash
   npm i -g netlify-cli
   ```
2. Set your Gemini API key (never commit this):
   ```bash
   netlify env:set GOOGLE_API_KEY "<your-key>"
   ```
3. Run locally:
   ```bash
   netlify dev
   ```
   - Site runs at http://localhost:8888
   - Functions run at `/.netlify/functions/*`

4. Deploy:
   ```bash
   netlify deploy --prod
   ```

## Structure
- `index.html`: Single-page app
- `netlify/functions/ai.js`: Serverless function proxy to Google Generative Language API
- `netlify.toml`: Build/publish configuration
- `_redirects`: SPA fallback to `index.html`

## Notes
- API calls are made to `/.netlify/functions/ai` so the API key stays server-side.
- Set `GOOGLE_API_KEY` in Netlify UI (Site settings → Environment variables) for production.
# HRSD_aimo
