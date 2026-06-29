---
name: api-data-fetching
description: "Use when writing API endpoints or data-fetching logic. Enforces consistent response format, error handling, and server/client fetch boundaries."
version: 1.0.0
author: [nama kamu]
license: MIT
metadata:
  tags: [api, data-fetching, backend]
---

# API & Data Fetching Rules

## Server vs Client Fetch
- Server fetch : data awal yang tidak butuh interaksi user
- Client fetch  : data yang berubah setelah interaksi user
- Pakai [SWR / React Query] untuk client fetch -- jangan pakai `useEffect`

## Format Response API
Selalu konsisten di semua endpoint:
```
{ success: boolean, data: T | null, message: string }
```

## Error Handling
- Try-catch di semua endpoint
- Status code yang tepat (200, 400, 401, 404, 500)
- Jangan expose detail error ke client di production

## Lokasi Fungsi Fetch
- Simpan di folder [services / api / lib]
- Jangan tulis fungsi fetch langsung di dalam komponen

## Environment
- URL & API key wajib lewat environment variable
- Jangan hardcode URL/secret apapun di kode

## Pitfalls
- Jangan return raw error object ke client
- Jangan lupa rate limit/auth check di endpoint sensitif

## Verification Checklist
- [ ] Response format konsisten di semua endpoint
- [ ] Tidak ada secret/URL hardcoded
