# Netlify Troubleshooting Cheatsheet

## Must-have Settings
- **Build command:** `npm run build`
- **Publish directory:** `dist`
- **Node:** set `NODE_VERSION=20` (Site settings → Build & deploy → Environment)
- `.node-version` file with `20` at repo root.

## If build fails
- Open **Deploys → Failed deploy → Logs**. Common fixes:
  - `astro: not found` → retry with **Clear cache and deploy site**.
  - `Node >=18 required` → set Node to 20 as above.
  - `Publish directory not found` → set `dist` in settings or `netlify.toml`.

## CMS login (Decap + Git Gateway)
1. Enable **Identity** (Project configuration → Identity → Enable)
2. Identity → **Registration**: Invite only
3. Identity → **Services** → Enable **Git Gateway**
4. Invite yourself (email) and login at `/admin`
