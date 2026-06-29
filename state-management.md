---
name: state-management
description: "Use when deciding or implementing state management approach (local, lifted, global) in [framework]."
version: 1.0.0
author: [nama kamu]
license: MIT
metadata:
  tags: [state-management, frontend]
---

# State Management Rules

## Hierarki State (gunakan dari yang paling sederhana)
1. Local state (`useState`)  -- hanya dipakai 1 komponen
2. Lifted state              -- dipakai 2-3 komponen berdekatan
3. Global state              -- dipakai banyak komponen/tempat

## Kapan Pakai Global State
- Data user/auth yang dibutuhkan banyak komponen
- UI state global (tema, bahasa, layout toggle)
- Data yang perlu persist antar halaman

## Aturan [Zustand / Redux / Pinia]
- Store per domain/fitur, jangan satu store untuk semuanya
- Jangan simpan data yang bisa dihitung dari data lain (derived state)
- Pakai selector untuk ambil data spesifik dari store

## Kapan Pakai Context
- Untuk data yang jarang berubah (tema, locale, config global)
- Jangan untuk state yang sering berubah

## Pitfalls
- Jangan taruh semua state di global -- bikin app sulit di-debug
- Jangan lupa cleanup subscription/listener di global store

## Verification Checklist
- [ ] State ditaruh di level paling sederhana yang cukup
- [ ] Tidak ada derived state yang disimpan manual
