# 🦷 LUXURY DENTAL WEBSITE — MASTER DESIGN PROMPT
### For Pennington Dental Care · Pennington, NJ
> Copy this entire file and paste it into Claude (claude.ai → New Chat → Artifact mode). Claude will produce a single, production-ready, luxury-styled, mobile-responsive HTML website.

---

## 🎯 PROMPT TO PASTE INTO CLAUDE

Build me a **single-file, production-grade, luxury-tier HTML website** for **Pennington Dental Care**, a high-end family & cosmetic dentistry in Pennington, NJ. The output must be ONE complete `.html` file containing all HTML, CSS, and JavaScript inline — no external frameworks except Google Fonts and Font Awesome (CDN). It must look like a **$25,000 boutique medical website** — refined, calm, premium, trustworthy — not a generic dental template.

### 🎨 DESIGN DIRECTION — "MODERN MEDICAL LUXURY"
Think **Aesop × Mayo Clinic × Apple**. Editorial whitespace, confident navy-and-cream palette, surgical typographic precision, glass-morphism CTAs, and subtle cinematic motion. NOT corporate. NOT cartoonish. NOT Bootstrap-default.

- **Mood**: Calm, clinical, expensive, reassuring
- **Density**: Generous whitespace, but no empty boredom — every section earns its space
- **Energy**: Slow, confident, intentional motion (no bouncy, no flashy)
- **Anti-patterns to AVOID**: purple gradients, dental-cliché tooth icons everywhere, stock-photo overload, rounded-rectangle everywhere, comic sans warmth

---

## 🎨 BRAND TOKENS (use these EXACTLY as CSS variables)

```css
:root {
  /* Core palette */
  --navy-deep: #0A3B6A;        /* primary — headings, nav, footer */
  --navy-ink:  #062845;        /* deepest accent for headlines */
  --blue-accent: #007BFF;      /* CTAs, links, highlights */
  --blue-soft: #E7F1FF;        /* soft section backgrounds */
  --cream: #FAF7F2;            /* warm luxury alt-background */
  --bg: #FFFFFF;               /* primary background — PURE WHITE */
  --ink: #0A3B6A;              /* body text dark */
  --muted: #5B6B7E;            /* secondary text */
  --line: #E5EAF0;             /* hairline dividers */
  --gold: #C9A961;             /* luxury accent — use sparingly for awards/badges */

  /* Typography */
  --font-display: 'Cormorant Garamond', 'Playfair Display', serif;  /* elegant serif for H1/H2 */
  --font-sans:    'Inter Tight', 'Manrope', sans-serif;             /* clean body */
  --font-mono:    'JetBrains Mono', monospace;                      /* small labels, numbers */

  /* Spacing rhythm — 8pt grid */
  --s-1: 4px; --s-2: 8px; --s-3: 16px; --s-4: 24px;
  --s-5: 40px; --s-6: 64px; --s-7: 96px; --s-8: 144px;

  /* Radius */
  --r-sm: 6px; --r-md: 14px; --r-lg: 28px; --r-pill: 999px;

  /* Shadows — soft, layered, never harsh */
  --shadow-sm: 0 1px 2px rgba(10,59,106,.04), 0 2px 8px rgba(10,59,106,.04);
  --shadow-md: 0 4px 16px rgba(10,59,106,.08), 0 12px 40px rgba(10,59,106,.06);
  --shadow-lg: 0 20px 60px rgba(10,59,106,.12);
}
```

**Background rule**: Page background is `#FFFFFF`. Alternate sections may use `--cream` or `--blue-soft` to create gentle rhythm. NEVER use full navy as section background except in the footer.

---

## 📐 LAYOUT & STRUCTURE (in this exact order)

### 1. Sticky Glass Navigation
- Translucent white bar with `backdrop-filter: blur(20px)` and 90% opacity, hairline bottom border
- **Left**: Logo (image URL below) — 52px tall
- **Center**: Home · Meet the Doctor · Services · Specials · Location · Contact
- **Right**: Phone pill `📞 609-818-0300` (outlined navy) + **"Book Appointment"** button (solid `--blue-accent`, pill radius, gentle shadow on hover lift -2px)
- Top thin announcement strip (navy bg, white text, 13px): `2425 Pennington Rd #101, Pennington, NJ 08534  •  We do not accept Medicaid`
- Mobile: hamburger that slides in a full-height drawer from the right with staggered link reveal

### 2. HERO — "The Editorial Statement"
- Two-column split on desktop, stacked on mobile
- **Left column (55%)**:
  - Small uppercase kicker in `--gold`, letter-spacing 0.3em: `EST. 2012 · PENNINGTON, NJ`
  - Massive serif headline (clamp 48px → 88px, `--font-display`, italic for one word):
    > `Crafted smiles, *quietly* extraordinary.`
  - Sub-headline (18px, `--muted`, 60ch max-width): `Advanced family & cosmetic dentistry led by Dr. Sri Angara. Personalized care, calm rooms, technology you can trust.`
  - Two CTAs side-by-side: Primary `Book Appointment →` (solid blue), Secondary `Call 609-818-0300` (ghost, navy outline)
  - Below CTAs: tiny trust row with 5 mini-avatars + `★★★★★ 5.0 from 100+ Google reviews`
- **Right column (45%)**:
  - A tall portrait image of Dr. Angara (use URL below) inside a rounded-rectangle frame with a **gold hairline border** offset by 12px (creates "framed portrait" effect)
  - Floating glass-card overlapping the image bottom-left showing: `New Patient Special · $99 · Exam + X-Rays + Cleaning + Fluoride` with a small `Book →` link
- **Background**: subtle radial gradient from `--blue-soft` at top-right to white. Add a barely-visible SVG noise texture overlay (opacity 0.03) for film-grain depth

### 3. Trust Bar (thin, white, centered)
Logos of insurances we accept — grayscale at 60% opacity, hover → full color. Show: UnitedHealthcare, Cigna, Blue Cross Blue Shield, Delta Dental, Aetna, MetLife, Guardian, Principal. Heading above: small caps `IN-NETWORK WITH MAJOR CARRIERS`.

### 4. SERVICES — "The Three Pillars" (hero services)
Three large cards side-by-side, each 1:1.3 aspect, image-top with overlay gradient, text-bottom:
1. **Family Dentistry** — `pexels-shvetsa-3845682.jpg`
2. **Cosmetic Treatments** — `pexels-karolina-grabowska-6627278.jpg`
3. **Emergency Same-Day Care** — `pexels-gustavo-fring-4971505.jpg`

Each card: small icon (Font Awesome), service name in `--font-display` 28px, two-line description, `Learn more →` link. On hover: image zooms 1.05x over 600ms ease-out, gradient deepens, card lifts -4px.

### 5. FULL SERVICE GRID — "Eight Specialties"
Below the three pillars, an 8-item grid (4 cols desktop, 2 cols tablet, 1 col mobile) — each item is a minimal card with just a thin icon (line-art) + service name + 1 line + arrow. Items: Orthodontic Services · Oral Surgery · Periodontic Treatment · Pediatric Dentistry · Restorative Services · Endodontics · Cosmetic Dentistry · Implant Dentistry. Hairline borders, no shadows — pure editorial.

### 6. IMPLANT FEATURE — "The Signature Offering"
Full-width section, cream background. Two columns:
- **Left (40%)**: Photo of Dr. Angara (use `Ellipse 1.png` URL below) inside a circular mask, gold ring around it
- **Right (60%)**:
  - Serif headline: `Restore your smile with dental implants`
  - Body: 2 short paragraphs explaining process, comfort, longevity
  - **Price card** (glass card, slight tilt -1deg): `Implant Special · $3,500 · Limited Time` with `Reserve Consult →` button

### 7. INVISALIGN BEFORE/AFTER
Interactive before/after slider (draggable handle) using the two images:
- BEFORE: `image%207.jpg`
- AFTER: `image%206.jpg`
- Caption above: `Transform your smile with Invisalign — virtually invisible, remarkably confident.`
- CTA below: `Schedule Invisalign Consult →`

### 8. MEET THE TEAM — "Eight portraits, eight stories"
Section title with elegant divider rule. Display all 8 team members in a grid (4×2 desktop, 2×4 tablet, 1 col mobile). Each card:
- Square portrait image (rounded-corner `--r-md`)
- Name in serif 22px
- Role in mono uppercase 11px letter-spacing 0.2em
- 2-line bio
- Tiny `Read Bio →` link

Team list (with EXACT image URLs in asset section):
1. **Dr. Sri Angara, DDS** — Owner & Lead Dentist (since 2012)
2. **Dr. Nawal A. Shaikh** — Associate Dentist, Endodontics specialty
3. **Michele** — Office Manager (since 2014)
4. **Jessica** — Hygienist (since 2024)
5. **Chaniece** — Certified Dental Assistant (since 2023)
6. **Ingrid** — Dental Assistant (since 2020)
7. **Shanta King** — Patient Care Coordinator
8. **Subha** — Receptionist & Billing Coordinator (since 2023)

### 9. SPECIALS BANNER (two-card luxury offer block)
Side-by-side cards on cream background:
- **Card 1 — New Patient Special $99**: Comprehensive Exam · X-Rays · Basic Cleaning · Fluoride. Expires 05/23/2026. Small print: New patients only · Cannot combine with insurance.
- **Card 2 — Zoom Whitening $550**: Limited-time prom & graduation offer.
Each card has subtle gold border, soft shadow, `Book →` CTA.

### 10. WHY CHOOSE US — "Three Promises"
Three columns, no images, just elegant typography:
1. **Skilled & Caring Team** — short manifesto paragraph
2. **Advanced Technology** — short manifesto paragraph
3. **Safety & Comfort First** — short manifesto paragraph
Each column has a thin numbered marker (01 / 02 / 03 in mono gold), serif heading, sans body.

### 11. TECHNOLOGY SHOWCASE
Four mini-cards in a row with line-icon + tech name + 1 sentence:
- **CBCT 3D Imaging** — Detailed views for implant precision
- **iTero Digital Scanner** — Laser-accurate scans, no goop
- **BIOLASE Laser** — Suture-free, faster healing
- **Intraoral Camera** — See what we see, in HD

### 12. REVIEWS — "Voices from Our Chairs"
Headline + 5-star Google badge. Horizontal scrolling marquee (auto-scroll slow, pause on hover) of 5 review cards. Each card: Google "G" icon, 5 yellow stars, quote in serif italic 18px, avatar + name below. Reviews:

> "Love the strong women who work here! Highly recommend coming here for your routine checkups and dental care." — **Gayathri Pratha**

> "The doctors and hygienists are very professional and attentive. I definitely recommend this dental practice!" — **Andrew Popow**

> "I had an excellent experience with this team of dentists! They are professional, friendly, and quick. Highly recommend!" — **Erin**

> "ALL the ladies that worked here were fabulous! Friendly, knowledgeable, personable. I'm glad I found this dental office!" — **Meaghan Bull**

> "Very knowledgeable and made it a comfortable experience. They suggested treatments others missed for healthy teeth." — **Emily Shaw**

### 13. OFFICE GALLERY — Mosaic
A masonry-style grid (CSS columns: 3 / 2 / 1) of the 7 office WhatsApp photos. Hover → slight zoom + caption overlay fades in. Lightbox on click (vanilla JS).

### 14. LOCATION & HOURS
Two-column split:
- **Left**: Embedded Google Map (iframe) of `2425 Pennington Rd #101, Pennington, NJ 08534`. Rounded corners, slight shadow.
- **Right**: 
  - Address block (serif heading + sans address)
  - Office hours table (clean rows, hairline dividers): Mon–Fri 9:00 AM – 5:00 PM · Sat 9:00 AM – 2:00 PM · Sun Closed
  - Phone: `609-818-0300` as large click-to-call link
  - "Get Directions →" button

### 15. FINAL CTA
Full-width section, navy gradient (deep navy → ink) with grain overlay:
- Serif headline white: `Your smile is waiting. So are we.`
- Sub: `Same-week appointments available · Most insurance accepted`
- White pill button: `Book Your Visit →`
- Below: tiny mono text `Call us · 609-818-0300`

### 16. FOOTER
Dark navy `--navy-ink` background, 4 columns:
1. Logo + tagline + Google review badge
2. Services (8 links)
3. Practice (Meet Doctor · Team · Tech · Specials · Reviews)
4. Visit (Address · Hours · Phone · Directions link)
Bottom strip: `© 2026 Pennington Dental Care · We do not accept Medicaid · Sitemap · Privacy`

---

## ✨ MOTION & INTERACTION SPECS

Use **Intersection Observer** for scroll reveals. Every major section animates in once:
```css
.reveal { opacity: 0; transform: translateY(24px); transition: all 900ms cubic-bezier(.2,.7,.2,1); }
.reveal.in { opacity: 1; transform: none; }
```

Specific motion moments:
- **Hero load**: serif headline letters fade-in word-by-word with 80ms stagger, image fades + scales from 0.96 over 1200ms
- **Number counters**: years-in-practice, patients-served, 5-star reviews — count up when scrolled into view
- **Cards**: hover lifts -4px, shadow expands, image inside zooms 1.05x — all 500ms ease
- **Buttons**: solid → on hover, slight scale 1.02, shadow grows. Add a subtle "shine sweep" (white gradient that crosses the button) every 8 seconds on the primary hero CTA
- **Marquee** for reviews: CSS-only infinite scroll, pause on hover
- **Before/After slider**: draggable, smooth, no jitter
- **Sticky nav**: shrinks 12px after 100px scroll, shadow appears
- **Decorative SVG**: A thin gold underline-swoosh draws itself under the hero word "extraordinary" using `stroke-dasharray` animation on load

**Performance**: All animations CSS-first. JS only for scroll observer, marquee pause, before/after slider, lightbox, and mobile menu.

---

## 📱 MOBILE RESPONSIVENESS (CRITICAL)

Mobile-first breakpoints:
- **Default (mobile)**: 0–639px — single column everywhere, hero stacks (text first, image second), hamburger menu, hero headline drops to clamp(36px, 9vw, 48px)
- **Tablet**: 640–1023px — 2-col grids
- **Desktop**: 1024px+ — full layouts as described

Mobile-specific rules:
- Touch targets minimum 44×44px
- No hover-dependent interactions — all hover effects must have tap equivalents
- Sticky bottom bar on mobile: phone icon + "Book" button (always visible, glass background)
- Hamburger drawer: full-height, right-slide, with large 24px nav links and quick-call button at bottom

---

## 🖼️ ASSET LIBRARY (use these EXACT URLs)

### Logo
```
https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67e1b4732d5d1dc446142091_logo%20(1).png
```

### Hero & Section Images
- Hero feature image: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67dc66366111f24d9c9ea901_pexels-fr3nks-287237.jpeg`
- Family Dentistry card: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67db1f6d8cb17c92b45bd011_pexels-shvetsa-3845682.jpg`
- Cosmetic Treatments card: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67db1f6bdde7646925262eef_pexels-karolina-grabowska-6627278.jpg`
- Emergency card: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67e18997ef764225a77354d5_pexels-gustavo-fring-4971505.jpg`
- Why Choose Us 1: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67db5e7bf97ca274801a6795_caroline-lm-QA9fRIi6sFw-unsplash.jpg`
- Why Choose Us 2: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67db5ee604a5434870bd8b01_quang-tri-nguyen-VckdJzo7ig0-unsplash.jpeg`
- Why Choose Us 3: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67e18e5a21ebc3692a583a41_dentist-8729624_1280.jpg`

### Implant Section
- Implant feature 1: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/68bb4fa8f0e84300ccad3a58_edsew31.jpg`
- Implant feature 2: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/68bb4f8f7737bea94860c70e_Frame%2037.jpg`
- Dr. Angara circular portrait: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/68bb50b19004e24d59090633_Ellipse%201.png`

### Invisalign Before / After
- BEFORE: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/68a78d3f910846515aafcf56_image%207.jpg`
- AFTER: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/68a78d53ad0aa6ca09adf032_image%206.jpg`

### Team Portraits (in display order)
1. Dr. Sri Angara: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f40064acc5b46088427565_Photo1.jpeg`
2. Dr. Nawal A. Shaikh: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f4051af0effdff19132881_Photo2.jpeg`
3. Michele: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f407ec0d566cba7b54e7e1_photo3Michele.jpeg`
4. Jessica: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f407ec73167645036d6b5f_photo4Jessica.jpeg`
5. Chaniece: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f407ec0bede911e7a5b329_photo5Chaniece.jpeg`
6. Ingrid: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f407ec62e44f8fdfd4b9ba_photo6Ingrid.jpeg`
7. Shanta King: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f407ecb3405a2dcf31df6e_photo7ShantaKing.jpeg`
8. Subha: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f407ecd3f9a1a4d919ebf8_photo8Subha.jpeg`

### Review Avatars
- Gayathri Pratha: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67da078785455d7a32f211b2_unnamed.avif`
- Andrew Popow: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67db1c935e9f03195ec443e3_Andre%20popow.avif`
- Erin: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67db1d217539735bc1e865d8_Erin.avif`
- Meaghan Bull: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67db1d7ab60eb59a842b8e49_Meghan.avif`
- Emily Shaw: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67db1dbd717e072d95276fd8_emily.avif`
- Google "G" icon: `https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67d9ddbfff9b76b42ca473a9_icon-google.svg`

### Office Gallery (use ALL 7)
```
https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f407edfea8e01930c1576f_WhatsApp%20Image%202025-04-04%20at%2017.15.45.jpeg
https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f407edc6b324ca8b5570c7_WhatsApp%20Image%202025-04-04%20at%2017.16.54.jpeg
https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f407ed8bf0e1f85325c5a7_WhatsApp%20Image%202025-04-04%20at%2017.15.44.jpeg
https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f407edc9d9ca3f35aa7dca_WhatsApp%20Image%202025-04-04%20at%2017.15.45%20(2).jpeg
https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f407ed5add6dc87e3c75ac_WhatsApp%20Image%202025-04-04%20at%2017.16.54%20(1).jpeg
https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f407ed48b51f01111fdc61_WhatsApp%20Image%202025-04-04%20at%2017.15.44%20(1).jpeg
https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67f407ed0bede911e7a5b3c1_WhatsApp%20Image%202025-04-04%20at%2017.15.45%20(1).jpeg
```

### Insurance Logos
```
UnitedHealthcare: https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67e1a8b81cb5ca42c7014eb1_unitedhealthcare-vector-logo-2021.svg
Cigna: https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67e1a8b82b3acd0be8b40bd4_cigna-3.svg
Blue Cross Blue Shield: https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67e1a8b8f98cfdd12ec184e0_blue-cross-blue-shield-vector-logo.svg
Delta Dental: https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67e1a8d7b66604fbd32fbd69_5f24309651b0ae9b642bcc60_5ed7c73050f6d64f894d0968_delta-dental.png
Aetna: https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67e1a8d7c4279fcf8820c40a_5f24309651b0aeccd62bcc82_aetna.png
MetLife: https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67e1a8d71d14690b746aac21_5f24309651b0aeb53d2bccae_metlife.png
Guardian: https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67e1a8d71775062d35762e0f_5f24309651b0aebe9e2bccaf_guardian.png
Principal: https://cdn.prod.website-files.com/67d9ddbfff9b76b42ca47388/67e1a8d71775062d35762e12_5f24309651b0ae6f992bccb0_principal.png
```

---

## 🔗 LINKS & CTA BEHAVIOR (every link wired)

- ALL "Book Appointment" buttons → `href="#book"` (anchor to a booking modal/section) OR `https://www.visitpenningtondentalcare.com/#book`
- Phone number anywhere → `tel:6098180300`
- Address / "Get Directions" → `https://www.google.com/maps/dir//2425+Pennington+Rd+%23101,+Pennington,+NJ+08534`
- Office video → `https://www.youtube.com/watch?v=UvRsk3a3dp4` (open in lightbox)
- Service "Learn more" → `#service-{slug}` anchors
- Footer service links → same `#service-{slug}` anchors
- Logo → `#top`

---

## 📋 CONTENT BLOCK — exact copy to use

### Hero
> EST. 2012 · PENNINGTON, NJ
> # Crafted smiles, *quietly* extraordinary.
> Advanced family & cosmetic dentistry led by Dr. Sri Angara. Personalized care, calm rooms, technology you can trust.

### Family Dentistry blurb
> Gentle care for every age. From your child's first visit to senior dental needs — we build relationships that last decades, not just appointments.

### Cosmetic blurb
> Subtle, natural, transformative. Whitening, veneers, bonding, and full smile design tailored to your face — never overdone.

### Emergency blurb
> Broken tooth at 4 PM? We hold appointments daily for the unexpected. Call us, and you'll be seen — usually the same day.

### Why Choose Us — manifesto paragraphs
> **01. Skilled & Caring Team** — We don't just treat teeth, we treat people. Every team member combines advanced training with genuine compassion, ensuring you feel valued, heard, and comfortable throughout your dental journey.
>
> **02. Advanced Technology** — 3D imaging, intraoral cameras, digital scanning, and dental lasers. We invest in tools that diagnose more precisely, treat more gently, and finish faster — because your time and comfort matter.
>
> **03. Safety & Comfort First** — Sterilization protocols that exceed industry standards. Calm, modern operatories designed around the patient. Scheduling that respects your day. Peace of mind, built in.

### Final CTA
> ## Your smile is waiting. So are we.
> Same-week appointments available · Most insurance accepted

---

## ✅ DELIVERY REQUIREMENTS — checklist Claude must satisfy

- [ ] **One single `.html` file**, fully self-contained (HTML + CSS in `<style>` + JS in `<script>`)
- [ ] Google Fonts: Cormorant Garamond + Inter Tight + JetBrains Mono (loaded via `<link>` preconnect + display=swap)
- [ ] Font Awesome 6 via CDN for icons
- [ ] **Background pure white** with cream/blue-soft accent sections
- [ ] All 30+ image URLs above are correctly placed where specified
- [ ] All phone numbers are `tel:6098180300` clickable
- [ ] Sticky glass navigation works on scroll
- [ ] Hero, Services pillars, Implants, Invisalign before/after, Team grid, Specials, Why Choose, Tech, Reviews marquee, Gallery, Map, Final CTA, Footer — all present
- [ ] Scroll reveal animations on every section
- [ ] Mobile responsive at 375px, 768px, 1280px, 1920px — TEST these breakpoints
- [ ] Sticky mobile bottom bar (Call + Book)
- [ ] Hamburger menu with smooth slide-in drawer
- [ ] Before/After image slider is draggable and works on touch
- [ ] Office gallery has lightbox on click
- [ ] Reviews marquee auto-scrolls + pauses on hover
- [ ] No `localStorage` / `sessionStorage`
- [ ] No `<form>` tags (use div + onclick for any form-like elements)
- [ ] Lighthouse-friendly: lazy-load all non-hero images with `loading="lazy"`
- [ ] Semantic HTML5: `<header>`, `<main>`, `<section>`, `<article>`, `<footer>`, proper `<h1>`–`<h3>` hierarchy
- [ ] All images have descriptive `alt` text
- [ ] Aria labels on icon-only buttons
- [ ] Smooth-scroll behavior on anchor links: `html { scroll-behavior: smooth; }`
- [ ] Scrollbar styled to match brand (thin, navy thumb)

---

## 🚫 ABSOLUTE DO-NOTS

- ❌ NO Bootstrap, Tailwind, or any external CSS framework
- ❌ NO purple gradients or generic AI-template aesthetics
- ❌ NO stock-dental cliches (oversized tooth icons, "perfect smile" cursive)
- ❌ NO Lorem Ipsum — use the exact copy from this brief
- ❌ NO placeholder images — every image URL above is REAL and must be used
- ❌ NO emoji-heavy decoration
- ❌ NO bouncy/playful animations — keep motion confident and slow
- ❌ NO fake testimonial faces — use the avatar URLs above
- ❌ NO `<form>` tags
- ❌ NO `localStorage`

---

## 🎬 FINAL INSTRUCTION TO CLAUDE

Produce the full single-file HTML now. Begin with `<!DOCTYPE html>` and end with `</html>`. Do not summarize, do not break it into parts, do not ask follow-up questions — just deliver the complete, polished, luxury website. Every section must be present, every image URL must be in place, every animation must be wired, and the result must look like it cost a fortune.

When done, the page should feel like walking into a Manhattan boutique dental clinic: hushed, warm-white, exquisitely lit, and absolutely confidence-inspiring.

---

### 📝 HOW TO USE THIS PROMPT

1. Open **Claude.ai** (claude.ai/new) and create a new chat
2. Make sure **Artifacts** is enabled (auto-enabled by default)
3. Copy this **entire** markdown file
4. Paste it as a single message
5. Claude will produce one `.html` file inside an artifact — preview it, download it, and host it
6. If anything's missing, simply reply: *"Add the [section name], using the same luxury style. Re-output the full file."*

— End of Master Prompt —
