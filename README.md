# Calb Music Website

Official website for Calb Music, featuring:
- Longform Mashup Projects (YouTube visual albums)
- DJ Mixes (Mixcloud embeds)
- About and Contact pages
- Media coverage showcase

## 🌐 Live Site

**Target URL**: [www.calbmusic.com](https://www.calbmusic.com)

## 📋 DNS Configuration Required

⚠️ **Important**: If the website is not accessible, you need to configure DNS records at your domain registrar.

👉 **See [DNS-SETUP.md](./DNS-SETUP.md) for detailed instructions**

## 🚀 Deployment

This site is automatically deployed to GitHub Pages via GitHub Actions workflow when changes are pushed to the `main` branch.

### Workflow Status
The Jekyll deployment workflow builds and deploys the site automatically. You can check the deployment status in the [Actions tab](https://github.com/belacmu/Calb-Website/actions).

## 📁 Project Structure

```
/
├── index.html          # Home page with projects
├── about.html          # About page
├── contact.html        # Contact page  
├── projects.html       # Projects page
├── styles.css          # Main stylesheet
├── images/             # Image assets
├── favicon/            # Favicon files
├── mylist-player/      # YouTube playlist player
├── CNAME               # Custom domain configuration
└── .github/
    └── workflows/
        └── jekyll-gh-pages.yml  # Deployment workflow
```

## 🛠️ Local Development

To preview the site locally:

1. Clone the repository
2. Open `index.html` in your browser
3. Or use a local web server:
   ```bash
   python -m http.server 8000
   # Then visit http://localhost:8000
   ```

## 📝 Making Changes

1. Edit the HTML, CSS, or assets
2. Commit and push to the `main` branch
3. GitHub Actions will automatically build and deploy the changes
4. Changes will be live within a few minutes

## 📧 Contact

For bookings and inquiries, see the [contact page](https://www.calbmusic.com/contact.html).
