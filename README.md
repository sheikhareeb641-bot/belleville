# Belleville Dental

**Tagline:** *Your Smile. Your Health. Your Knowledge.*

A complete, professional, fully responsive **multi-page** dental education and information portal
built with **HTML5, CSS3, Bootstrap 5, JavaScript, jQuery** and vanilla front-end data.

---

## 📁 Project Structure

```
Belleville-Dental/
│
├── index.html                    # Home page (cinematic hero video)
├── professional-education.html   # Courses, documents, faculty/student resources, case studies
├── patient-education.html        # Decay, gums, brushing, flossing, prevention, FAQ
├── symptom-checker.html          # Interactive symptom checker with local guidance engine
├── research.html                 # Latest research, articles, documents, videos, media library
├── products.html                 # Product catalogue with filters, search, sort & star ratings
├── gallery.html                  # Responsive gallery + filters + lightbox
├── doctors.html                  # Our dental team, bios, specialty filters
├── kids-dental.html              # Kids education + two playable browser games
├── about.html                    # Mission, purpose, organization information
├── queries.html                  # Query form with JavaScript validation
├── contact.html                  # Contact info, form, hours, map placeholder, social links
├── sitemap.html                  # Complete sitemap of every page
│
├── css/
│   └── styles.css                # All styling (Belleville clinical dentistry theme)
│
├── js/
│   ├── script.js                 # All behaviour (data, filters, rating, ticker, forms…)
│   ├── symptom-checker.js        # Symptom checker scoring + guidance engine
│   ├── kids-game.js              # Brush-the-teeth + Healthy Food Matcher games
│   ├── chatbot.js                # On-site assistant widget (rules + quick replies)
│   └── bg-animation.js           # Lightweight animated background layer (canvas particles)
│
├── assets/
│   ├── logo.svg                  # Belleville Dental logo
│   ├── videos/dental-hero.mp4    # Looping hero background video
│   ├── images/                   # Dental / clinic / education photography (47 files)
│   ├── products/                 # 20 product photographs (JPG)
│   ├── doctors/                  # 6 doctor profile photographs (JPG)
│   └── pdfs/                     # 27 downloadable guide, resource & research PDFs
│
└── README.md
```

> **No backend required.** Open `index.html` in a browser (or serve the folder with any static server).

---

## 🧭 Pages & Navigation

All 13 pages share the **same responsive navbar and footer**, and the active page is highlighted
automatically. The mobile hamburger menu opens/closes smoothly on tablets and phones.

**Navigation layout** — 8 top-level links plus two dropdowns:

- **Home · Education ▾ · Research · Explore ▾ · Doctors · Kids Dental · About Us · Queries · Contact Us · Sitemap**
- **Education ▾** → Professional Education, Patient Education, *Symptom Checker* (divider separates the new page)
- **Explore ▾** → Gallery, Products
- The active page highlights both its dropdown item and the parent dropdown label.

| # | Page | Highlights |
|---|------|------------|
| 1 | `index.html` | Hero video, intro, quick-access cards, featured education/research/products, gallery preview, CTA |
| 2 | `professional-education.html` | Education assistance, 5 resource categories, search + category filters, **12 downloadable PDFs** |
| 3 | `patient-education.html` | 7 oral-health topics, awareness cards, **7 downloadable patient-guide PDFs**, tips, FAQ accordion |
| 5 | `research.html` | Spotlight, filterable research library, media library, video modal, **8 downloadable PDFs** |
| 6 | `products.html` | 20 products, 5 categories, search, sort, **interactive 1–5 star rating** |
| 7 | `gallery.html` | 22 images, category filters, hover zoom, keyboard-friendly lightbox |
| 8 | `doctors.html` | 6 sample doctor profiles, bios, expertise tags, specialty filters |
| 9 | `kids-dental.html` | Kid-friendly lessons + **two playable games** (brushing & food matcher) |
| 10 | `about.html` | Purpose, mission/vision, values, timeline, organization details |
| 11 | `queries.html` | Validated query form + success notification |
| 12 | `contact.html` | Email/phone/address cards, contact form, hours, map, social icons |
| 13 | `sitemap.html` | Grouped sitemap cards + full page directory |

---

## ⚙️ Key Features

- **Light theme** — bright, clean clinical dentistry look on every page (single light theme,
  no toggle).
- **Symptom Checker** (`symptom-checker.html`) — 4-step form (area → symptoms → duration →
  warning signs) with validation messages, local scoring engine → **Routine / See a dentist
  within a few days / Urgent** results, likely-cause list, numbered advice, summary line, toast
  and reset. Runs fully client-side in `js/symptom-checker.js`.
- **On-site chatbot** — fixed launcher button (bottom-right) opens a chat assistant on every page.
  It answers questions about opening hours, appointments, location, prices, services, tooth pain,
  kids care, products and more from a local rule engine, shows inline links to the right pages and
  offers quick-reply chips. Type, press Enter or Esc to close — all in `js/chatbot.js`. Replaces the
  old “Back to Top” button.
- **Downloadable PDF library** — 27 self-contained PDFs in `assets/pdfs/` (course syllabi, faculty &
  student resources, case studies, patient guides and research briefs). Education and Research cards
  render real “Open PDF” links, and the Patient Education page has a *Downloadable Guides* section —
  every file opens inline in a new tab or saves with `download`.
- **Cinematic hero video** — autoplaying, muted, looping `assets/videos/dental-hero.mp4` with a
  gradient tint for readable text, poster fallback (`hero-clinic.jpg`), and reduced-motion fallback
  (video hidden, poster background stays)
- **Visitor counter** (top-right, `localStorage` front-end demo) — displays `Visitors: 001245`
- **Date / Time / Location ticker** fixed at the bottom of every page
  - Updates the clock every second
  - Uses the **HTML5 Geolocation API** + free reverse-geocoding
  - Falls back to `Location unavailable` when permission is denied — never breaks the page
- **Navbar behaviour**: scroll effect, hover colour, click colour flash, active-page highlight
- **Doctors page**: 6 profiles with circular photos, qualifications, experience chips, bios and a
  specialty filter that updates the "Showing X of 6" counter
- **Kids page**: lesson cards with facts, mascot/speech-bubble visual, plus two games —
  **Brush the Teeth** (30s timer, plaque targets, score) and **Healthy Food Matcher** (8-card memory
  style score game) — both fully client-side in `js/kids-game.js`
- **Product system**: search → filter by category → sort (price / rating / name) → rate 1–5 stars
  (ratings persist in `localStorage`)
- **Forms**: required-field + email + message validation, inline error messages, success banner, toast
- **Animations**: page fade-in, staggered header rise, hero entrance, scroll-reveal, card lift, image
  zoom, button hover, navbar transitions — all disabled under `prefers-reduced-motion`
- **Responsive**: desktop multi-column, tablet 2–3 columns, mobile hamburger + single column, no horizontal scrolling

---

## 🎨 Design Theme

| Token | Colour |
|-------|--------|
| Primary (clinical blue) | `#0E6BA8` |
| Primary dark | `#0A4F7E` |
| Secondary (teal) | `#12A5B0` |
| Accent (sky) | `#46C2E0` |
| Brand accent | `#1B9AAA` |
| Soft accent (ice) | `#E2F3F7` |
| Background | Blue-white `#F4F9FC` |
| Soft background | `#E8F2F8` |
| Text / muted | `#1C3A4A` / `#5E7480` |
| Rating stars | Amber `#E0912B` |

Font: **Poppins** (Google Fonts). Icons: **Bootstrap Icons**. Framework: **Bootstrap 5.3**.

The site uses a **clean clinical dentistry** identity: bright blue-white surfaces, medical blue and
teal accents, crisp borders, tighter 14px card radius and minimal shadows for a trustworthy,
professional healthcare feel.

---

## 🚀 How to Run

1. Copy the whole folder to your computer.
2. Double-click **`index.html`**, **or** serve it locally:
   ```
   python -m http.server 8000
   # then open http://localhost:8000
   ```
3. An internet connection is needed for the CDNs (Bootstrap, jQuery, fonts) and photos.

---

## 🖼️ Image Credits

Photography and product photos are sourced from free / Creative-Commons collections
(StockSnap.io, Openverse, Wikimedia Commons and Flickr CC) for educational project use.
Most product photos are CC0 / public domain; two are used under Creative Commons
(“Panasonic electric toothbrush” by Mk2010, CC BY-SA 4.0; “Tepe Interdental Brush” by
Brett Jordan, CC BY 2.0). The logo is an original SVG created for this project.

---

## 🧪 Quick Test Checklist (for viva)

1. Open every page from the navbar → no broken links, active item highlights.
2. Resize the browser → hamburger menu works on tablet/mobile.
3. Home hero → video plays automatically (mute, loop) and text stays readable; pause/reduced-motion still shows the poster.
4. Products → search “kids”, filter “Electrical”, sort by price, click **Rate Product** → pick 4 stars → toast appears.
5. Doctors → filter by specialty → grid and “Showing X of 6” counter update.
6. Kids Dental → play **Brush the Teeth** (timer/score/win message) and **Healthy Food Matcher** (score updates).
7. Queries → submit an empty form → errors shown; type a valid email → success banner + toast.
8. Bottom ticker → date/time update live; allow location → city appears; deny → “Location unavailable”.
9. Top-right visitor counter → increments on a new session.
10. Gallery → hover zoom + click lightbox (arrow keys / Esc work).
11. Check every page at 390px width → no horizontal scrolling.
12. Navbar dropdowns (Education / Explore) open on click and close on Esc.
13. Education ▾ → Symptom Checker → submit empty → three inline messages; pick
    “A tooth” + “Throbbing or constant pain” + “More than two weeks” + “Fever with the pain”
    → **Urgent** result with causes and advice; **Reset** clears everything.
14. Chatbot (bottom-right on every page) → click the headset button → greeting appears; try
    “Opening hours” chip and type “tooth pain” → both reply with links; press **Esc** closes and
    reopening keeps the history; it also fits on mobile (no horizontal scroll).
15. PDFs → open **Professional Education** / **Research** cards and the **Patient Education →
    Downloadable Guides** section → click any **Open PDF** link → the document opens in a new tab;
    all 27 files load and are valid.

---

© 2026 Belleville Dental. All Rights Reserved.
