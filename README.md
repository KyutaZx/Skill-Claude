# Claude Skill Templates

Kumpulan template *skills* modular untuk konfigurasi AI Coding Assistant (seperti Claude Code, Cursor, atau AI agent sejenis). Proyek ini memecah konfigurasi *monolithic* `CLAUDE.md` menjadi file-file berformat *skill* yang spesifik, kontekstual, dan terfokus pada satu area pengembangan.

Didasarkan pada prinsip dan praktik terbaik **"Cara Membuat SKILL.md untuk Claude Code"** (@satriabahari).

---

## Mengapa Proyek Ini Dibuat?

Seringkali, pengembang memasukkan semua aturan dan konteks proyek ke dalam satu file besar (contoh: `CLAUDE.md`). Pendekatan ini memiliki kelemahan mendasar saat digunakan bersama AI:
1. **Context Overload:** AI sering kebingungan menentukan prioritas instruksi jika file panduan terlalu panjang dan kompleks.
2. **Relevansi Rendah:** Aturan *styling* (CSS) tidak relevan saat AI sedang mengerjakan logika *backend* atau *database*, namun tetap terbaca karena berada di file yang sama, membuang token dan mengaburkan fokus AI.

**Solusinya:** Memecah aturan proyek yang kaku menjadi file-file *skill* modular.
* **Fokus & Tajam:** Setiap file idealnya hanya berisi 5-15 baris instruksi spesifik.
* **Injeksi Konteks Akurat:** AI dapat memanggil dan menerapkan *skill* yang tepat sesuai dengan jenis tugas atau ekstensi file yang sedang dikerjakan.

## Daftar Template Skill

Setiap file di bawah ini mewakili satu *domain* aturan spesifik di dalam proyek. Template menggunakan *placeholders* `[...]` yang siap Anda isi dengan *tech-stack* spesifik Anda.

| Nama File | Fokus / Area | Kegunaan |
|-----------|--------------|----------|
| `naming-convention.md` | **Naming Conventions** | Aturan penamaan variabel, fungsi, tipe data, file, dan folder. |
| `code-convention.md` | **Code Conventions** | Standar penulisan kode, pola arsitektur, dan paradigma *clean code*. |
| `component-rules.md` | **Component Rules** | Standar pembuatan komponen UI, *props*, dan hierarki (React/Vue/dsb). |
| `styling-convention.md` | **Styling Rules** | Konvensi *styling* menggunakan framework CSS (Tailwind, SCSS, dsb). |
| `api-data-fetching.md` | **API & Data Fetching** | Standar pemanggilan API, *error handling*, validasi payload, dan *loading*. |
| `state-management.md` | **State Management** | Aturan pengelolaan *state* lokal dan global (Zustand, Redux, dsb). |
| `performance-optimization.md`| **Performance Rules** | Praktik optimasi performa seperti *memoization* atau *lazy loading*. |
| `git-workflow.md` | **Git Rules** | Konvensi format pesan *commit*, penamaan *branch*, dan *workflow*. |
| `testing-convention.md` | **Testing** | Aturan penulisan *unit test*, *integration test*, dan metrik *coverage*. |
| `project-guardrails.md` | **Do Not (Guardrails)** | Hal-hal yang **dilarang keras** dilakukan oleh AI (menghapus komen, dsb). |

> **Praktik Terbaik:** Konteks umum (seperti *Project Overview*, *Tech Stack Utama*, atau *Environment Variables*) **TIDAK** disarankan menjadi *skill* terpisah. Hal tersebut bersifat referensi makro dan sebaiknya tetap diletakkan di `CLAUDE.md` utama agar selalu dibaca di awal percakapan.

## Panduan Penggunaan

1. **Salin Template:**
   Unduh atau salin file `.md` yang Anda butuhkan dari repositori ini, lalu masukkan ke dalam direktori konfigurasi AI di *root* proyek Anda (misalnya `.claude/skills/` atau `.cursor/rules/`).

2. **Isi Placeholders:**
   Buka setiap file dan temukan teks dalam kurung siku `[seperti ini]`. Ganti teks tersebut dengan standar aktual proyek Anda.
   > *Contoh:* Ubah `[Sebutkan framework styling, misal: Tailwind CSS]` menjadi `Tailwind CSS v3`.

3. **Sesuaikan dengan Proyek (Tailoring):**
   Gunakan hanya *skill* yang relevan. Jika Anda membangun proyek *backend* murni (misalnya dengan Go/Node.js), hapus file `component-rules.md` dan `styling-convention.md`.

4. **Bagikan ke Tim:**
   Lakukan *commit* terhadap folder *skills* tersebut ke repositori Anda. Dengan demikian, seluruh anggota tim yang menggunakan AI asisten akan secara otomatis mengikuti standar proyek yang identik.

---
*Didesain untuk mendorong pengembangan yang dibantu AI (AI-assisted development) menjadi lebih terstruktur, efisien, dan profesional.*
