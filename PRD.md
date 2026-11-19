# Product Requirements Document (PRD) — Aldur Hoang Web Portfolio (2026)

## 1. Positioning & Target Audience
- **Owner:** Aldur Hoang (Nguyễn Vũ Minh Hoàng)
- **Headline:** Multidisciplinary Motion Designer — 2D/3D Motion, Concert Stage Visuals & Brand Systems
- **Target Audience:** Creative Directors, Entertainment/Concert Producers, Advertising & Design Agencies, International & Local Brands.
- **Hosting Target:** `https://aldurhoang612.github.io` (GitHub Pages — $0 cost).

## 2. Site Structure (Sitemap)
1. **Top Navigation (Sticky, minimal):**
   - Brand mark: `ALDUR HOANG`
   - Links: `Work`, `Showreel`, `About`, `Contact`
   - Controls: `EN / VI` toggle
2. **Hero Section:**
   - Bold kinetic typography introducing Aldur Hoang.
   - Short positioning statement (bridging 2D/3D motion, stage visuals, brand identity, and AI workflows).
   - Interactive **Showreel Preview Card** (plays embedded YouTube Showreel `https://youtu.be/lToSXfzFkKI` in a clean fullscreen modal, ready to be swapped when the 2026 Showreel is uploaded).
   - Quick metadata bar: `5+ Years Experience` • `Ho Chi Minh City, VN` • `After Effects / Blender / Figma`.
3. **Selected Works Section (`Work`):**
   - Filter Tabs:
     1. `All`
     2. `Concert & Stage Visuals`
     3. `Commercial Motion & LED`
     4. `Brand Identity & Key Visuals`
     5. `3D Mascots, Editorial & Community`
   - Bento / asymmetric editorial grid showing Flagship projects larger than standard projects.
   - Clicking any project opens a **Case Study View** (modal or dedicated page `/project/:slug`) displaying:
     - Cover visual / video embed
     - Metadata grid: `Year`, `Role`, `Client / Studio`, `Deliverables`, `Specs` (e.g., LED resolution), `Tools`
     - Story sections: `Overview`, `Creative Challenge & Execution`, `Highlights / Impact`
     - Media Gallery grid (with clean placeholders until Aldur adds screenshots/renders)
     - Credit / NDA notice where applicable (e.g., Goofi Team / Shuttlerock).
4. **About & Experience Timeline:**
   - Bio summary & design philosophy.
   - Interactive Experience Timeline (2022 – 2026): Shuttlerock, Goofi Team (Project collaborations), Bloomberg Businessweek Vietnam, Rotaract Club of One Million Lives, DeThird Studio, Hoa Sen University (B.A. Graphic Design).
   - Skills & Toolchain badges (Motion & 3D, Brand & UI, AI & Workflow).
   - Download CV button (links to `assets/cv/Aldur-Hoang-CV-2026.pdf`).
5. **Contact & Footer:**
   - Direct contact info (`aldurhoang@gmail.com`, `(+84) 901 498 984`).
   - Social links: Behance, Vimeo, Instagram, GitHub.
   - Static Contact Form powered by Web3Forms or Formspree (placeholder endpoint clearly marked in `.env.example` or config).

## 3. Content Rules & Safeguards
- Clearly credit studio collaborations (e.g., `Role: 3D & Motion Visual Artist | Studio: Goofi`).
- Support an optional `"nda": true` flag on projects so sensitive commercial work can show a lock badge or blurred preview if needed.
- Ensure the `Ráp Vô Band` project (if added later to Archive) does NOT reuse the Bloomberg Businessweek copy from the old PDF.
