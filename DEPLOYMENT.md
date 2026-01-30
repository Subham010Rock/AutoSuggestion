# Deployment Guide for LSP (Monaco Editor + ATA)

This guide covers deploying your Monaco Editor with Automatic Type Acquisition (ATA) project to **Vercel** and **Render**.

---

## 🚀 Vercel Deployment (Recommended for Frontend)

### Prerequisites

- GitHub account with your project pushed to a repository
- Vercel account (sign up at [vercel.com](https://vercel.com))

### Steps

1. **Push to GitHub** (if not already done):

   ```bash
   git init
   git add .
   git commit -m "Initial commit: Monaco Editor with ATA"
   git remote add origin https://github.com/YOUR_USERNAME/lsp-monaco-editor.git
   git push -u origin main
   ```

2. **Deploy to Vercel**:
   - Go to [vercel.com/new](https://vercel.com/new)
   - Import your GitHub repository
   - Vercel auto-detects Vite configuration
   - Click **Deploy**

3. **Build Settings** (auto-detected):
   | Setting | Value |
   |---------|-------|
   | Framework | Vite |
   | Build Command | `npm run build` |
   | Output Directory | `dist` |

4. **Your Live URL**: `https://your-project-name.vercel.app`

---

## 🌐 Render Deployment (Static Site)

### Steps

1. **Push to GitHub** (same as above)

2. **Create Static Site on Render**:
   - Go to [render.com](https://render.com) → Dashboard
   - Click **New** → **Static Site**
   - Connect your GitHub repository

3. **Configure Build Settings**:
   | Setting | Value |
   |---------|-------|
   | Build Command | `npm install && npm run build` |
   | Publish Directory | `dist` |

4. **Deploy**: Click **Create Static Site**

5. **Your Live URL**: `https://your-project-name.onrender.com`

---

## 📁 Files Ready for Deployment

The project is already configured correctly:

- ✅ `vite.config.ts` - Build configuration
- ✅ `package.json` - Build scripts (`npm run build`)
- ✅ `tsconfig.json` - TypeScript configuration
- ✅ Static output in `dist/` after build

---

## 🔧 Pre-deployment Checklist

```bash
# Test the production build locally
npm run build
npm run preview
```

This ensures everything works before deploying.

---

## 💡 Pro Tips

1. **Custom Domain**: Both Vercel and Render support custom domains for free
2. **Environment Variables**: Not needed for this static project
3. **Auto-Deploy**: Both platforms auto-deploy on every `git push`

---

## 🔗 Quick Links

| Platform | Dashboard                                            |
| -------- | ---------------------------------------------------- |
| Vercel   | [vercel.com/dashboard](https://vercel.com/dashboard) |
| Render   | [dashboard.render.com](https://dashboard.render.com) |
