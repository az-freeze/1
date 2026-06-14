# Arizona Freeze - Static Website for GitHub Pages

This is a complete static HTML website for Arizona Freeze appliance repair service, optimized for GitHub Pages hosting.

## Features

✓ **Fully Static** - Pure HTML, CSS, and JavaScript (no backend required)
✓ **GitHub Pages Ready** - Deploy directly to GitHub Pages
✓ **Responsive Design** - Mobile-first design works on all devices
✓ **SEO Optimized** - Meta tags, Open Graph, and schema markup
✓ **Contact Form** - Integrated with Formspree for email submissions
✓ **Fast Loading** - Minimal dependencies, optimized CSS
✓ **Professional Design** - International Typographic Style (white, red, black)

## File Structure

```
azfreeze-github-pages/
├── index.html              # Homepage
├── styles.css              # Main stylesheet
├── brands.html             # Brands page
├── service-areas.html      # Service areas page
├── services/
│   ├── refrigerator.html   # Service pages (add more as needed)
│   └── ...
├── README.md               # This file
└── .gitignore              # Git ignore file
```

## How to Deploy to GitHub Pages

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository
2. Name it `azfreeze` or `yourusername.github.io`
3. Make it public

### Step 2: Upload Files

**Option A: Using Git (Recommended)**

```bash
# Clone the repository
git clone https://github.com/yourusername/azfreeze.git
cd azfreeze

# Copy all files from azfreeze-github-pages/ into this directory
cp -r /path/to/azfreeze-github-pages/* .

# Add, commit, and push
git add .
git commit -m "Initial commit: Arizona Freeze website"
git push origin main
```

**Option B: Using GitHub Web Interface**

1. Go to your repository on GitHub
2. Click "Add file" → "Upload files"
3. Drag and drop all HTML and CSS files
4. Commit the changes

### Step 3: Enable GitHub Pages

1. Go to your repository settings
2. Scroll to "GitHub Pages" section
3. Select "main" branch as source
4. Click "Save"
5. Your site will be live at `https://yourusername.github.io/azfreeze/`

## Customization

### Update Contact Information

Replace these placeholders throughout all HTML files:

- `(XXX) XXX-XXXX` → Your actual phone number
- `service@azfreeze.com` → Your actual email
- `yourusername.github.io/azfreeze` → Your actual domain

### Update Contact Form

The contact form uses Formspree for email delivery:

1. Go to [Formspree.io](https://formspree.io)
2. Sign up and create a new form
3. Get your form ID
4. In `index.html`, replace `YOUR_FORM_ID` in the contact form with your actual ID:

```html
<form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### Add More Service Pages

1. Copy `services/refrigerator.html` as a template
2. Update the title, description, and content
3. Save as `services/service-name.html`
4. Add a link in `index.html` services grid

### Modify Colors

Edit `styles.css` and change the color variables:

```css
:root {
    --primary-red: #DC143C;    /* Main red color */
    --dark-black: #000000;     /* Black color */
    --white: #ffffff;          /* White color */
    --light-gray: #f5f5f5;     /* Light gray background */
}
```

## SEO Optimization

All pages include:
- ✓ Meta descriptions
- ✓ Open Graph tags for social sharing
- ✓ JSON-LD schema markup
- ✓ robots.txt (create in root directory)
- ✓ sitemap.xml (create in root directory)

### Create robots.txt

Create a file named `robots.txt` in the root directory:

```
User-agent: *
Allow: /

Sitemap: https://yourusername.github.io/azfreeze/sitemap.xml
```

### Create sitemap.xml

Create a file named `sitemap.xml` in the root directory:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://yourusername.github.io/azfreeze/</loc>
    <lastmod>2026-06-14</lastmod>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://yourusername.github.io/azfreeze/brands.html</loc>
    <lastmod>2026-06-14</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.9</priority>
  </url>
  <url>
    <loc>https://yourusername.github.io/azfreeze/service-areas.html</loc>
    <lastmod>2026-06-14</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.9</priority>
  </url>
</urlset>
```

## Google Search Console

1. Go to [Google Search Console](https://search.google.com/search-console)
2. Add your GitHub Pages URL
3. Verify ownership (add meta tag to `index.html`)
4. Submit your sitemap.xml

## Analytics

To add Google Analytics:

1. Create a Google Analytics account
2. Get your Measurement ID (G-XXXXXXXXXX)
3. Add this to the `<head>` of each HTML file:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

## Custom Domain

To use a custom domain (e.g., azfreeze.com):

1. Purchase a domain from a registrar (GoDaddy, Namecheap, etc.)
2. Add a CNAME record pointing to `yourusername.github.io`
3. In your GitHub repository settings, add the custom domain
4. GitHub will automatically create a CNAME file

## Performance Tips

- ✓ Images are optimized and minimal
- ✓ CSS is inline to reduce HTTP requests
- ✓ No JavaScript frameworks (pure HTML/CSS)
- ✓ Mobile-first responsive design
- ✓ Fast page load times

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Troubleshooting

### Pages not loading
- Check that all file paths are correct
- Ensure files are committed and pushed to GitHub
- Wait 5-10 minutes for GitHub Pages to rebuild

### Contact form not working
- Verify your Formspree form ID is correct
- Check that emails are being sent to your Formspree account
- Test the form with a test submission

### Styling issues
- Clear browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
- Check that styles.css is in the root directory
- Verify CSS file paths in HTML files

## Support

For issues or questions:
1. Check the [GitHub Pages documentation](https://docs.github.com/en/pages)
2. Review the [Formspree documentation](https://formspree.io/docs)
3. Test locally before pushing to GitHub

## License

MIT License - Feel free to use and modify this template.

---

**Last Updated:** June 14, 2026
**Version:** 1.0
