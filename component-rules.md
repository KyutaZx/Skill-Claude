---
name: component-rules
description: "Use when creating or editing UI components in [framework, contoh: React/Next.js]. Enforces consistent component structure and server/client boundaries."
version: 1.0.0
author: [nama kamu]
license: MIT
metadata:
  tags: [component, frontend, react, structure]
---

# Component Rules

## Urutan Penulisan dalam Satu Komponen
1. Import
2. Tipe/Interface props
3. Definisi komponen
4. Hooks (`useState`, `useEffect`, dll)
5. Handler & fungsi lokal
6. Return JSX
7. Export

## Aturan Props
- Tipe props wajib eksplisit
- Default value untuk props opsional
- Maksimal [angka] props per komponen -- pecah jika lebih

## Server vs Client Component (Next.js)
- Default: Server Component
- `'use client'` hanya jika butuh: hooks, event listener, browser API, atau library non-SSR

## Komponen Kecil
- Pisah ke file sendiri jika dipakai lebih dari satu tempat
- Boleh inline jika hanya dipakai di satu komponen

## Pitfalls
- Jangan taruh logic fetching langsung di komponen -- pisahkan ke service/hook
- Jangan bikin komponen lebih dari [angka] baris -- pecah jadi sub-komponen

## Verification Checklist
- [ ] Urutan penulisan sesuai konvensi
- [ ] Props punya tipe eksplisit
- [ ] `'use client'` hanya dipakai jika benar-benar perlu
