# ��� My Photography Portfolio

A warm, green-themed personal photography portfolio website — built with pure HTML, CSS, and JavaScript. No frameworks, no dependencies. Just drop it on any host and go.

---

## ��� Project Structure

```
portfolio-site/
├── index.html        ← Your entire website (edit this)
├── images/           ← Put ALL your photos here
│   ├── me.jpg        ← Your profile / about photo
│   ├── hero.jpg      ← Hero section main photo
│   ├── photo1.jpg
│   ├── photo2.jpg
│   └── ...
└── README.md         ← This file
```

---

## ✏️ How to Personalise

Open `index.html` in any text editor (VS Code recommended) and find + replace the following:

| Placeholder | Replace with |
|---|---|
| `[Your Name]` | Your actual name |
| `[Your City]` | Your city |
| `your.name` | Your brand/domain name |
| `hello@yourname.com` | Your email |
| `+91 98765 43210` | Your phone/WhatsApp |
| `@yourhandle` | Your Instagram handle |
| `yourhandle` | Your Instagram username (in the link) |

---

## ��� Adding Your Photos

### 1. Profile photo (About section + Nav avatar)

Place your photo at `images/me.jpg`, then update:

```html
<!-- About section — find this block and replace the src -->
<div class="your-photo-circle">
  <img src="images/me.jpg" alt="Your Name — Photographer" />
</div>

<!-- Nav avatar — find this and replace the placeholder div -->
<div class="nav-avatar">
  <img src="images/me.jpg" alt="Your Name" />
</div>
```

### 2. Hero photo (main big image on the right)

Place your best shot at `images/hero.jpg`, then find:

```html
<div class="hero-photo-main">
  <img src="https://images.unsplash.com/..." alt="Portrait photography" />
```

Replace the `src` with:
```html
  <img src="images/hero.jpg" alt="Portrait photography" />
```

### 3. Gallery photos

Place your gallery photos in `images/` and update each masonry item. For each photo, update **both** the `data-src` (used for the lightbox) and the `src` (thumbnail):

```html
<div class="masonry-item reveal" data-src="images/photo1.jpg">
  <img src="images/photo1.jpg" alt="Portrait" loading="lazy"/>
  <div class="masonry-overlay"><span>Your Caption ↗</span></div>
</div>
```

You can add or remove as many `masonry-item` blocks as you like.

---

## ��� Updating Prices

Find the Services section in `index.html` and update the `.s-price` divs:

```html
<div class="s-price">Starting at ₹2,500</div>
```

Change the currency symbol (₹) and amount to match your pricing.

---

## ��� Deploying to Cloudflare Pages

### First time setup

```bash
# 1. Initialise git (if not already done)
git init

# 2. Stage all files
git add .

# 3. Commit
git commit -m "Initial portfolio site"

# 4. Add your GitHub/GitLab remote
git remote add origin https://github.com/yourusername/your-repo.git

# 5. Push
git push -u origin main
```

Then in **Cloudflare Pages**:
1. Go to [pages.cloudflare.com](https://pages.cloudflare.com)
2. Click **Create a project → Connect to Git**
3. Select your repo
4. Build settings:
   - **Framework preset:** None
   - **Build command:** *(leave blank)*
   - **Build output directory:** *(leave blank)*
5. Click **Save and Deploy**

### Connecting your custom domain

1. In Cloudflare Pages → your project → **Custom Domains**
2. Click **Set up a custom domain**
3. Enter your domain name
4. If domain is already on Cloudflare → DNS is added automatically ✅
5. Wait 1–2 minutes — you're live!

### Pushing future updates

Every push to `main` triggers an automatic redeploy (~30 seconds):

```bash
git add .
git commit -m "Updated photos and pricing"
git push
```

---

## ��� Design Notes

- **Colours:** Light green & white palette with sage, mint, and deep forest green accents
- **Fonts:** Playfair Display (headings) + DM Sans (body) — loaded from Google Fonts
- **Patterns:** 4 hand-crafted SVG botanical patterns used as section backgrounds
- **Your photo:** Displayed in a circular frame with a glowing green ring and animated spinning leaf wreath in the About section
- **Gallery:** Masonry grid with hover overlays and a full click-to-open lightbox (keyboard navigation supported: ← → Esc)
- **Custom cursor:** Green dot + trailing ring
- **Marquee strip:** Scrolling text band between Hero and Gallery
- **Mobile:** Fully responsive with hamburger menu

---

## ��� Recommended Tools

- **Code editor:** [VS Code](https://code.visualstudio.com/) (free)
- **Git GUI (optional):** [GitHub Desktop](https://desktop.github.com/) — easier than command line
- **Image optimisation:** Compress your photos at [squoosh.app](https://squoosh.app) before uploading (keeps the site fast)
- **Recommended photo size:** Max 1200px wide, under 300KB each

---

## ��� Contact Form Note

The contact form currently shows a success message on submit but **does not actually send emails** — it's UI only. To make it fully functional, consider connecting it to a free service like:

- [Formspree](https://formspree.io) — just change the form action, free tier available
- [Web3Forms](https://web3forms.com) — easy setup, no backend needed

---

Made with ��� and lots of love for photography.

