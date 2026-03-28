# Digital Startos — Agency Website

A single-file, fully responsive agency website for **Digital Startos** — a digital agency offering web development, app development, Shopify/e-commerce, and digital marketing services.

---

## 📁 File Structure

```
digital-startos.html   ← The entire website (HTML + CSS + JS in one file)
README.md              ← This file
```

No frameworks. No build tools. No dependencies. Just open the HTML file in a browser.

---

## 🚀 Features

- **Single-file architecture** — everything in one `.html` file, zero setup required
- **Fully responsive** — mobile, tablet, and desktop layouts
- **Custom cursor** — neon dot + follower (desktop only)
- **Smooth scroll animations** — scroll reveal on all sections
- **Floating particle effect** — subtle ambient particles on the hero
- **Marquee trust strip** — infinite scrolling capability highlights
- **Mobile hamburger menu** — full-screen overlay nav for small screens
- **Floating WhatsApp button** — fixed CTA with tooltip, always visible
- **Contact form** — with service dropdown and submit feedback state
- **Scroll-aware navbar** — transparent → frosted glass on scroll

---

## 🧩 Sections

| Section | ID | Description |
|---|---|---|
| Navbar | — | Fixed, scroll-aware with mobile menu |
| Hero | `#home` | Headline, CTAs, founder note, key pillars |
| Trust Strip | — | Scrolling marquee of capability highlights |
| Services | `#services` | 5 service cards with hover effects |
| What You Get | — | 4 client commitment cards |
| Our Work | `#work` | Concept/demo portfolio grid |
| Why Us | `#why` | 4 differentiator cards |
| Process | `#process` | 4-step connected process flow |
| Founding Offer | — | First-client special offer section |
| Pricing | `#pricing` | 3-tier pricing cards |
| Final CTA | — | Full-width conversion section |
| Contact | `#contact` | Split layout — info + contact form |
| Footer | — | Links, socials, copyright |

---

## ✏️ How to Customize

### 1. Update Contact Details
Search and replace all placeholder contact info:

```
+91 99999 99999        →  your actual phone number
hello@digitalstartos.com  →  your actual email
https://wa.me/919999999999  →  your actual WhatsApp link
```

### 2. Update the Logo / Brand Name
Find `Digital<span>Startos</span>` — appears in the navbar and footer.

### 3. Add Real Portfolio Work
In the `#work` section, each `.portfolio-card` has:
- An emoji placeholder in `.portfolio-card-img` — replace with a real screenshot using `<img>`
- `.portfolio-cat` — update the category label
- `.concept-badge` — remove this once you have real client work
- `.portfolio-info h4` and `span` — update with real project name and result

**Example — replacing an emoji card with a real screenshot:**
```html
<!-- Before -->
<div class="portfolio-card-img pc-1">🛒</div>

<!-- After -->
<div class="portfolio-card-img" style="padding:0">
  <img src="your-screenshot.jpg" alt="Project Name"
       style="width:100%;height:100%;object-fit:cover;">
</div>
```

### 4. Connect the Contact Form
The form currently shows a visual success state only — no data is actually sent. To make it functional:

**Option A — Formspree (free, no backend needed):**
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
  <!-- wrap existing inputs inside this form tag -->
</form>
```

**Option B — WhatsApp redirect on submit:**
```javascript
function handleFormSubmit(btn) {
  const name = document.querySelector('input[type="text"]').value;
  const msg = encodeURIComponent(`Hi, I'm ${name}. I'd like to discuss a project.`);
  window.open(`https://wa.me/919999999999?text=${msg}`, '_blank');
}
```

### 5. Add Social Media Links
In the footer, replace the `href="#"` placeholders:
```html
<a href="https://instagram.com/yourhandle" class="social-btn">📸</a>
<a href="https://linkedin.com/company/yourcompany" class="social-btn">💼</a>
<a href="https://twitter.com/yourhandle" class="social-btn">🐦</a>
<a href="https://youtube.com/@yourchannel" class="social-btn">▶️</a>
```

### 6. Update Pricing
Pricing cards are in the `#pricing` section. Find `.price-amount` to change numbers. The "Growth" card is marked featured — adjust which one is highlighted by moving the `featured` class.

---

## 🎨 Design Tokens

All colors are defined as CSS variables at the top of the `<style>` block:

```css
:root {
  --purple: #7C3AED;
  --purple-light: #A855F7;
  --blue: #2563EB;
  --neon: #00F5FF;       /* primary accent */
  --neon2: #39FF14;      /* secondary accent */
  --pink: #EC4899;
  --dark: #030712;       /* page background */
  --dark2: #0D0F1A;
  --dark3: #111827;
  --glass: rgba(255,255,255,0.04);
  --glass-border: rgba(255,255,255,0.08);
  --text: #F9FAFB;
  --text-muted: #9CA3AF;
  --text-dim: #6B7280;
}
```

Change `--neon` to change the primary accent color across the whole site.

---

## 🌐 Fonts Used

Loaded from Google Fonts — requires internet connection to render correctly.

| Font | Usage |
|---|---|
| [Cabinet Grotesk](https://fonts.google.com/specimen/Cabinet+Grotesk) | Headings, logo, step numbers |
| [Instrument Sans](https://fonts.google.com/specimen/Instrument+Sans) | Body text, buttons, labels |

---

## 📦 Deployment

### GitHub Pages
1. Create a repo (e.g. `digitalstartos-website`)
2. Upload `digital-startos.html`
3. Rename it to `index.html`
4. Go to **Settings → Pages → Source → main branch**
5. Your site is live at `https://yourusername.github.io/digitalstartos-website/`

### Netlify (Drag & Drop)
1. Go to [netlify.com](https://netlify.com) → **Add new site → Deploy manually**
2. Rename the file to `index.html`
3. Drag the file into the Netlify drop zone
4. Live in under 60 seconds with a free `.netlify.app` URL

### Vercel
1. Push to a GitHub repo
2. Import the repo at [vercel.com](https://vercel.com)
3. Vercel auto-detects static HTML — no config needed

---

## 📋 Checklist Before Going Live

- [ ] Replace all `+91 99999 99999` with real phone number
- [ ] Replace `hello@digitalstartos.com` with real email
- [ ] Update WhatsApp link with real number
- [ ] Add real social media links in the footer
- [ ] Connect or redirect the contact form
- [ ] Replace concept portfolio cards with real work (when available)
- [ ] Update copyright year if needed (`© 2025`)
- [ ] Test on mobile before sharing

---

## 🛠️ Browser Support

Works in all modern browsers. Custom cursor is desktop-only — automatically inactive on touch devices. No polyfills needed.

---

*Built by Digital Startos. Single file. Zero dependencies. Ready to ship.*
