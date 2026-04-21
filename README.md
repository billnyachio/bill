# Bill Onyoni Portfolio — Netlify Deployment Guide

## Files in this folder
```
netlify-portfolio/
├── index.html       ← Your complete portfolio (static, no PHP)
├── netlify.toml     ← Netlify config (headers, redirects)
├── robots.txt       ← SEO
└── assets/
    └── img/
        └── profile.jpg  ← ADD YOUR PHOTO HERE
```

---

## Deploy to Netlify (3 methods)

### Method 1 — Drag & Drop (Easiest, 2 minutes)
1. Go to https://netlify.com → Sign up free (use GitHub or Google)
2. From the dashboard click **"Add new site"** → **"Deploy manually"**
3. Drag the entire `netlify-portfolio/` folder into the upload box
4. Done! Netlify gives you a URL like `https://random-name-123.netlify.app`
5. To rename: Site Settings → General → Site name → change it

### Method 2 — GitHub (Best for updates)
1. Create a free account at https://github.com
2. Create a new repository called `portfolio`
3. Upload all files in this folder to that repo
4. Go to https://netlify.com → "Add new site" → "Import from Git"
5. Connect GitHub → select your `portfolio` repo
6. Build settings: leave blank (no build command needed)
7. Publish directory: leave blank or type `.`
8. Click **Deploy site**
9. Every time you push changes to GitHub, Netlify auto-redeploys ✓

### Method 3 — Netlify CLI
```bash
npm install -g netlify-cli
cd netlify-portfolio
netlify deploy --prod
```

---

## After deploying — Set up your contact form

1. Go to your Netlify dashboard → your site → **Forms** tab
2. You will see the `contact` form listed after the first submission
3. Go to **Forms → Form notifications → Add notification → Email**
4. Enter your email: billonyoni@gmail.com
5. Now every contact form submission emails you instantly ✓

---

## Add your custom domain (e.g. billonyoni.com)

1. Buy a domain from Namecheap, GoDaddy, or Google Domains (~$10/year)
2. Netlify dashboard → your site → **Domain management → Add custom domain**
3. Follow the DNS instructions Netlify shows you
4. Netlify provides free SSL/HTTPS automatically ✓

---

## Add your profile photo

1. Put your photo in `assets/img/` named `profile.jpg`
2. Re-upload or push to GitHub
3. The portfolio will show your photo automatically

---

## Update the portfolio later

- **Via GitHub**: Edit `index.html` → commit → Netlify auto-deploys in ~30 seconds
- **Via drag & drop**: Re-drag the updated folder to Netlify dashboard

---

## Free tier limits (more than enough)
- Bandwidth: 100GB/month
- Build minutes: 300/month
- Forms: 100 submissions/month
- Sites: unlimited
- HTTPS: free always
