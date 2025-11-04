# GitHub Pages Setup Guide

This guide will help you set up GitHub Pages to host your Privacy Policy and Terms of Service.

## Step 1: Create a GitHub Repository

1. Go to GitHub.com and create a new repository
2. Name it `bank-on-it` (or your preferred name)
3. Make it public (required for free GitHub Pages)
4. Don't initialize with README (you already have files)

## Step 2: Upload Files to Repository

### Option A: Using GitHub Web Interface

1. Click "uploading an existing file" in your new repository
2. Upload the entire `docs` folder contents:
   - `index.html` (Privacy Policy)
   - `terms.html` (Terms and Conditions)
   - `_config.yml`
   - `README.md`

### Option B: Using Git Command Line

```bash
cd /Users/muhammadrohailnaveed/Documents/FlutterProjects/github/bank-on-it
git init
git add docs/
git commit -m "Add GitHub Pages documentation"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/bank-on-it.git
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on **Settings** tab
3. Scroll down to **Pages** section (left sidebar)
4. Under **Source**, select:
   - **Branch:** `main` (or `master`)
   - **Folder:** `/docs`
5. Click **Save**

## Step 4: Access Your Site

After a few minutes, your site will be available at:
```
https://YOUR_USERNAME.github.io/bank-on-it/
```

Or if repository name is different:
```
https://YOUR_USERNAME.github.io/REPOSITORY_NAME/
```

## Step 5: Update Links

1. Update `_config.yml` with your actual GitHub username:
   ```yaml
   url: https://yourusername.github.io
   baseurl: /bank-on-it
   ```

2. Update links in `index.html` and `terms.html` if needed

3. Update the support email in both HTML files:
   - Replace `Wyzemedialc@gmail.com` with your actual email

4. Update the dates:
   - Replace `[Date]` with actual dates in both HTML files

## Step 6: Custom Domain (Optional)

If you want to use a custom domain:

1. In GitHub Pages settings, enter your custom domain
2. Add a `CNAME` file in the `docs` folder with your domain name
3. Update DNS records as instructed by GitHub

## Updating Your Site

To update content:

1. Edit the HTML files locally
2. Commit and push changes:
   ```bash
   git add docs/
   git commit -m "Update privacy policy"
   git push
   ```
3. Changes will appear on your site within a few minutes

## Linking from Your App

You can link to your hosted pages from your app:

- Privacy Policy: `https://YOUR_USERNAME.github.io/bank-on-it/`
- Terms: `https://YOUR_USERNAME.github.io/bank-on-it/terms.html`

## Troubleshooting

**Site not loading?**
- Wait 5-10 minutes after enabling Pages
- Check that the branch and folder are correct in Settings
- Ensure files are in the `docs` folder (not root)

**Changes not appearing?**
- GitHub Pages can take a few minutes to rebuild
- Check for build errors in the Pages settings
- Clear your browser cache

**Need help?**
- GitHub Pages documentation: https://docs.github.com/en/pages
- Check GitHub Status: https://www.githubstatus.com/


