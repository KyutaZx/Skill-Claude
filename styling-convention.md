---
name: styling-convention
description: "Use when writing styles/CSS for [styling tool, contoh: Tailwind CSS]. Enforces class ordering, responsive design, and dark mode rules."
version: 1.0.0
author: [nama kamu]
license: MIT
metadata:
  tags: [styling, css, tailwind, responsive]
---

# Styling Convention

## Pendekatan
- Pakai [Tailwind CSS / CSS Modules / Styled Components]
- Jangan pakai inline style kecuali nilai benar-benar dinamis
- Jangan pakai `!important`

## Tailwind CSS (jika dipakai)
- Class langsung di JSX
- Pakai `clsx`/`cn` untuk conditional class
- Ekstrak ke komponen jika class yang sama dipakai berulang
- Urutan class: layout > spacing > sizing > color > typography > state

## Responsive Design
- Pendekatan mobile-first
- Breakpoint: sm (640px) / md (768px) / lg (1024px) / xl (1280px)

## Dark Mode
- Pakai [dark: prefix Tailwind / CSS variables]
- Wajib test tampilan dark mode setiap bikin komponen baru

## Design Tokens
- Pakai CSS variable untuk warna, spacing, typography
- Jangan hardcode nilai warna langsung

## Pitfalls
- Jangan duplikasi kombinasi utility class yang panjang -- extract ke komponen
- Jangan lupa test di breakpoint terkecil

## Verification Checklist
- [ ] Tidak ada inline style/`!important` yang tidak perlu
- [ ] Sudah dicek di mode mobile & dark mode
