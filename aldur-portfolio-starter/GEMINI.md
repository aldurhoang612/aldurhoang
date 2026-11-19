# Workspace Instructions for Google Antigravity — Aldur Hoang Portfolio

## 1. Project Mission
Build a high-craft, dark-mode-first personal portfolio website for **Aldur Hoang (Nguyễn Vũ Minh Hoàng)**, a Multidisciplinary Motion Designer specializing in **Concert & Stage Visuals, 2D/3D Motion Graphics, Brand Identity Systems, and Visual Design**.

The website must be **100% free to host** on **GitHub Pages** (`https://aldurhoang612.github.io`) with zero backend dependencies.

## 2. Tech Stack & Architecture Rules
- **Recommended Stack:** Vite + React + TypeScript + Tailwind CSS (or Astro + Tailwind CSS if static-first is preferred). Must compile cleanly to static files (`dist/`) for GitHub Pages deployment via GitHub Actions.
- **Alternative Lightweight Stack:** Plain HTML5 + Tailwind CSS + Vanilla JS / GSAP if requested by the user.
- **Data-Driven Content:** Always load profile info, experience, and portfolio projects dynamically from `data/projects.json`. Never hardcode project lists directly inside JSX/HTML components so Aldur can easily add/edit projects later.
- **Static Hosting Constraints (GitHub Pages):**
  - Do NOT store large video files (`.mov`, large `.mp4` > 5MB) in the Git repository.
  - Embed full-length reels and stage visuals via **YouTube / Vimeo iframes** or lazy-loaded lightbox players.
  - Only allow ultra-compressed short muted preview loops (`< 3MB`, `.mp4`/`.webm`) for hover cards if provided in `assets/videos/`.
  - All images must use `loading="lazy"` and graceful placeholder fallbacks (stylized gradient/typography cards) when actual media files have not been dropped into `assets/images/projects/` yet.
  - Contact form must be static-compatible (e.g., **Web3Forms** or **Formspree**, plus direct `mailto:aldurhoang@gmail.com` fallback).

## 3. Visual & UX Direction
- **Aesthetic:** Editorial Dark Mode, cinema & concert-stage inspired (`#09090B` obsidian background, `#F4F4F5` crisp off-white typography, subtle glassmorphism borders, restrained electric accent color).
- **Typography:** Expressive display sans-serif for headings (e.g., *Syne*, *Space Grotesk*, or *Plus Jakarta Sans* — must support Vietnamese diacritics cleanly!) paired with clean body typography (*Inter* or *Be Vietnam Pro*) and monospace metadata (*JetBrains Mono*) for project years, resolutions (e.g., `9830×2868 LED`), and tools.
- **Bilingual Support:** Support an **EN / VI** language toggle (default: **EN**, with full Vietnamese content available in `data/projects.json`).
- **Motion & Interaction:** Smooth, intentional micro-interactions (subtle hover reveals, category filter transitions, project case-study drawer/modal or dedicated route, video showreel lightbox). Respect `prefers-reduced-motion`.
- **Responsive Design:** Mobile-first polish across desktop (`1440px`), tablet, and mobile (`390px`).

## 4. Quality & Verification Checklist
Before finishing any milestone:
1. Run build (`npm run build`) and ensure zero TypeScript/bundler errors.
2. Verify in browser preview that all 4 project categories filter smoothly, the EN/VI toggle switches all copy accurately, and broken/missing local images fall back gracefully to clean visual cards.
3. Include a ready-to-use `.github/workflows/deploy.yml` configured for GitHub Pages deployment to `aldurhoang612.github.io`.
