# Skill Templates — .claude/skills/

Kumpulan ini adalah hasil "pecahan" dari satu CLAUDE.md project (file konfigurasi
umum/satu-pintu) menjadi beberapa SKILL.md spesifik, sesuai format dan prinsip
dari guide "Cara Membuat SKILL.md untuk Claude Code" (@satriabahari).

**Status: TEMPLATE FORMAT** — semua placeholder `[seperti ini]` belum diisi.
Isi dulu sesuai stack & aturan project kamu sebelum dipakai beneran.

## Kenapa dipecah, bukan digabung jadi satu file besar?
Sesuai prinsip guide-nya sendiri:
1. "Mulai dari yang spesifik" — skill per topik/stack, bukan satu skill general.
2. "Jangan panjang-panjang" — idealnya 5-15 baris aturan per skill, biar Claude
   gak bingung prioritas. Kalau semua section CLAUDE.md digabung jadi satu
   SKILL.md, isinya akan jauh lebih panjang dari itu.
3. Auto-inject jadi lebih akurat — skill yang lebih sempit konteksnya lebih
   mudah "dipanggil" sesuai jenis file/tugas yang sedang dikerjakan.

## Daftar File
| File | Diambil dari section CLAUDE.md |
|---|---|
| naming-convention.md       | 5. Naming Conventions |
| code-convention.md         | 6. Code Conventions |
| component-rules.md         | 7. Component Rules |
| styling-convention.md      | 8. Styling Rules |
| api-data-fetching.md       | 9. API & Data Fetching Rules |
| state-management.md        | 10. State Management Rules |
| performance-optimization.md| 11. Performance Rules |
| git-workflow.md            | 12. Git Rules |
| testing-convention.md      | 14. Testing |
| project-guardrails.md      | 15. Do Not |

> Catatan: section 1-4 (Project Overview, Tech Stack, Commands, Project
> Structure) dan 13/16 (Features, Environment Variables) sengaja TIDAK
> dijadikan skill terpisah — sifatnya overview/referensi project, bukan
> "aturan kerja" berulang, jadi lebih cocok tetap di CLAUDE.md utama
> daripada di .claude/skills/.

## Cara Pakai
1. Copy semua file `.md` ke folder `.claude/skills/` di root project kamu.
2. Isi setiap placeholder `[...]` sesuai stack & aturan project (contoh:
   `[Bahasa, contoh: TypeScript]` → `TypeScript`).
3. Sesuaikan/hapus skill yang tidak relevan (misal kalau project full-backend,
   `component-rules.md` & `styling-convention.md` bisa dihapus).
4. Commit folder `.claude/skills/` ke repo biar satu tim pakai standar sama.
