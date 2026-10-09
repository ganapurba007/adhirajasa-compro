# CHANGELOG.md

> Riwayat aktif proyek — hanya simpan ~10-15 fase terbaru di sini. Fase lama dipindahkan ke `CHANGELOG-archive.md` (ringkas, jangan copy-paste detail penuh). Entri terbaru selalu di PALING ATAS.

<!--
Format tiap entri:

## Fase [N] — [judul singkat] ([tanggal])
**FR terkait:** [nomor FR dari PRD.md §3, kalau ada]
**Yang dikerjakan:**
- [poin singkat]
**File yang berubah:** [daftar file utama, tidak perlu semua kalau banyak]
**Test:** [X passed / Y total]
**Docs updated:** [PRD §9 / SCHEMA.md / tidak ada perubahan scope]
-->

## Fase 0 — Setup Dasar Proyek & Data JSON (2026-10-09)
**Yang dikerjakan:**
- Konfigurasi Tech Stack Vue 3 + Tailwind CSS + Vue Router + Pinia + Lucide Icons + Vitest
- Integrasi Tailwind CSS v4 dengan custom design tokens (warna brand, tipografi Outfit/Inter)
- Setup struktur data dummy JSON lengkap di `src/data/` (`company.json`, `home.json`, `services.json`, `projects.json`, `team.json`, `testimonials.json`) sesuai `SCHEMA.md`
- Inisialisasi rute dan dynamic meta title di Vue Router
- Verifikasi build dan unit test
**File yang berubah:** AGENTS.md, context/PRD.md, context/CHANGELOG.md, package.json, postcss.config.js, tailwind.config.js, src/assets/main.css, src/router/index.js, src/views/*, src/data/*.json
**Test:** 1 passed / 1 total
**Docs updated:** PRD §9 (Amandemen stack Vue 3) dan AGENTS.md
