<div align="center">

# ⚡ Aman Aaryan — Developer Portfolio

### `amanaaryan672@gmail.com` · [LinkedIn](https://www.linkedin.com/in/amanaaryan) · [GitHub](https://github.com/thestethoguy)

[![Live Site](https://img.shields.io/badge/🌐_Live_Site-00d4ff?style=for-the-badge&logoColor=black)](https://thestethoguy.github.io/portfolio/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Google Fonts](https://img.shields.io/badge/Google_Fonts-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://fonts.google.com/)
[![GitHub Pages](https://img.shields.io/badge/Deployed_on-GitHub_Pages-181717?style=for-the-badge&logo=github&logoColor=white)](https://pages.github.com/)

<br/>

> *A zero-dependency, production-grade personal portfolio built with vanilla HTML, CSS, and JavaScript —*
> *featuring scroll-reveal animations, a live typing effect, biometric-inspired dark UI, and real-time*
> *certificate verification links. No frameworks. No build tools. Just clean, fast, deployable code.*

<br/>

```
╔═══════════════════════════════════════════════════════════╗
║   aman_aaryan  //  portfolio.v1  //  zero dependencies   ║
║   stack: html · css · vanilla js  //  deploy: gh-pages   ║
╚═══════════════════════════════════════════════════════════╝
```

</div>

---

## 📋 Table of Contents

- [🖥️ Live Preview](#️-live-preview)
- [✨ Features](#-features)
- [🏗️ Architecture & Page Flow](#️-architecture--page-flow)
- [🎨 Design System](#-design-system)
- [📐 Layout Architecture](#-layout-architecture)
- [🔧 Technical Deep-Dive](#-technical-deep-dive)
- [📁 Project Structure](#-project-structure)
- [🚀 Sections Breakdown](#-sections-breakdown)
- [⚙️ How to Run Locally](#️-how-to-run-locally)
- [☁️ Deployment Guide](#️-deployment-guide)
- [📊 Performance & Metrics](#-performance--metrics)
- [🔮 Roadmap](#-roadmap)
- [📜 License](#-license)

---

## 🖥️ Live Preview

```
 ┌─────────────────────────────────────────────────────────────┐
 │  🌐  https://YOUR_GITHUB_PAGES_URL                         │
 │                                                             │
 │  ┌─── NAV ──────────────────────────────────────────────┐  │
 │  │  aman_aaryan    About  Skills  Projects  Contact     │  │
 │  └──────────────────────────────────────────────────────┘  │
 │                                                             │
 │  // Hello, World! — Welcome to my portfolio                 │
 │                                                             │
 │  ██████╗  [name]       ╭──────────────╮                    │
 │  ██╔══██╗  Aman        │  🖼️  Photo   │                    │
 │  ███████║  Aaryan      │   (circular) │                    │
 │  ╚══════╝              ╰──────────────╯                    │
 │                                                             │
 │  Full-Stack Developer|█                                     │
 │                                                             │
 │  [ View Projects ↓ ]  [ Get In Touch → ]                   │
 │                                                             │
 │  ──── Scroll to explore                                     │
 └─────────────────────────────────────────────────────────────┘
```

---

## ✨ Features

| Feature | Implementation | Details |
|---|---|---|
| 🌑 **Dark Cyber Theme** | Pure CSS Variables | `#07070e` base, `#00d4ff` cyan accent |
| ⌨️ **Typing Effect** | Vanilla JS | Cycles through 4 roles, 80ms type / 40ms erase |
| 🎞️ **Scroll Reveal** | `IntersectionObserver` API | Threshold 0.12, staggered `fadeUp` animation |
| 📐 **CSS Grid Background** | CSS `background-image` | Dual linear-gradient at 60×60px grid |
| 🖼️ **Hero Photo** | CSS `border-radius: 50%` | Circular, cyan-bordered, glow shadow |
| 🏅 **Live Cert Links** | `<a target="_blank">` | Direct Credly + Coursera verify URLs |
| 🔗 **Clickable Stat Cards** | Anchor `<a>` tags | Scroll-link to Projects, Certifications, etc. |
| 🔝 **Glassmorphism Nav** | `backdrop-filter: blur(16px)` | Fixed, 85% opacity dark background |
| 📱 **Responsive Design** | CSS Media Queries | Breakpoint at `768px` |
| ♿ **Semantic HTML** | `<nav>`, `<section>`, `<footer>` | Accessible, crawlable structure |
| 🚀 **Zero Dependencies** | No npm, no build step | Open `index.html` → works |
| ⚡ **Instant Load** | No JS frameworks | No bundle, no hydration, no waiting |

---

## 🏗️ Architecture & Page Flow

### 📌 Overall Document Structure

```
index.html
│
├── <head>
│   ├── Google Fonts (Syne · JetBrains Mono · DM Sans)
│   └── <style> — 400+ lines of CSS
│
└── <body>
    │
    ├── <nav>  ─────────────── Fixed glassmorphism navbar
    │   ├── Logo: aman_aaryan
    │   └── Links: About · Skills · Projects · Education · Certifications · Contact
    │
    ├── <section id="hero">  ── Full-viewport hero
    │   ├── .hero-container (CSS Grid: 1.2fr 0.8fr)
    │   │   ├── .hero-text-content
    │   │   │   ├── Eyebrow label
    │   │   │   ├── <h1> Name
    │   │   │   ├── Typing effect span
    │   │   │   ├── Description paragraph
    │   │   │   └── CTA Buttons
    │   │   └── .hero-image-wrapper
    │   │       └── <img> Circular photo
    │   └── .scroll-hint
    │
    ├── <section id="about">  ── About + Stats
    │   └── CSS Grid (1fr 1fr)
    │       ├── Bio text (3 paragraphs)
    │       └── 4× Stat cards (clickable anchors)
    │
    ├── <section id="skills">  ─ Skills
    │   └── auto-fit grid (minmax 260px)
    │       └── 6× Skill category cards + tags
    │
    ├── <section id="projects">  Projects
    │   └── 4× Project cards (grid: 1fr auto)
    │       ├── Project info (num, name, desc, tech tags)
    │       └── Links (GitHub ↗ · Live ↗)
    │
    ├── <section id="education">  Education
    │   └── 3× Edu cards (flex: space-between)
    │
    ├── <section id="certifications">  Certifications
    │   └── auto-fit grid (minmax 280px)
    │       └── 5× Cert cards + "View Certificate ↗" button
    │
    ├── <section id="contact">  Contact CTA
    │   └── Centered card with 4 contact links
    │
    ├── <footer>  Copyright
    │
    └── <script>
        ├── Typing effect engine
        ├── IntersectionObserver (scroll reveal)
        └── Blink cursor keyframe injection
```

---

### 🔄 JavaScript Engine Flow

```
Page Load
    │
    ▼
┌─────────────────────────────────┐
│       TYPING EFFECT ENGINE      │
│                                 │
│  roles[] = [                    │
│    'B.Tech IT Student @ KIIT',  │
│    'Full-Stack Developer',      │
│    'Machine Learning Engineer', │
│    'AWS Certified Cloud Grad'   │
│  ]                              │
│                                 │
│   ri=0, ci=0, del=false         │
│         │                       │
│    ┌────▼────┐                  │
│    │  del?   │                  │
│    └────┬────┘                  │
│   No    │    Yes                │
│    ▼    │     ▼                 │
│  type   │   erase               │
│  80ms   │   40ms                │
│    │    │     │                 │
│    └────┴─────┘                 │
│  ci === len? → pause 1800ms     │
│  ci === 0?   → next role        │
└─────────────────────────────────┘

    │
    ▼
┌──────────────────────────────────┐
│     SCROLL REVEAL ENGINE         │
│                                  │
│  IntersectionObserver            │
│  threshold: 0.12                 │
│                                  │
│  All .reveal elements:           │
│  opacity: 0                      │
│  transform: translateY(24px)     │
│       │                          │
│       │  element enters viewport │
│       ▼                          │
│  .reveal.visible:                │
│  opacity: 1                      │
│  transform: translateY(0)        │
│  transition: 0.6s ease           │
└──────────────────────────────────┘

    │
    ▼
┌──────────────────────────────────┐
│     BLINK CURSOR INJECTION       │
│                                  │
│  document.createElement('style') │
│  → @keyframes blink              │
│  → appended to <head>            │
└──────────────────────────────────┘
```

---

### 🎞️ Animation Timeline (On Page Load)

```
Timeline ──────────────────────────────────────────────────────▶
 0ms     200ms    400ms    600ms    800ms   1000ms   1400ms
  │        │        │        │        │        │        │
  │        ▼        │        │        │        │        │
  │   Eyebrow       │        │        │        │        │
  │   fadeUp        ▼        │        │        │        │
  │                Name      │        │        │        │
  │               fadeUp     ▼        │        │        │
  │                        Role       │        │        │
  │                        fadeUp     ▼        │        │
  │                                 Desc       │        │
  │                                 fadeUp     ▼        │
  │                                           Btns      │
  │                                           fadeUp    ▼
  │                                                  Scroll
  │                                                   hint
  │
  ▼ (continuous)
 Typing effect starts immediately, loops infinitely
```

---

## 🎨 Design System

### 🎨 Color Palette

```
 ╔══════════════════════════════════════════════════════════╗
 ║                   COLOUR PALETTE                        ║
 ╠══════════════════════════════════════════════════════════╣
 ║                                                         ║
 ║  ████  #07070e  --bg       Page background (near-black) ║
 ║  ████  #0d0d1a  --bg2      Card surfaces                ║
 ║  ████  #111127  --bg3      Elevated surfaces            ║
 ║  ████  #00d4ff  --cyan     Primary accent (electric)    ║
 ║  ████  #0099bb  --cyan2    Hover state for cyan         ║
 ║  ████  #f0f4ff  --white    Body text / headings         ║
 ║  ████  #6b7a99  --gray     Muted text / descriptions    ║
 ║  ░░░░  rgba(0,212,255,0.12)  --border  Subtle borders   ║
 ║                                                         ║
 ╚══════════════════════════════════════════════════════════╝
```

### 🔤 Typography System

```
 ┌────────────────────────────────────────────────────────┐
 │               TYPOGRAPHY HIERARCHY                     │
 ├────────────────────────────────────────────────────────┤
 │                                                        │
 │  SYNE (700–800 weight)  ──── Display / Headings        │
 │  ┌────────────────────────────────────────────────┐    │
 │  │  AMAN AARYAN  ← clamp(3.5rem, 8vw, 7rem)      │    │
 │  │  Who I Am     ← clamp(2rem, 4vw, 3rem)        │    │
 │  │  Project Name ← 1.4rem                        │    │
 │  └────────────────────────────────────────────────┘    │
 │                                                        │
 │  JETBRAINS MONO (300–500 weight)  ─ Code / Labels      │
 │  ┌────────────────────────────────────────────────┐    │
 │  │  // 01. About     ← section labels             │    │
 │  │  FULL-STACK DEV   ← skill tags, nav links      │    │
 │  │  March 2026       ← dates, metadata            │    │
 │  └────────────────────────────────────────────────┘    │
 │                                                        │
 │  DM SANS (300–500 weight)  ────── Body / Descriptions  │
 │  ┌────────────────────────────────────────────────┐    │
 │  │  I'm a Software Developer and ML Engineer...   │    │
 │  │  font-size: 16px, line-height: 1.7             │    │
 │  └────────────────────────────────────────────────┘    │
 └────────────────────────────────────────────────────────┘
```

---

## 📐 Layout Architecture

### 🖥️ Hero Section — CSS Grid (Two-Column)

```
┌─────────────────────────────────────────────────────────────┐
│   grid-template-columns: 1.2fr  │  0.8fr                    │
│                                 │                           │
│   .hero-text-content            │  .hero-image-wrapper      │
│   ─────────────────             │  ─────────────────────    │
│   // Hello, World! eyebrow      │                           │
│                                 │     ╭───────────╮         │
│   AMAN                          │    ╱             ╲        │
│   AARYAN   (7rem, weight 800)   │   │   aman.jpg   │        │
│                                 │   │  320×320px   │        │
│   Full-Stack Developer|         │    ╲             ╱        │
│                 (typing effect) │     ╰───────────╯         │
│                                 │   border: 3px cyan        │
│   Bio paragraph...              │   box-shadow: cyan glow   │
│                                 │                           │
│   [View Projects] [Contact]     │                           │
│                                 │                           │
│   ──── Scroll to explore        │                           │
└─────────────────────────────────┴───────────────────────────┘

Mobile (≤768px):  grid-template-columns: 1fr  (stacks vertically)
                  photo: 240×240px, centered below text
```

### 📦 Project Card Layout

```
┌──────────────────────────────────────────────────────┐  ◄── 2px cyan
│  grid-template-columns: 1fr                │  auto  │      gradient
│                                            │        │      on hover
│  .project-num   Project 01                 │        │
│  .project-name  Pratyahara — AI Wellness   │  [Git] │
│                                            │  [ ↗ ] │
│  .project-desc  Production full-stack...   │        │
│                 ...                        │  [Live] │
│                                            │  [ ↗ ] │
│  [React 18][FastAPI][MongoDB]...           │        │
└────────────────────────────────────────────┴────────┘
      ↑ hover: border cyan + translateY(-3px)
```

### 🏅 Certification Card Layout

```
┌─────────────────────────────────┐
│  .cert-issuer                   │  ← JetBrains Mono, 0.68rem, cyan
│  AMAZON WEB SERVICES            │
│                                 │
│  .cert-name                     │  ← DM Sans, 0.95rem, white
│  AWS Academy Graduate –         │
│  Cloud Foundations              │
│                                 │
│  .cert-date                     │  ← JetBrains Mono, 0.68rem, gray
│  April 2026                     │
│                                 │
│  [ View Certificate ↗ ]         │  ← Cyan button → Credly/Coursera URL
└─────────────────────────────────┘
      flex-direction: column
      gap: 0.35rem
      margin-top: auto on button (pushes to bottom)
```

---

## 🔧 Technical Deep-Dive

### 🌐 CSS Grid Background

```css
/* Creates the iconic cyan-tinted graph paper effect */
body::before {
  content: '';
  position: fixed;          /* Stays fixed during scroll */
  inset: 0;
  background-image:
    linear-gradient(rgba(0,212,255,0.03) 1px, transparent 1px),
    linear-gradient(90deg, rgba(0,212,255,0.03) 1px, transparent 1px);
  background-size: 60px 60px;  /* Grid cell size */
  pointer-events: none;
  z-index: 0;
}
```

### 🔍 Glassmorphism Navigation

```css
nav {
  position: fixed;
  background: rgba(7,7,14,0.85);    /* 85% opacity — content shows through */
  backdrop-filter: blur(16px);       /* Frosted glass effect */
  border-bottom: 1px solid rgba(0,212,255,0.12);
}
```

### 🎯 Project Card Top-Line Reveal

```css
.project-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 2px;
  background: linear-gradient(90deg, var(--cyan), transparent);
  opacity: 0;
  transition: opacity 0.2s;
}
.project-card:hover::before { opacity: 1; }
```

### 👁️ IntersectionObserver — Scroll Reveal

```javascript
const obs = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (e.isIntersecting) e.target.classList.add('visible');
  });
}, { threshold: 0.12 }); // Triggers when 12% of element is in viewport

document.querySelectorAll('.reveal').forEach(el => obs.observe(el));
```

```css
.reveal {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity 0.6s, transform 0.6s;
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
```

### ⌨️ Typing Effect — State Machine

```javascript
const roles = ['B.Tech IT Student @ KIIT', 'Full-Stack Developer', ...];
let ri = 0, ci = 0, del = false;

function type() {
  const cur = roles[ri];
  if (!del) {
    el.textContent = cur.slice(0, ++ci);
    if (ci === cur.length) { del = true; setTimeout(type, 1800); return; }
  } else {
    el.textContent = cur.slice(0, --ci);
    if (ci === 0) { del = false; ri = (ri + 1) % roles.length; }
  }
  setTimeout(type, del ? 40 : 80);  // Erase faster than type
}
```

---

## 📁 Project Structure

```
portfolio/
│
├── 📄 index.html          ← The entire portfolio (single file)
├── 🖼️  aman.jpg           ← Hero profile photo (same folder as index.html)
└── 📖 README.md           ← This file
```

> **Why a single file?**
> Zero build tooling required. No npm install, no webpack, no vite config.
> Drop `index.html` + `aman.jpg` on any static host and it works instantly.

---

## 🚀 Sections Breakdown

### `// 01. Hero`
- **Layout:** 2-column CSS Grid (`1.2fr 0.8fr`)
- **Typing effect** cycles: `B.Tech IT Student @ KIIT` → `Full-Stack Developer` → `Machine Learning Engineer` → `AWS Certified Cloud Graduate`
- Profile photo: `320px` circle, `3px` cyan border, `box-shadow` cyan glow
- Two CTAs: `View Projects ↓` (primary cyan) + `Get In Touch →` (outline)
- Scroll hint animates in at `1400ms` delay

### `// 02. About`
- **Layout:** 2-column grid — bio text left, 4 stat cards right
- Stat cards are **clickable anchors** that deep-link to their sections:
  - `4+ Projects` → `#projects`
  - `5 Certifications` → `#certifications`
  - `6K+ Hackathon Participants` → `#zomathon-project`
  - `2.26M Loan Records` → `#p2p-project`

### `// 03. Skills`
- **6 categories:** Languages · Web Dev · ML & Data Science · Databases · Cloud & Tools · Engineering
- `auto-fit` grid with `minmax(260px, 1fr)` — self-adapting columns
- 30+ individual skill tags with cyan-tinted styling

### `// 04. Projects`
- **4 projects** with full descriptions, tech stacks, and live/GitHub links
- Projects 02 and 03 have named IDs for deep-linking from stat cards
- Top-border gradient reveal on hover via CSS `::before` pseudo-element

### `// 05. Education`
- 3 institutions with degree, school, year range, and grade
- Right-aligned metadata, year in cyan

### `// 06. Certifications`
- 5 cards with **real, live certificate URLs:**

| Certificate | Issuer | Verify Link |
|---|---|---|
| AWS Academy Graduate – Cloud Foundations | Amazon Web Services | [Credly Badge](https://www.credly.com/badges/4c82f8d8-f506-442a-b7be-bd856bebd2dd/public_url) |
| Agentic AI with LangChain and LangGraph | IBM – Coursera | [Coursera Verify](https://www.coursera.org/account/accomplishments/verify/BIW7P7RYBVQ1) |
| Generative AI for Digital Marketing | IBM – Coursera | [Coursera Specialization](https://www.coursera.org/account/accomplishments/specialization/VHV0QN6LGC8F) |
| Hello, Python! | Google – Coursera | [Coursera Verify](https://www.coursera.org/account/accomplishments/verify/NPO2E6UEGPUX) |
| Health Systems Development Specialization | Imperial College London | [Coursera Specialization](https://www.coursera.org/account/accomplishments/specialization/3E3AHKTWPBFB) |

### `// 07. Contact`
- Email · Phone · GitHub · LinkedIn — all in bordered pill buttons
- Radial cyan gradient glow decoration (top-right corner of card)

---

## 📊 Performance & Metrics

| Metric | Value | Notes |
|---|---|---|
| 📦 **Total Files** | 2 | `index.html` + `aman.jpg` |
| 🌐 **External Requests** | 1 | Google Fonts CDN only |
| ⚡ **JS Framework** | None | Zero overhead, instant parse |
| 🔨 **Build Step Required** | None | No npm, no webpack, no Vite |
| 🎨 **CSS Custom Properties** | 8 | Easy to retheme in one place |
| 📐 **Responsive Breakpoint** | 768px | Single mobile breakpoint |
| 🎞️ **Animation Types** | 3 | `fadeUp`, `blink`, `IntersectionObserver` |
| ♿ **Semantic HTML Tags** | 5 | `nav`, `section`, `footer`, `h1`–`h2`, `img alt` |
| 🔗 **Named Anchor IDs** | 8 | 6 sections + 2 project deep-links |
| 🏅 **Live Cert URLs** | 5 | All verified Credly/Coursera links |

---

## 🔮 Roadmap

- [ ] 🌙 Light / dark mode toggle
- [ ] 📄 Downloadable PDF resume button
- [ ] 🌍 Custom domain (`amanaaryan.dev`)
- [ ] 📧 Working contact form (Formspree / EmailJS)
- [ ] 🖼️ Project screenshot thumbnails
- [ ] 📊 GitHub contribution graph embed
- [ ] 🌐 Multi-language support (Hindi / English toggle)
- [ ] 🧪 Lighthouse CI score badges in README

---

## 📜 License

```
MIT License — Copyright (c) 2026 Aman Aaryan

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files, to deal in
the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or
sell copies of the Software, and to permit persons to whom the Software
is furnished to do so, subject to the following conditions:

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.
```

---

<div align="center">

**Built with 🖤 and `#00d4ff` by [Aman Aaryan](https://github.com/thestethoguy)**

*B.Tech Information Technology · KIIT University, Bhubaneswar · 2023–2027*

```
// if you found this useful, drop a ⭐ on the repo
```

</div>
