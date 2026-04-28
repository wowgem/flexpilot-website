# FlexPilot Website

Static website for FlexPilot — Smart Block Assistant for Amazon Flex Drivers.

## Domain

`flexpilot-app.com`

## Structure

- `index.html` — single-page site with all required sections
- `CNAME` — custom domain config for GitHub Pages

## Deployment Options

### Option 1: GitHub Pages (recommended)

1. Create new GitHub repo: `flexpilot-website` (public)
2. Push these files to `main` branch
3. Repo Settings → Pages
4. Source: Deploy from branch `main`, folder `/ (root)`
5. Custom domain: `flexpilot-app.com`
6. Enforce HTTPS: ✓
7. Update DNS at GoDaddy (see below)

### Option 2: Cloudflare Pages

1. Create Cloudflare account
2. Pages → Create project → Connect to GitHub
3. Select `flexpilot-website` repo
4. Build settings: framework preset = none, build command = empty, output directory = `/`
5. Custom domain: `flexpilot-app.com`
6. Update DNS (Cloudflare guides through this)

### Option 3: Vercel

1. Connect repo to Vercel
2. **Disable Deployment Protection** (Settings → Deployment Protection → Off)
3. Custom domain: `flexpilot-app.com`
4. Update DNS

## DNS Configuration (GoDaddy → GitHub Pages example)

In GoDaddy DNS panel, add these records:

```
Type   Name    Value                  TTL
A      @       185.199.108.153        1 hr
A      @       185.199.109.153        1 hr
A      @       185.199.110.153        1 hr
A      @       185.199.111.153        1 hr
CNAME  www     <username>.github.io   1 hr
```

Wait 30-60 min for DNS propagation.

## Required URLs After Deploy

- Homepage: `https://flexpilot-app.com/`
- Privacy Policy: `https://flexpilot-app.com/#privacy-policy`
- Terms of Service: `https://flexpilot-app.com/#terms`
- Account Deletion: `https://flexpilot-app.com/#account-deletion`

These URLs go into Google Play Console:
- Privacy policy URL field: `https://flexpilot-app.com/#privacy-policy`
- Account Deletion URL on Data Safety form: `https://flexpilot-app.com/#account-deletion`

## Verification Checklist (before submitting to Play)

- [ ] Site loads in incognito mode (no auth gate)
- [ ] All three anchor URLs scroll to correct sections
- [ ] Page mentions "FlexPilot" prominently
- [ ] Page mentions "Smartpace Technologies" prominently
- [ ] Account deletion section has clear instructions
- [ ] Privacy policy section is comprehensive (data collected, used, shared, rights)
- [ ] Terms of Service is present and comprehensive
- [ ] Mobile responsive
- [ ] HTTPS enabled
