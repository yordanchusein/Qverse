# Deployment Guide for Qverse

This guide provides detailed instructions for deploying Qverse to various free hosting platforms.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Before You Deploy](#before-you-deploy)
- [Deployment Options](#deployment-options)
  - [GitHub Pages](#github-pages)
  - [Netlify](#netlify)
  - [Vercel](#vercel)
  - [Render](#render)
  - [Firebase Hosting](#firebase-hosting)
- [Post-Deployment](#post-deployment)
- [Troubleshooting](#troubleshooting)

## Prerequisites

- Node.js installed (v14 or higher)
- npm or yarn package manager
- Git installed and configured
- A GitHub account (for most options)

## Before You Deploy

1. **Build the project:**
   ```bash
   npm install
   npm run build
   ```

2. **Test locally:**
   ```bash
   npm run preview
   ```
   Visit `http://localhost:8000` to ensure everything works.

3. **Commit your changes:**
   ```bash
   git add .
   git commit -m "Prepare for deployment"
   git push origin main
   ```

## Deployment Options

---

### GitHub Pages

**Best for:** Beginners, simple static sites  
**Cost:** FREE  
**Custom Domain:** Yes (FREE)  
**Deploy Time:** ~1-2 minutes  
**URL Format:** `https://username.github.io/Qverse`

#### Steps:

1. **Push your code to GitHub:**
   ```bash
   git add .
   git commit -m "Deploy to GitHub Pages"
   git push origin main
   ```

2. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Click **Settings** → **Pages**
   - Under "Source", select:
     - Branch: `main` (or `master`)
     - Folder: `/ (root)`
   - Click **Save**

3. **Wait for deployment:**
   - GitHub will build and deploy automatically
   - Check the green checkmark in the Actions tab
   - Your site will be live in 1-2 minutes

4. **Access your site:**
   - URL: `https://yourusername.github.io/Qverse`

#### Custom Domain (Optional):

1. In GitHub Pages settings, add your domain
2. Create a `CNAME` file in the root:
   ```
   yourdomain.com
   ```
3. Configure DNS with your domain provider:
   - Add A records pointing to GitHub's IPs:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - Or add CNAME record: `username.github.io`

---

### Netlify

**Best for:** Advanced features, best performance  
**Cost:** FREE  
**Custom Domain:** Yes (FREE)  
**Deploy Time:** ~30 seconds  
**URL Format:** `https://your-site-name.netlify.app`

#### Method 1: Drag & Drop (Easiest)

1. **Build the project locally:**
   ```bash
   npm install
   npm run build
   ```

2. **Deploy:**
   - Go to [app.netlify.com](https://app.netlify.com)
   - Sign up/login
   - Drag and drop your entire project folder
   - Done! Site is live instantly

#### Method 2: Git Integration (Recommended)

1. **Connect to Netlify:**
   - Go to [app.netlify.com](https://app.netlify.com)
   - Click **"Add new site"** → **"Import an existing project"**
   - Choose **GitHub** and authorize

2. **Select repository:**
   - Choose the **Qverse** repository
   - Click **Deploy site**

3. **Configure build settings** (auto-detected from `netlify.toml`):
   - Build command: `npm run build`
   - Publish directory: `.` (current directory)

4. **Deploy:**
   - Click **Deploy site**
   - Wait ~30 seconds
   - Your site is live!

5. **Custom domain:**
   - Go to **Domain settings**
   - Click **Add custom domain**
   - Follow DNS configuration instructions

#### Netlify CLI (Alternative):

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login
netlify login

# Initialize
netlify init

# Deploy
netlify deploy --prod
```

---

### Vercel

**Best for:** Fast deployment, great developer experience  
**Cost:** FREE  
**Custom Domain:** Yes (FREE)  
**Deploy Time:** ~20 seconds  
**URL Format:** `https://your-site-name.vercel.app`

#### Steps:

1. **Connect to Vercel:**
   - Go to [vercel.com](https://vercel.com)
   - Sign up/login with GitHub

2. **Import project:**
   - Click **"Add New..."** → **"Project"**
   - Import the **Qverse** repository

3. **Configure** (auto-detected from `vercel.json`):
   - Framework Preset: Other
   - Build Command: `npm run build`
   - Output Directory: `.`
   - Install Command: `npm install`

4. **Deploy:**
   - Click **Deploy**
   - Wait ~20 seconds
   - Your site is live!

5. **Custom domain:**
   - Go to project **Settings** → **Domains**
   - Add your custom domain
   - Configure DNS as instructed

#### Vercel CLI (Alternative):

```bash
# Install Vercel CLI
npm install -g vercel

# Login
vercel login

# Deploy
vercel

# Deploy to production
vercel --prod
```

---

### Render

**Best for:** Simple deployment, good free tier  
**Cost:** FREE  
**Custom Domain:** Yes (FREE on paid plans, but deployment is free)  
**Deploy Time:** ~1-2 minutes  
**URL Format:** `https://your-site-name.onrender.com`

#### Steps:

1. **Connect to Render:**
   - Go to [render.com](https://render.com)
   - Sign up/login with GitHub

2. **Create static site:**
   - Click **"New"** → **"Static Site"**
   - Connect the **Qverse** repository

3. **Configure:**
   - Name: `qverse` (or your choice)
   - Branch: `main`
   - Build Command: `npm run build`
   - Publish Directory: `.`

4. **Deploy:**
   - Click **"Create Static Site"**
   - Wait 1-2 minutes
   - Your site is live!

---

### Firebase Hosting

**Best for:** Google ecosystem integration  
**Cost:** FREE  
**Custom Domain:** Yes (FREE)  
**Deploy Time:** ~1 minute  
**URL Format:** `https://your-project.web.app`

#### Steps:

1. **Create Firebase project:**
   - Go to [console.firebase.google.com](https://console.firebase.google.com)
   - Click **"Add project"**
   - Follow the setup wizard

2. **Install Firebase CLI:**
   ```bash
   npm install -g firebase-tools
   ```

3. **Login to Firebase:**
   ```bash
   firebase login
   ```

4. **Initialize Firebase:**
   ```bash
   firebase init hosting
   ```
   - Select your Firebase project
   - Public directory: `.` (current directory)
   - Configure as single-page app: `No`
   - Set up automatic builds: `No`

5. **Build the project:**
   ```bash
   npm run build
   ```

6. **Deploy:**
   ```bash
   firebase deploy
   ```

7. **Access your site:**
   - URL will be shown in the terminal
   - Format: `https://your-project.web.app`

---

## Post-Deployment

### Verify Deployment

1. Visit your deployed URL
2. Test all pages:
   - Landing page (index.html)
   - Dashboard (dashboard.html)
3. Check responsive design on mobile
4. Verify all images load correctly
5. Test all navigation links

### Update Your Site

Whenever you make changes:

1. **Edit files locally**
2. **Test locally:**
   ```bash
   npm run dev
   ```
3. **Build:**
   ```bash
   npm run build
   ```
4. **Commit and push:**
   ```bash
   git add .
   git commit -m "Update content"
   git push origin main
   ```
5. **Auto-deploy:** Most platforms auto-deploy on push

### Monitor Performance

- **Netlify:** Check Analytics dashboard
- **Vercel:** Check Analytics and Speed Insights
- **GitHub Pages:** Use Google Analytics (add script)
- **Firebase:** Check Firebase Console for analytics

---

## Troubleshooting

### Build Fails

**Problem:** "npm install failed"  
**Solution:**
```bash
rm -rf node_modules package-lock.json
npm install
npm run build
```

**Problem:** "Tailwind CSS not compiling"  
**Solution:**
```bash
npm install @tailwindcss/cli tailwindcss
npm run build
```

### Site Not Loading

**Problem:** Blank page or 404 errors  
**Solution:**
- Check that `index.html` is in the root directory
- Verify publish directory is set to `.` or `/`
- Check browser console for errors

### Images Not Showing

**Problem:** Images return 404  
**Solution:**
- Verify image paths are relative (not absolute)
- Check that `assets/` and `icon/` folders are deployed
- Ensure case-sensitive paths match exactly

### CSS Not Applied

**Problem:** Site has no styling  
**Solution:**
- Run `npm run build` before deploying
- Check that `src/output.css` exists and is up to date
- Verify CSS path in HTML files is correct

### Custom Domain Issues

**Problem:** Custom domain not working  
**Solution:**
- Wait 24-48 hours for DNS propagation
- Verify DNS records are correct
- Check SSL certificate status (auto-generated)
- Use DNS checker: `https://dnschecker.org`

---

## Need Help?

- 📖 [GitHub Pages Docs](https://docs.github.com/en/pages)
- 📖 [Netlify Docs](https://docs.netlify.com)
- 📖 [Vercel Docs](https://vercel.com/docs)
- 📖 [Render Docs](https://render.com/docs)
- 📖 [Firebase Docs](https://firebase.google.com/docs/hosting)

---

**Happy Deploying! 🚀**
