# TWISS Legal Pages — GitHub Pages Deployment

This folder contains the legal pages required for Meta App Review submission for the TwissInfluencer application.

## Files

- `index.html` — Landing page with links to all legal docs
- `privacy.html` — Privacy Policy
- `terms.html` — Terms of Service
- `data-deletion.html` — Data Deletion Request instructions

## Quick Deployment to GitHub Pages (10 minutes)

### Step 1 — Create a GitHub repository

1. Go to https://github.com/new
2. **Repository name:** `twiss-legal` (or any name you want)
3. **Visibility:** Public (required for free GitHub Pages)
4. **Initialize:** Leave unchecked (we'll upload manually)
5. Click **Create repository**

### Step 2 — Upload these files

Option A: Drag and drop (easiest, no git needed)
1. On the new repo page, click **"uploading an existing file"**
2. Drag the 4 HTML files (`index.html`, `privacy.html`, `terms.html`, `data-deletion.html`) into the upload area
3. Commit message: `Initial legal pages`
4. Click **Commit changes**

Option B: Git CLI
```bash
cd "/Users/johannsenlum/Documents/Projects/twiss/marketing/performance marketing/twiss-legal"
git init
git add .
git commit -m "Initial legal pages"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/twiss-legal.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. In your repo, go to **Settings** (top menu)
2. Left sidebar → **Pages**
3. **Source:** Deploy from a branch
4. **Branch:** `main` / `/ (root)`
5. Click **Save**
6. Wait 1-2 minutes for the first deployment

### Step 4 — Get your URLs

After deployment, GitHub Pages shows you the live URL at the top of the Pages settings. It will look like:

```
https://YOUR_USERNAME.github.io/twiss-legal/
```

Your full URLs will be:

| Page | URL |
|---|---|
| Home | `https://YOUR_USERNAME.github.io/twiss-legal/` |
| Privacy Policy | `https://YOUR_USERNAME.github.io/twiss-legal/privacy.html` |
| Terms of Service | `https://YOUR_USERNAME.github.io/twiss-legal/terms.html` |
| Data Deletion | `https://YOUR_USERNAME.github.io/twiss-legal/data-deletion.html` |

## Optional: Custom Domain (e.g., legal.twiss.studio)

If you want professional URLs like `https://legal.twiss.studio/privacy.html`:

1. In your domain registrar (where twiss.studio is registered), add a CNAME record:
   - **Name:** `legal`
   - **Value:** `YOUR_USERNAME.github.io`
2. In GitHub Pages settings → **Custom domain** field → enter `legal.twiss.studio`
3. Wait for DNS propagation (~5-30 min)
4. GitHub auto-provisions a free SSL certificate
5. Your URLs become `https://legal.twiss.studio/privacy.html` etc.

## Updating the Pages

Edit the HTML files directly on GitHub (click any file → pencil icon) or push updates via git. Changes go live within 1-2 minutes.

## Meta App Settings — Field-by-Field Guide

Once your pages are live, fill the TwissInfluencer app settings as follows:

| Field | Value |
|---|---|
| App ID | `1508303767337414` (already filled) |
| Display name | `TwissInfluencer` (already filled) |
| Namespace | Leave blank |
| App domains | `YOUR_USERNAME.github.io` (or `twiss.studio` if using custom domain) |
| Contact email | `johannsen.lum@twiss.io` (already filled) |
| Privacy policy URL | `https://YOUR_USERNAME.github.io/twiss-legal/privacy.html` |
| Terms of Service URL | `https://YOUR_USERNAME.github.io/twiss-legal/terms.html` |
| User data deletion | Select "Data deletion instructions URL" → `https://YOUR_USERNAME.github.io/twiss-legal/data-deletion.html` |
| Category | `Business and Pages` (or `Marketing` — both are accepted) |
| App icon | Upload a 1024x1024 TWISS logo PNG |
| Data Protection Officer | Optional — fill if you handle EU customer data routinely |
| Address | Your TWISS business address in Singapore |

## Verifying the URLs Work

Before submitting App Review:

1. Open each URL in a private/incognito window
2. Confirm the page renders correctly
3. Confirm internal links work (privacy → home → terms → home)
4. Confirm mailto links open your email client

## Notes

- These pages are **starting templates**. Review and customize before going Live.
- If your business address is not Singapore, update the location references throughout all three HTML files.
- The "Anthropic PBC" mention in the Privacy Policy is included because the bridge uses Claude AI — remove if not applicable.
- Update the "Last updated" date if you make substantive changes.
- Get legal review before relying on these documents in a high-stakes commercial context.
