---
name: git-workflow
description: "Use when committing changes via Claude Code. Enforces commit message format and auto-commit-after-change workflow for [nama project]."
version: 1.0.0
author: [nama kamu]
license: MIT
metadata:
  tags: [git, workflow, commit]
---

# Git Workflow

## Auto-commit
Setiap kali selesai membuat perubahan/penambahan kode, langsung commit ke repo sebelum lanjut ke task berikutnya -- supaya kode lama vs baru mudah dibandingkan dan bisa di-undo.

## Format Commit Message
```
feat     : [fitur baru]
fix      : [bug fix]
refactor : [perubahan refactor]
style    : [styling/formatting]
docs     : [dokumentasi]
test     : [penambahan/perubahan test]
chore    : [konfigurasi/tooling]
```

## Contoh
```
feat: add user authentication with Google OAuth
fix: resolve infinite scroll not triggering on mobile
refactor: extract user card into reusable component
```

## Aturan Tambahan
- Jangan commit file `.env` atau file berisi secret
- Satu commit = satu perubahan spesifik
- Jangan gabungkan banyak perubahan tak berkaitan dalam satu commit

## Pitfalls
- Jangan commit kode yang belum lulus lint/test
- Jangan rebase/force-push ke branch shared tanpa konfirmasi

## Verification Checklist
- [ ] Commit message sesuai format type: description
- [ ] Tidak ada secret/`.env` ikut ter-commit
