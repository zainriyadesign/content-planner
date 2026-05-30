# Content Planner — Vercel Deploy Guide

## Deploy in 5 minutes

1. Go to [vercel.com](https://vercel.com) and sign up with GitHub (free)
2. Click **Add New Project**
3. Choose **"Deploy from a folder"** or drag this entire folder into the Vercel dashboard
4. On the settings screen, click **Environment Variables** and add:
   - Name: `ANTHROPIC_API_KEY`
   - Value: your key from console.anthropic.com
5. Click **Deploy**
6. Done — Vercel gives you a URL like `yourplanner.vercel.app`

## First time after deploy
- Open your URL
- Everything works — no API key needed in the app itself, it's on the server

## Backup your data
- Use the **↑ Backup** button monthly — saves a JSON file to your computer
- If you ever need to restore, use **↓ Restore** and upload the JSON

## Files
- `public/index.html` — the whole app
- `api/generate.js` — serverless function that calls Anthropic (keeps your key safe)
- `vercel.json` — routing config
