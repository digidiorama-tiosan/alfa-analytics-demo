# Alfa Analytics Platform — GitHub Pages

A ready-to-publish demo of the **Alfa Analytics Commercial Intelligence Platform**.
Everything is self-contained (no build step, no dependencies) — just push and enable Pages.

## What's inside
| File | URL once published | What it is |
|---|---|---|
| `index.html` | `https://<user>.github.io/<repo>/` | The full interactive dashboard (login + 3D Command Center + reports) |
| `blueprint.html` | `https://<user>.github.io/<repo>/blueprint.html` | Production architecture blueprint (for stakeholders) |
| `.nojekyll` | — | Tells Pages to serve files as-is (skip Jekyll) |

## Demo logins
| Role | Email | Password |
|---|---|---|
| Admin / IT | `maya@alfaretail.com` | `admin` |
| Commercial | `rangga@alfaretail.com` | `analyst` |

Or click **Request access** on the login screen to register a new account, then approve it as the admin
in **Access Control**. Inside an empty report, use **Load sample data** to populate the dashboard.

## Publish in ~2 minutes

### Option A — Command line
```bash
# from inside this folder
git init
git add .
git commit -m "Alfa Analytics platform demo"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```
Then on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch →
Branch: `main` / `/ (root)` → Save.** Your site goes live at `https://<your-username>.github.io/<repo-name>/`
within a minute.

### Option B — Web upload (no git)
1. Create a new repository on GitHub (e.g. `alfa-analytics-demo`).
2. **Add file → Upload files** → drag `index.html`, `blueprint.html`, and `.nojekyll` in → Commit.
3. **Settings → Pages** → Source: `main` / root → Save.

## Notes
- This is a **Phase 0 demo**: the UI and flows are complete, but accounts and uploaded data live in
  each visitor's **own browser** (not shared). For "admin uploads once → everyone sees it" and cross-device
  login, implement the backend in the handoff package (`design_handoff_production/`).
- Want a custom domain? Add a `CNAME` file with your domain and configure DNS (GitHub docs: *Managing a
  custom domain for your GitHub Pages site*).
- To update the demo later, replace `index.html` with a freshly exported standalone file and push again.
