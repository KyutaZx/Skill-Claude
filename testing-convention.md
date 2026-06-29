---
name: testing-convention
description: "Use when writing tests for [framework]. Enforces test structure, coverage target, and what should/shouldn't be tested."
version: 1.0.0
author: [nama kamu]
license: MIT
metadata:
  tags: [testing, quality, coverage]
---

# Testing Convention

## Pendekatan
- Jenis testing : [Unit / Integration / E2E / Manual]
- Framework     : [Jest / Vitest / Playwright / Cypress]

## Yang Wajib Di-test
- Semua fungsi utility & helper
- Logic bisnis yang kompleks
- API endpoint (happy path & error case)
- Komponen kritis yang sering dipakai banyak halaman

## Yang Tidak Perlu Di-test
- Komponen presentational yang sangat sederhana
- Third-party library
- File konfigurasi

## Aturan Penulisan Test
- Satu test file per satu file yang ditest
- Nama deskriptif: "should [expected behavior] when [condition]"
- Pola AAA: Arrange, Act, Assert

## Coverage Target
- Minimum coverage : [angka]%
- Prioritas         : business logic > API > UI

## Pitfalls
- Jangan test implementasi internal -- test behavior/output yang visible
- Jangan share state antar test tanpa cleanup

## Verification Checklist
- [ ] Nama test deskriptif & mengikuti pola AAA
- [ ] Coverage minimum tercapai untuk modul kritis
