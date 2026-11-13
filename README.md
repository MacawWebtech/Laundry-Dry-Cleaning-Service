# FreshFold — Laundry & Dry Cleaning HTML Template

A premium, multi-page HTML5 template for laundry, dry cleaning and doorstep pickup-and-delivery businesses. Built with **Bootstrap 5.3**, **vanilla ES6+ JavaScript** and plain CSS — no build step, no frameworks.

**Version:** 1.6.7 · **Released:** 12 November 2026

---

## What's included

| | |
|---|---|
| **23 HTML pages** | 2 home layouts + 11 other public pages + 10 customer-dashboard pages |
| **Design system** | CSS variables, 8 px spacing scale, 2 Google Fonts, Bootstrap Icons |
| **Dark / light mode** | System preference detection, saved in `localStorage`, no flash on load |
| **RTL support** | One-click toggle for Arabic / Hebrew layouts |
| **Working JS** | Quick booking, 7-step pickup wizard, price estimator, live order tracking, orders table (search / filter / paginate), addresses, payments, support chat |
| **Accessibility** | WCAG 2.1 AA colours, skip link, focus states, ARIA labels, keyboard support, `prefers-reduced-motion` |
| **SEO** | Unique titles & meta descriptions, single H1 per page, JSON-LD (`DryCleaningOrLaundry`, `FAQPage`), Open Graph, `sitemap.xml`, `robots.txt` |
| **Performance** | Local photos bundled in `assets/images/`, lazy loading, explicit image sizes (CLS-safe), minified CSS/JS |
| **Integration placeholders** | Formspree / Netlify forms, Mailchimp, Google Maps, Stripe / PayPal / UPI, Chart.js, booking-calendar hook, live chat |

## Quick start

1. Unzip the package.
2. Open `pages/index.html` in your browser (or `index.html` at the root, which redirects there).
3. To publish, upload the whole folder to any static host — Netlify, Vercel, GitHub Pages, cPanel / Hostinger, S3.

> Forms run in **demo mode** until you add real endpoints, so every interaction works offline.

## Folder structure

```
freshfold/
├── index.html              → redirects to pages/index.html
├── sitemap.xml, robots.txt
├── README.md
├── assets/
│   ├── css/   style.css, dark-mode.css, rtl.css (+ .min.css)
│   ├── js/    main.js, dashboard.js (+ .min.js), plugins/
│   ├── images/ WebP + JPG illustrations (1200 px and 600 px), favicon.svg, og-image
│   └── fonts/  (empty — see README inside to self-host)
├── pages/     all 23 HTML pages
└── documentation/index.html   full guide (open in a browser)
```

## Pages

**Public:** `index` (Home 1 — Classic), `index-2` (Home 2 — Express), `services`, `service-details` (Dry Cleaning), `pricing`, `how-it-works`, `about`, `contact`, `login`, `register`, `forgot-password`, `404`, `coming-soon`

**Customer dashboard:** `dashboard`, `schedule-pickup`, `track-order`, `orders`, `order-details`, `payments`, `addresses`, `profile-settings`, `messages`, `notifications`

## Customize in 5 minutes

- **Colours & fonts** → `:root` at the top of `assets/css/style.css` (dark palette in `dark-mode.css`).
- **Banner photos** → each banner has `style="--ff-bg-img:url(...);--ff-bg-img-sm:url(...)"`; swap the URLs. Overlay strength is in section 22 of `style.css` (black overlay).
- **Brand name** → search & replace `FreshFold` across `pages/` and swap the logo markup (`.ff-logo`).
- **Phone, email, address, WhatsApp** → search the pages for `+91 80 4567 8900`, `hello@freshfold.example`, `918045678900`.
- **Service areas & prices** → `CONFIG` at the top of `assets/js/main.js` (pincodes, currency, surcharges, time slots).
- **Forms** → paste your Formspree ID into `CONFIG.formspreeEndpoint` / the contact form `action`; Mailchimp URL into `CONFIG.mailchimpEndpoint`.
- **Domain** → replace `https://www.freshfold.example` in page heads, `sitemap.xml` and `robots.txt`.

Every customization point is marked with a `TODO:` comment — search for it.

See **documentation/index.html** for the full installation, customization and integration guide.

## Browser support

Latest Chrome, Edge, Firefox, Safari (macOS & iOS) and Samsung Internet.

## Credits

- [Bootstrap 5.3](https://getbootstrap.com) — MIT
- [Bootstrap Icons](https://icons.getbootstrap.com) — MIT
- [Chart.js 4](https://www.chartjs.org) — MIT (dashboard only)
- Fonts: [Outfit](https://fonts.google.com/specimen/Outfit) & [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans) — SIL Open Font License
- Photos: bundled locally in `assets/images/` — no external image CDN. Swap in your own photos by replacing the files (or the paths in the HTML).

## Changelog

**1.6.7 — 13 Nov 2026** · About page team: real portrait photos (initials shown if a photo fails to load).

**1.6.6 — 13 Nov 2026** · Pricing estimator: photo with "Free pickup & delivery" caption fills the summary panel.

**1.6.5 — 13 Nov 2026** · Equal-height image + text rows on Services (4 sections), Dry Cleaning, How It Works (4 steps), About and Home 2 business.

**1.6.4 — 13 Nov 2026** · Home 2 reviews: equal-height cards with names aligned at the bottom; on tablets the third card spans the full row.

**1.6.3 — 13 Nov 2026** · Home 2 "For business": photo matches the text column height (`.ff-eqrow` / `.ff-eqimg` helpers).

**1.6.2 — 13 Nov 2026** · Home 2 services tabs: equal-height columns, photo fills the panel.

**1.6.1 — 13 Nov 2026** · New "How it works" design on Home 1: interactive step selector (tabs with progress bars) and a blue detail card that auto-advances, with keyboard support and reduced-motion respect.

**1.6.0 — 13 Nov 2026** · Black overlay on every banner photo (light and dark mode) with white text; cards inside banners keep normal colours.

**1.5.2 — 13 Nov 2026** · Direction toggle now shows the word "RTL" (or "LTR" while in right-to-left mode) instead of "عربي".

**1.5.1 — 13 Nov 2026** · Fixed service-card icons being partly hidden behind card photos; added customer photos to testimonials (initials shown if a photo can't load).

**1.5.0 — 12 Nov 2026** · Dark mode switched to true black (`#000` page, `#0a0a0a`/`#141414` surfaces, `#2a2a2a` borders) with blue accents.

**1.4.0 — 12 Nov 2026** · Blue colour scheme throughout: brand blue `#1a64e0` primary, blue-gradient CTAs, deep navy `#0d2547`, pale-blue highlights. No orange anywhere (including fallback illustrations).

**1.3.0 — 12 Nov 2026** · Photo backgrounds with tinted overlays on every banner (home heroes, page headers, CTA, coloured bands, app promo, auth panels, 404/coming-soon).

**1.4.0 — 13 Nov 2026** · New FreshFold logo: `assets/images/logo.png` (light backgrounds) and `logo-light.png` (footer, photo banners, dark mode), plus `favicon.png` / `apple-touch-icon.png`. To change the logo, replace these files and keep the names.

**1.3.0 — 13 Nov 2026** · All remote (Unsplash) image links removed; every photo and banner background now uses the bundled images in `assets/images/`.

**1.2.0 — 12 Nov 2026** · Real Unsplash photos replace the illustrations (WebP/JPG, 600 & 1200 px, automatic local fallback).

**1.1.0 — 12 Nov 2026** · Added Home 2 (Express layout): centered hero with booking bar, service tabs, comparison table, same-day band, monthly/yearly plan toggle, business section, app promo. Home dropdown in the header.

**1.0.0 — 12 Nov 2026** · Initial release.

## Support

Questions or a bug? Include your browser, the page and steps to reproduce when contacting support through the marketplace item page. *(TODO: add your support email / link.)*
