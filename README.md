# Qverse - Digital Islamic Education Platform

> **Bridging Gen Z with Qur'anic Values through Modern Technology**

Qverse is a digital Islamic education and advocacy platform designed specifically for Gen Z. It integrates Islamic education, short-form content (micro-dakwah), and worship tracking with modern Qur'anic values.

## 🌟 Features

### Four Main Pillars

1. **Smart Learning Paths** - Personalized Islamic education tailored to your level
2. **Micro-Dakwah** - 1-3 minute bite-sized Islamic content for quick learning
3. **Ramadhan Mode** - Worship scheduling and tracking during the holy month
4. **Impact Tracker** - Monitor your spiritual growth and progress

## 🚀 Quick Start

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yordanchusein/Qverse.git
cd Qverse
```

2. Install dependencies:
```bash
npm install
```

3. Build the CSS:
```bash
npm run build
```

4. Open `index.html` in your browser or use a local server:
```bash
npm run preview
```

Then visit `http://localhost:8000` in your browser.

## 🛠️ Development

To run the development server with live CSS rebuilding:

```bash
npm run dev
```

This will watch for changes in your CSS and automatically rebuild.

## 📦 Publishing (FREE Options)

This is a static website that can be deployed for **FREE** on multiple platforms. Choose the one that works best for you:

### Option 1: GitHub Pages (Recommended for Beginners)

**FREE** ✅ | **Easy** ✅ | **Custom Domain** ✅

1. Go to your GitHub repository settings
2. Navigate to **Pages** section (Settings > Pages)
3. Under "Source", select the branch (usually `main` or `master`)
4. Select `/` (root) as the folder
5. Click **Save**
6. Your site will be live at: `https://yourusername.github.io/Qverse`

**Custom Domain (Optional):**
- In the Pages settings, enter your custom domain
- Add a `CNAME` file to the root with your domain name

### Option 2: Netlify

**FREE** ✅ | **Easy** ✅ | **Best Performance** ✅

#### Method A: Drag & Drop (Easiest)

1. Go to [netlify.com](https://netlify.com)
2. Sign up/login (can use GitHub account)
3. Drag and drop your project folder
4. Done! Your site is live

#### Method B: Git Integration (Recommended)

1. Go to [netlify.com](https://netlify.com) and login
2. Click **"Add new site" > "Import an existing project"**
3. Choose **GitHub** and authorize
4. Select the **Qverse** repository
5. Build settings:
   - **Build command:** `npm run build`
   - **Publish directory:** `/` (root)
6. Click **Deploy site**
7. Your site will be live at: `https://your-site-name.netlify.app`

**Custom Domain:** Available in free tier!

### Option 3: Vercel

**FREE** ✅ | **Fast Deployment** ✅ | **Great DX** ✅

1. Go to [vercel.com](https://vercel.com)
2. Sign up/login with GitHub
3. Click **"Add New" > "Project"**
4. Import the **Qverse** repository
5. Vercel auto-detects settings, or configure:
   - **Build Command:** `npm run build`
   - **Output Directory:** `/` (root)
6. Click **Deploy**
7. Your site will be live at: `https://your-site-name.vercel.app`

**Custom Domain:** Available in free tier!

### Option 4: Render

**FREE** ✅ | **Simple** ✅

1. Go to [render.com](https://render.com)
2. Sign up/login with GitHub
3. Click **"New" > "Static Site"**
4. Connect the **Qverse** repository
5. Configure:
   - **Build Command:** `npm run build`
   - **Publish Directory:** `/` (root)
6. Click **Create Static Site**

### Option 5: Firebase Hosting

**FREE** ✅ | **Google Integration** ✅

1. Install Firebase CLI:
```bash
npm install -g firebase-tools
```

2. Login to Firebase:
```bash
firebase login
```

3. Initialize Firebase:
```bash
firebase init hosting
```

4. Deploy:
```bash
firebase deploy
```

## 📁 Project Structure

```
Qverse/
├── index.html          # Landing page
├── dashboard.html      # Main dashboard
├── package.json        # Dependencies and scripts
├── src/
│   ├── input.css      # Tailwind source
│   └── output.css     # Compiled CSS
├── assets/            # Images and media
├── icon/              # Icon files
└── README.md          # This file
```

## 🎨 Tech Stack

- **HTML5** - Semantic markup
- **CSS3** - Modern styling
- **Tailwind CSS v4.1.18** - Utility-first CSS framework
- **JavaScript** - Vanilla JS for interactions
- **Feather Icons** - Beautiful icon set
- **Google Fonts** - Quantico, Poppins, Noto Naskh Arabic

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License.

## 🌐 Live Demo

- GitHub Pages: `https://yordanchusein.github.io/Qverse`
- Netlify: [Deploy to get URL]
- Vercel: [Deploy to get URL]

## 📞 Support

For support, please open an issue in the GitHub repository.

---

**Made with ❤️ for the Muslim Ummah**
