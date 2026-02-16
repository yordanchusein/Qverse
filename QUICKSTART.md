# Quick Start: Deploy Qverse in 5 Minutes

Choose your preferred method and follow the steps below:

## 🚀 Option 1: GitHub Pages (Easiest - 2 Minutes)

**Requirements:** GitHub account only

1. **Enable GitHub Pages:**
   - Go to https://github.com/yordanchusein/Qverse/settings/pages
   - Under "Source", select branch: `main`
   - Click **Save**
   - ✅ Done! Your site will be live at: `https://yordanchusein.github.io/Qverse`

2. **Automatic Deployment:**
   - The GitHub Actions workflow will automatically build and deploy
   - Every push to `main` branch will trigger a new deployment
   - Check progress in the **Actions** tab

---

## 🎨 Option 2: Netlify (Best Performance - 3 Minutes)

**Requirements:** GitHub account

1. **One-Click Deploy:**
   - Go to [app.netlify.com](https://app.netlify.com)
   - Click **"Add new site"** → **"Import an existing project"**
   - Select **GitHub** and choose **Qverse** repository
   - Click **Deploy site**
   - ✅ Done! Your site is live at: `https://your-site.netlify.app`

2. **Custom Domain (Optional):**
   - Go to **Domain settings** in Netlify
   - Add your custom domain
   - Follow DNS instructions

---

## ⚡ Option 3: Vercel (Fastest Deployment - 2 Minutes)

**Requirements:** GitHub account

1. **One-Click Deploy:**
   - Go to [vercel.com](https://vercel.com)
   - Sign in with GitHub
   - Click **"Add New..."** → **"Project"**
   - Import **Qverse** repository
   - Click **Deploy**
   - ✅ Done! Your site is live at: `https://your-site.vercel.app`

---

## 📋 What You Get

All methods include:

✅ **FREE hosting**  
✅ **Automatic HTTPS/SSL**  
✅ **Fast CDN delivery**  
✅ **Automatic deployments on push**  
✅ **Custom domain support**  
✅ **99.9% uptime**

---

## 🔧 Local Development

Want to test locally first?

```bash
# 1. Clone the repository
git clone https://github.com/yordanchusein/Qverse.git
cd Qverse

# 2. Install dependencies
npm install

# 3. Build CSS
npm run build

# 4. Open in browser
# Simply open index.html in your browser
# OR use a local server:
npm run preview
```

Visit `http://localhost:8000`

---

## 📚 Need More Details?

- Full deployment guide: See [DEPLOYMENT.md](DEPLOYMENT.md)
- Project documentation: See [README.md](README.md)

---

## 🆘 Troubleshooting

**Site not loading?**
- Wait 2-3 minutes for first deployment
- Check that `index.html` is in the root directory
- Verify build status in platform dashboard

**CSS not applied?**
- Run `npm run build` locally first
- Ensure `src/output.css` exists
- Check build logs in platform dashboard

**Need help?**
- Open an issue on GitHub
- Check platform documentation links in README.md

---

**You're all set! 🎉 Choose a method above and deploy your site now!**
