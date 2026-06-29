---
name: code-convention
description: "Use when writing or reviewing [bahasa/framework] code. Enforces type safety, import order, export pattern, and error handling for [nama project]."
version: 1.0.0
author: [nama kamu]
license: MIT
metadata:
  tags: [code-style, type-safety, convention]
---

# Code Convention

## Pendekatan
- Terapkan [clean code / DRY / SOLID]
- Hindari duplikasi -- jadikan function jika dipakai lebih dari sekali
- Prioritaskan keterbacaan di atas keringkasan

## [Bahasa, contoh: TypeScript]
- Strict mode wajib aktif
- Tidak boleh pakai tipe `any`
- Tulis return type function secara eksplisit
- `interface` untuk object shape, `type` untuk union/intersection

## Urutan Import
1. Library eksternal
2. Internal absolut (`@/...`)
3. Internal relatif (`./`, `../`)
4. Tipe dan interface
5. Assets dan styles

## Export Pattern
- Named export untuk komponen & fungsi
- Default export hanya untuk file entry-point (`page.tsx`, `layout.tsx`)

## Error Handling
- Semua async function wajib try-catch
- Pesan error informatif dan spesifik
- Jangan biarkan error tanpa penanganan

## Pitfalls
- Jangan commit kode dengan `console.log` debug
- Jangan ignore error type checking tanpa alasan jelas

## Verification Checklist
- [ ] Tidak ada `any` / type-ignore tanpa alasan
- [ ] Import terurut sesuai aturan
- [ ] Semua async function ada try-catch
