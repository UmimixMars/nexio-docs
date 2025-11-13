# Nexio Website

Official website for Nexio Discord bot - deployed via GitHub Pages.

## Features

- Multi-page static website with downtown purple theme
- Responsive mobile-first design
- Interactive accordions and mobile menu
- Premium tier comparison table
- Complete documentation for commands, premium plans, and support

## Pages

1. **index.html** - Home page with hero section and feature cards
2. **commands.html** - Complete command reference with collapsible sections
3. **premium.html** - Premium tier comparison and pricing
4. **support.html** - Support information and FAQ
5. **legal.html** - Terms of Service, Privacy Policy, and Refund Policy
6. **404.html** - Custom error page

## GitHub Pages Deployment Instructions

### Option 1: Deploy to GitHub Pages from `gh-pages` Branch

1. **Create a new repository on GitHub**
   - Go to https://github.com/new
   - Name your repository (e.g., `nexio-website`)
   - Make it public
   - Do NOT initialize with README, .gitignore, or license

2. **Initialize Git in your local project**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Nexio website"
   ```

3. **Create and switch to `gh-pages` branch**
   ```bash
   git branch -M gh-pages
   ```

4. **Add your GitHub repository as remote**
   ```bash
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   ```
   Replace `YOUR-USERNAME` with your GitHub username and `YOUR-REPO-NAME` with your repository name.

5. **Push to GitHub**
   ```bash
   git push -u origin gh-pages
   ```

6. **Enable GitHub Pages**
   - Go to your repository on GitHub
   - Click **Settings** > **Pages**
   - Under "Source", select branch: `gh-pages`
   - Click **Save**
   - Your site will be published at: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

### Option 2: Deploy from Main Branch

1. **Create a new repository on GitHub** (same as Option 1, step 1)

2. **Initialize Git and commit**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Nexio website"
   ```

3. **Rename branch to main**
   ```bash
   git branch -M main
   ```

4. **Add remote and push**
   ```bash
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   git push -u origin main
   ```

5. **Enable GitHub Pages**
   - Go to **Settings** > **Pages**
   - Under "Source", select branch: `main`
   - Select folder: `/ (root)`
   - Click **Save**

### Updating Your Website

After making changes to your website:

```bash
git add .
git commit -m "Update website"
git push origin gh-pages
```

Changes will be live within a few minutes.

### Custom Domain (Optional)

1. In your repository **Settings** > **Pages**
2. Enter your custom domain under "Custom domain"
3. Add a CNAME record in your domain's DNS settings pointing to `YOUR-USERNAME.github.io`

## Local Development

To preview the website locally, you can use any static server:

**Using Python:**
```bash
python3 -m http.server 5000
```

**Using Node.js (npx):**
```bash
npx serve -p 5000
```

Then open http://localhost:5000 in your browser.

## Technology Stack

- HTML5
- Tailwind CSS (via CDN)
- Vanilla JavaScript
- Jekyll (GitHub Pages)
- Inter Font (Google Fonts)

## GitHub Pages Requirements Met

✅ Static HTML/CSS/JS only - no server-side code  
✅ All files < 100MB each  
✅ Total repository < 1GB  
✅ Public repository ready  
✅ HTTPS enabled by default  
✅ Custom domain support  
✅ Custom 404.html included  
✅ Jekyll _config.yml included  
✅ Mobile-responsive design  
✅ No prohibited content  

## Support

For questions or issues with the bot, visit:
- Support Server: https://discord.gg/vMWuDvk4dZ
- Ko-fi: https://ko-fi.com/uximixmars

## License

© 2025 Nexio - Built with Python by Mars
