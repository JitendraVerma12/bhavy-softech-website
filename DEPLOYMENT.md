# GitHub Deployment Guide

This guide will help you deploy your Bhavy Softech website to GitHub and GitHub Pages.

## Method 1: GitHub Pages (Free Hosting)

### Step 1: Create a GitHub Repository

1. Go to [GitHub.com](https://github.com) and sign in
2. Click the **"+"** button in the top right corner
3. Select **"New repository"**
4. Name your repository: `bhavy-softech-website`
5. Set it to **Public** (required for free GitHub Pages)
6. Check **"Add a README file"**
7. Click **"Create repository"**

### Step 2: Upload Your Files

**Option A: Using GitHub Web Interface**
1. In your new repository, click **"uploading an existing file"**
2. Drag and drop these files:
   - `index.html`
   - `styles.css`
   - `script.js`
   - `README.md`
3. Write a commit message: "Initial website upload"
4. Click **"Commit changes"**

**Option B: Using Git Commands** (if you have Git installed)
```bash
# Clone your repository
git clone https://github.com/YOUR_USERNAME/bhavy-softech-website.git
cd bhavy-softech-website

# Copy your website files to this folder
# (copy index.html, styles.css, script.js, README.md)

# Add and commit files
git add .
git commit -m "Initial website upload"
git push origin main
```

### Step 3: Enable GitHub Pages

1. In your repository, go to **Settings** tab
2. Scroll down to **"Pages"** in the left sidebar
3. Under **"Source"**, select **"Deploy from a branch"**
4. Choose **"main"** branch and **"/ (root)"** folder
5. Click **"Save"**

### Step 4: Access Your Live Website

After 5-10 minutes, your website will be live at:
```
https://YOUR_USERNAME.github.io/bhavy-softech-website/
```

## Method 2: Other Hosting Platforms

### Netlify (Alternative Free Option)
1. Go to [netlify.com](https://netlify.com)
2. Sign up with your GitHub account
3. Click **"New site from Git"**
4. Connect your GitHub repository
5. Deploy settings:
   - Build command: (leave empty)
   - Publish directory: (leave empty)
6. Click **"Deploy site"**

### Vercel (Alternative Free Option)
1. Go to [vercel.com](https://vercel.com)
2. Sign up with your GitHub account
3. Click **"New Project"**
4. Import your GitHub repository
5. Click **"Deploy"**

## Custom Domain (Optional)

If you want to use a custom domain like `www.bhavysoftech.com`:

1. Buy a domain from a registrar (GoDaddy, Namecheap, etc.)
2. In your GitHub repository settings → Pages
3. Add your custom domain in the **"Custom domain"** field
4. Update your domain's DNS settings to point to GitHub Pages:
   ```
   CNAME record: www → YOUR_USERNAME.github.io
   A records: @ → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   ```

## Repository Structure

Your final GitHub repository should look like:
```
bhavy-softech-website/
├── index.html
├── styles.css
├── script.js
├── README.md
└── DEPLOYMENT.md (this file)
```

## Benefits of GitHub Deployment

- **Free hosting** with GitHub Pages
- **Automatic SSL certificate** (HTTPS)
- **Easy updates** - just push new code
- **Version control** - track all changes
- **Custom domains** supported
- **Global CDN** for fast loading
- **No server maintenance** required

## Updating Your Website

To update your website after deployment:

1. Make changes to your local files
2. Upload the updated files to GitHub (replace existing ones)
3. Your live website will update automatically within minutes

## Troubleshooting

**Website not loading?**
- Wait 10-15 minutes after initial setup
- Check that GitHub Pages is enabled in Settings
- Ensure `index.html` is in the root directory

**Images not showing?**
- All image URLs are external (Pixabay), so they should work fine
- No additional setup needed for images

**Custom domain not working?**
- DNS changes can take 24-48 hours to propagate
- Double-check your DNS settings with your domain provider

---

Your Bhavy Softech website will be live and accessible worldwide once deployed!