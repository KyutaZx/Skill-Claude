---
name: performance-optimization
description: "Use when optimizing rendering, bundle size, or asset loading in [framework]."
version: 1.0.0
author: [nama kamu]
license: MIT
metadata:
  tags: [performance, optimization, frontend]
---

# Performance Rules

## Code Splitting
- Dynamic import untuk komponen besar yang tidak langsung terlihat
- Lazy load halaman/komponen yang jarang diakses

## Image Optimization
- Pakai komponen Image dari framework ([next/image], dll)
- Wajib set width & height
- Pakai format WebP/AVIF untuk gambar baru

## Re-render Optimization
- `useMemo` untuk kalkulasi berat
- `useCallback` untuk fungsi yang dikirim sebagai props
- Jangan overuse memo -- profiling dulu sebelum optimasi

## Bundle Size
- Import spesifik, bukan seluruh library
  - Benar: `import { debounce } from 'lodash'`
  - Salah: `import _ from 'lodash'`

## SSR & SSG
- Default Server Component untuk kurangi JS di client
- Static Generation untuk halaman dengan data jarang berubah
- ISR untuk halaman yang butuh revalidasi berkala

## Pitfalls
- Jangan optimasi prematur tanpa profiling
- Jangan import library besar untuk satu fungsi kecil

## Verification Checklist
- [ ] Gambar punya width/height & format optimal
- [ ] Tidak ada import library penuh untuk fungsi kecil
