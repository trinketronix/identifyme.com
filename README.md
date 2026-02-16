# Identify Me - Landing Page

A single-page, production-ready landing website for Identify Me's AI-powered object recognition mobile app.

## 📁 File Structure

```
identify-me/
├── index.html          ← The entire website (all HTML, CSS, JS)
└── README.md           ← This file
```

**That's it!** This is a single-file website with no build process, no dependencies, no framework bloat.

---

## 🚀 Quick Start

### Local Testing

1. **Clone the repo**
   ```bash
   git clone https://github.com/yourusername/identify-me.git
   cd identify-me
   ```

2. **Open in browser**
   ```bash
   # Option A: Double-click index.html
   # Option B: Use a local server (recommended)
   python3 -m http.server 8000
   # Visit: http://localhost:8000
   ```

3. **Edit & refresh** to see changes instantly

### Deploy to Production

1. **Make changes locally**
2. **Commit and push to `main` branch**
   ```bash
   git add index.html
   git commit -m "Update landing page content"
   git push origin main
   ```
3. **Create a PR and merge to `main`**
4. **GitHub Actions automatically deploys to identifyme.com** ✅

---

## ✏️ How to Customize

### 1. **Update Text Content**

Find the section in `index.html` and edit:

**Hero Section (Main Headline)**
```html
<h1>
    Don't Waste Time.
    <span class="hero-highlight">Identify It Instantly.</span>
</h1>
<p>Your washing machine broke. You don't know where to start...</p>
```

**Problem Cards**
```html
<div class="problem-card">
    <h3>💸 Expensive Repairs</h3>
    <p>Calling a repair technician costs hundreds...</p>
</div>
```

**Features Section**
```html
<div class="feature">
    <div class="feature-icon">🤖</div>
    <h3>AI-Powered Recognition</h3>
    <p>State-of-the-art machine learning...</p>
</div>
```

**Donation Section**
```html
<div class="donation-card">
    <h3>☕ Buy a Coffee</h3>
    <p>Support ongoing development with a one-time donation...</p>
    <a href="https://ko-fi.com/yourname">Donate $5</a>
</div>
```

### 2. **Update Donation Links**

Replace with your actual payment platforms:

```html
<!-- Ko-fi (One-time) -->
<a href="https://ko-fi.com/yourname" target="_blank">Donate $5</a>

<!-- GitHub Sponsors (Monthly) -->
<a href="https://github.com/sponsors/yourusername" target="_blank">Start Monthly</a>

<!-- Patreon Alternative -->
<a href="https://patreon.com/identifyme" target="_blank">Become a Patron</a>

<!-- PayPal -->
<a href="https://paypal.me/identifyme" target="_blank">Donate Now</a>
```

### 3. **Update Social Links**

In the footer, update to your actual profiles:

```html
<a href="https://github.com/yourname" target="_blank" title="GitHub">
<a href="https://twitter.com/yourhandle" target="_blank" title="Twitter">
<a href="https://linkedin.com/company/identifyme" target="_blank" title="LinkedIn">
```

### 4. **Update App Download Links**

```html
<button class="btn-primary">Get the App</button>
```

Change to point to your app stores:

```html
<a href="https://play.google.com/store/apps/details?id=com.identifyme" class="btn-primary">
  Get on Google Play
</a>
<a href="https://apps.apple.com/app/identify-me/id1234567890" class="btn-secondary">
  Get on App Store
</a>
```

---

## 🎨 Customizing Design

### Colors

Edit the CSS variables at the top of `<style>`:

```css
:root {
    --primary-dark: #0a0e27;        /* Background color */
    --secondary-dark: #1a1f3a;      /* Card backgrounds */
    --accent-cyan: #00d9ff;         /* Primary accent */
    --accent-purple: #7c3aed;       /* Secondary accent */
    --accent-orange: #ff6b35;       /* Use case accent */
    --text-primary: #ffffff;        /* Main text */
    --text-secondary: #a8b5d1;      /* Secondary text */
}
```

**Example**: Change primary accent from cyan to green:
```css
--accent-cyan: #00ff00;
```

### Fonts

Find the `font-family` declaration:
```css
font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
```

Replace with your preferred font (e.g., `'Inter', 'Roboto'`, etc.)

### Spacing & Layout

- `padding: 6rem 5%` → Increase/decrease section padding
- `font-size: 2.8rem` → Adjust heading sizes
- `gap: 2rem` → Change spacing between cards

---

## 📱 Responsive Design

The site is **fully responsive** and automatically adapts to:
- ✅ Mobile (320px+)
- ✅ Tablet (768px+)
- ✅ Desktop (1024px+)

Test locally:
```bash
# Open DevTools: F12 or Cmd+Option+I
# Click device toggle (top left)
# Test on different sizes
```

---

## 🔧 Add New Sections

To add a new section (e.g., "Team", "Roadmap"):

1. **Copy an existing section structure**
   ```html
   <section class="your-section">
       <div class="section-header">
           <h2>Your Title</h2>
           <p>Your description</p>
       </div>
       <!-- Your content here -->
   </section>
   ```

2. **Add to navigation**
   ```html
   <ul>
       <li><a href="#your-section">Your Section</a></li>
   </ul>
   ```

3. **Add CSS styling** (copy an existing section's CSS and modify)

---

## 🐛 Common Tasks

### Change the main logo text
```html
<div class="logo">IDENTIFY ME</div>
```

### Add/remove a navigation link
```html
<nav>
    <ul>
        <li><a href="#section">Section Name</a></li>  <!-- Add here -->
    </ul>
</nav>
```

### Update footer copyright year
```html
<p>&copy; 2025 Identify Me...</p>
```

### Add a new donation platform
```html
<div class="donation-card">
    <h3>💳 Open Collective</h3>
    <p>Transparent community funding.</p>
    <a href="https://opencollective.com/identifyme">Contribute</a>
</div>
```

---

## 📊 Performance

- **No external dependencies** - Pure HTML/CSS/JS
- **Fast load time** - All styles inline, no HTTP requests for CSS/JS
- **SEO friendly** - Semantic HTML, clean structure
- **Mobile optimized** - Responsive design, fast rendering

---

## 🚀 Deployment

### Via GitHub Actions (Automatic)

1. Edit `index.html` locally
2. Commit: `git commit -m "Update landing page"`
3. Push: `git push origin main`
4. Create PR and merge to `main`
5. **GitHub Actions deploys automatically** ✅

View status: **GitHub repo → Actions tab**

### Manual FTP Upload (If needed)

```bash
# Using lftp
lftp -u username,password ftp.example.com
> set ssl:verify-certificate no
> put index.html
> cd /identifyme.com
> put index.html
> quit
```

---

## 🔍 Testing Checklist

Before deploying:

- [ ] All donation links point to correct URLs
- [ ] Social media links are correct
- [ ] App store links work (or removed)
- [ ] No typos in content
- [ ] Test on mobile (use DevTools)
- [ ] Test all navigation links scroll smoothly
- [ ] Colors look good in both light/dark environments

---

## 📝 Making Pull Requests

1. Create a feature branch
   ```bash
   git checkout -b feature/update-content
   ```

2. Make your changes to `index.html`

3. Test locally
   ```bash
   python3 -m http.server 8000
   ```

4. Commit with clear message
   ```bash
   git commit -m "Update donation platforms and social links"
   ```

5. Push and create PR
   ```bash
   git push origin feature/update-content
   ```

6. Merge when ready → **Auto-deploys to production** ✅

---

## ⚡ Tips for Developers

- **Use browser DevTools** (F12) to inspect and test changes
- **Uncomment unused sections** instead of deleting (easier to restore)
- **Keep section structure consistent** - easier to maintain
- **Test all links** before merging to main
- **Colors are CSS variables** - change once, applies everywhere
- **No build process needed** - edit and refresh, that's it!

---

## 📞 Need Help?

- **Local testing issues?** Use `python3 -m http.server`
- **Deployment problems?** Check GitHub Actions logs
- **Design changes?** Edit CSS variables or individual styles
- **Content updates?** Find the text and replace it

---

## 📄 File Info

- **Size**: ~35KB (uncompressed)
- **Load time**: <1 second on 4G
- **Browser support**: All modern browsers (Chrome, Firefox, Safari, Edge)
- **Last updated**: February 2025

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### What This Means

You are free to:
- Use this code for any purpose (commercial or personal)
- Modify and adapt the code
- Distribute and share the code
- Use it in your own projects

Just include the license and copyright notice.

**Happy coding! 🚀**