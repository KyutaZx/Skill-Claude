---
name: project-guardrails
description: "Use as a safety checklist before Claude Code makes structural, dependency, security, or database changes. Lists actions that always require explicit confirmation."
version: 1.0.0
author: [nama kamu]
license: MIT
metadata:
  tags: [guardrails, safety, do-not-list]
---

# Project Guardrails (Do Not List)

Jika instruksi atau prompt ambigu, TANYA DULU sebelum mulai coding. Jangan berasumsi dan langsung mengerjakan tanpa konfirmasi.

## Struktur & File
- Jangan buat folder baru tanpa konfirmasi
- Jangan hapus file tanpa konfirmasi
- Jangan pindahkan file tanpa konfirmasi
- Jangan ubah struktur folder yang sudah ada

## Kode
- Jangan gunakan tipe `any`
- Jangan hardcode nilai yang seharusnya dari environment variable
- Jangan commit file `.env` atau file berisi secret
- Jangan install package baru tanpa konfirmasi
- Jangan hapus/ubah fitur yang sudah berjalan tanpa instruksi jelas

## Database
- Jangan jalankan perintah yang mengubah/menghapus data production
- Jangan buat migrasi database tanpa konfirmasi
- Jangan expose credential database ke sisi client

## Keamanan
- Jangan expose API key/secret apapun ke client
- Jangan bypass validasi input dari user
- Jangan skip error handling di API routes

## Verification Checklist
- [ ] Sudah konfirmasi ke user sebelum ubah struktur/dependency/database
- [ ] Tidak ada secret yang terekspos ke client/commit
