---
name: naming-convention
description: "Use when creating or renaming files, folders, variables, functions, or git branches. Enforces consistent naming convention for [nama project]."
version: 1.0.0
author: [nama kamu]
license: MIT
metadata:
  tags: [naming, convention, style-guide]
---

# Naming Convention

## File & Folder
- Komponen      : PascalCase   contoh: `UserCard.tsx`
- Non-komponen  : camelCase    contoh: `useAuth.ts`, `getUserById.ts`
- Folder        : kebab-case   contoh: `user-profile/`
- Halaman       : `page.tsx` atau `index.tsx`
- Layout        : `layout.tsx`
- Test file     : `[nama].test.ts` atau `[nama].spec.ts`

## Di Dalam Kode
- Variabel       : camelCase     `userData`, `isLoading`
- Konstanta      : UPPER_SNAKE   `MAX_RETRY`, `BASE_URL`
- Fungsi         : camelCase     `getUserById`, `formatDate`
- Tipe/Interface : PascalCase    `UserType`, `ApiResponse`
- Enum           : PascalCase    `UserRole`, `OrderStatus`
- CSS Class      : kebab-case    `user-card`, `nav-item`

## Git Branch
- Fitur baru : `feat/[nama-fitur]`
- Bug fix    : `fix/[nama-bug]`
- Hotfix     : `hotfix/[nama]`
- Refactor   : `refactor/[nama]`

## Pitfalls
- Jangan campur PascalCase & camelCase untuk hal yang sama dalam satu project
- Jangan pakai singkatan ambigu (`usr`, `tmp`, `val`) tanpa konteks jelas

## Verification Checklist
- [ ] Nama file/folder sesuai kategori (komponen/non-komponen/folder)
- [ ] Variabel & fungsi konsisten camelCase
- [ ] Branch name sesuai prefix yang berlaku
