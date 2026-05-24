# 🪳 Cockroach Janta Party — Blog Page

> A college project blog documenting India's most viral youth movement of 2026.

## 📋 Project Overview

This is a static HTML blog page about the **Cockroach Janta Party (CJP)** — the satirical political movement that took India by storm in May 2026. The project includes a fully designed blog page with CI/CD pipelines implemented using GitHub Actions.

---

## 🚀 CI/CD Pipeline

This project implements a complete **CI/CD (Continuous Integration / Continuous Deployment)** pipeline.

### What is CI/CD?

| Term | Full Form | What it does |
|------|-----------|--------------|
| **CI** | Continuous Integration | Automatically tests/validates code on every push or pull request |
| **CD** | Continuous Deployment | Automatically deploys the site to GitHub Pages when code is merged to `main` |

### Pipeline Architecture

```
Developer pushes code
        │
        ▼
┌───────────────────┐
│  CI Pipeline      │  (runs on every push & pull request)
│  ─────────────    │
│  ✅ HTML Validate  │
│  ✅ Lighthouse     │
│  ✅ Link Checker   │
└────────┬──────────┘
         │ All checks pass
         ▼
┌───────────────────┐
│  CD Pipeline      │  (runs only on push to `main`)
│  ─────────────    │
│  📦 Build Site    │
│  🚀 Deploy Pages  │
│  📢 Post Summary  │
└───────────────────┘
         │
         ▼
   🌐 Live Website
   (GitHub Pages URL)
```

### Files

```
.github/
└── workflows/
    ├── ci.yml    → Continuous Integration (test & validate)
    └── cd.yml    → Continuous Deployment (build & deploy)
index.html        → Main blog page
README.md         → This file
```

---

## 🛠️ How to Set Up

### 1. Fork / Clone this repo
```bash
git clone https://github.com/YOUR_USERNAME/cjp-blog.git
cd cjp-blog
```

### 2. Enable GitHub Pages
- Go to your repo → **Settings** → **Pages**
- Under "Build and deployment", select **GitHub Actions** as the source
- Save

### 3. Push to main
Any push to `main` will:
1. **Trigger CI** — validate HTML, run Lighthouse, check links
2. **Trigger CD** — build and deploy to GitHub Pages automatically

### 4. View your live site
After the first deployment, your site will be live at:
```
https://YOUR_USERNAME.github.io/cjp-blog/
```

---

## 📁 Project Structure

```
cjp-blog/
├── index.html                  # Blog page (all HTML, CSS, JS in one file)
├── README.md                   # Project documentation
└── .github/
    └── workflows/
        ├── ci.yml              # CI: HTML validation, Lighthouse, link check
        └── cd.yml              # CD: build + deploy to GitHub Pages
```

---

## 📰 Blog Content

The blog covers:
- **Origin** — How a Supreme Court judge's remark sparked a movement
- **Timeline** — Day-by-day chronicle from May 15–24, 2026
- **Demands** — The CJP's 5 core policy demands
- **Crackdown** — Government actions, bans, and the digital siege
- **Reactions** — Voices from politicians, citizens, and the founder
- **Analysis** — Why the movement matters for Indian democracy

---

## 🎓 College Project Notes

This project demonstrates:
- ✅ Static website development (HTML/CSS/JS)
- ✅ CI/CD implementation with GitHub Actions
- ✅ Automated HTML validation (html-validate)
- ✅ Performance auditing (Lighthouse CI)
- ✅ Automated deployment (GitHub Pages)
- ✅ Branching strategy (develop → main)
- ✅ Concurrency control for deployments

---

*Sources: Wikipedia, CBS News, CNN, Al Jazeera, Business Today, The Quint, Lukmaan IAS*
