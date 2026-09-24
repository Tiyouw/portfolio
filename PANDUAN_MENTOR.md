# 🧑‍🏫 PANDUAN MENTOR — Setup & Jalankan Praktikum

Panduan untuk pembimbing proker pengajaran HTML/CSS.

---

## 1. Sinkronisasi dengan Draft Rundown Acara

Draft rundown dari panitia (Sesi Praktik 60 menit, 4 praktik) **sudah bagus secara
pedagogi** — urutannya logis: identitas → konten → warna → tipografi.
Tapi ada beberapa titik yang **tidak cocok dengan template** dan **satu langkah besar
yang hilang**. Berikut hasil audit.

### 1.1 Yang sudah cocok (tidak perlu diubah)

| Draft praktik | Status di template |
|---|---|
| Ganti teks nama bawaan | ✅ `Nama Kamu` (hero + footer) |
| Ubah deskripsi biodata pada `<p>` | ✅ `hero-desc` + 2 `<p>` di `about` |
| Tambah `<ul>` / `<li>` untuk hobi, prestasi, cita-cita | ✅ 3 kotak daftar sudah disiapkan di `about` |
| Ubah `font-family` | ✅ ada komentar `✏️ PRAKTIK 4` |
| Ubah `font-size` judul | ✅ `.hero-name` diberi komentar |

### 1.2 Yang harus di-adjust (perbedaan draft vs template)

| # | Draft bilang | Masalah | Sudah diperbaiki jadi |
|---|---|---|---|
| 1 | "ganti file gambar profil **di folder aset**" | Template lama **tidak punya** folder `assets/` — peserta akan bingung nyari | Folder `assets/` dibuat, berisi `profil.jpg`. Peserta upload foto dengan nama sama → otomatis tertimpa |
| 2 | "ganti warna pada properti `background-color` bagian header" | Navbar lama pakai properti `background` (bukan `background-color`) + nilai `rgba()` → peserta yang Ctrl+F `background-color` **tidak menemukannya** | Navbar diubah ke `background-color: rgba(...)` dengan komentar `✏️ PRAKTIK 3` |
| 3 | Implisit: "cari kode warna hex di berbagai tempat" | Warna tersebar di ~40 baris. Salah ganti 1 baris → warna web jadi belang | Semua warna dikumpulkan di blok `:root` (CSS variables) di baris paling atas. Ubah 1 baris → seluruh web berubah |
| 4 | Tidak ada langkah **publish/deploy** | Padahal output yang diinginkan: **tiap peserta punya URL portfolio sendiri**. Tanpa ini, hasil kerja cuma ada di laptop/lab | Ditambah **Praktik 5 — Publish ke GitHub Pages** (5 menit) |
| 5 | Tidak ada langkah **daftar akun GitHub** | Tidak mungkin publish tanpa akun. Daftar + verifikasi email = 10–15 menit | Diubah jadi **PR (pekerjaan rumah) sebelum hari-H** |

### 1.3 Soal waktu — 60 menit KURANG

Hitung realistis dengan draf saat ini:

| Aktivitas | Estimasi |
|---|---|
| Buka & sambung internet + pembukaan | 10 menit |
| Praktik 0 — ambil template | 3 menit |
| Praktik 1 — identitas + foto | 15 menit |
| Praktik 2 — daftar | 10 menit |
| Praktik 3 — warna | 12 menit |
| Praktik 4 — tipografi | 10 menit |
| Praktik 5 — publish | 5 menit |
| Buffer debugging (404, lupa commit, dll) | 10 menit |
| **Total** | **75 menit** |

**Rekomendasi:**
- Naikkan slot jadi **90 menit**, ATAU
- Kalau tetap 60 menit: jadikan Praktik 4 sebagai **tugas tambahan** (yang cepat selesai
  lanjut sendiri), dan wajibkan daftar GitHub sebagai PR sebelum hari-H.
- Jangan potong Praktik 5 — publish adalah **momentum utama** proker ini.

---

## 2. Jawaban Pertanyaan Tools (buat dibalas ke grup)

> Rizqi: *"kira-kira tools apa aja yang dipakai?"*

**Rekomendasi: browser saja, tanpa install.** Alasannya: lab sekolah sering
terkunci hak admin, versi Node/Python beda-beda, dan install Git di 30 komputer
makan waktu sesi. Semua alur template ini memang dirancang browser-only.

| Kebutuhan | Tools | Install? | Catatan |
|---|---|---|---|
| Edit kode | **GitHub web editor** (github.com) | ❌ | Cukup klik pensil ✏️ di file. Paling aman untuk lab |
| Lihat hasil | **Tab browser** (buka file HTML / URL Pages) | ❌ | Refresh tiap habis commit |
| Inspeksi warna & layout | **DevTools browser** (F12) | ❌ | Bawaan Chrome/Edge/Firefox |
| Foto profil | **HP peserta** (kirim ke email diri sendiri) atau kabel data | ❌ | Siapkan sebelum sesi |

**Kalau lab benar-benar mendukung install** (opsional, bukan wajib):

| Tools | Fungsi | Catatan |
|---|---|---|
| **VS Code** | Editor nyaman + autocomplete | Extension wajib: **Live Server** (preview auto-refresh) |
| **Git** (opsional) | Push dari komputer | Butuh pemahaman dasar clone/commit/push — berat untuk pemula |
| **Chrome** | DevTools | Umumnya sudah ada |

**Yang sebaiknya DIHINDARI untuk sesi massal:**
- ❌ **GitHub Codespaces** — VS Code di browser, keren tapi boros bandwidth &
  kena limit kuota gratis. Jaringan lab yang lemot akan tersedak kalau 30 orang
  buka serentak.
- ❌ **Vercel / Netlify** — butuh login OAuth, konsep "deploy" lebih abstrak,
  dan menambah satu platform lagi yang harus dipahami pemula. GitHub Pages
  cukup karena peserta sudah di GitHub untuk edit.
- ❌ **Live Share / ngoding bersama real-time** — rawan bentrok, tidak perlu.

**Jawaban singkat untuk grup:**
> Browser doang cukup — edit di github.com, publish ke GitHub Pages. Nggak perlu install
> apa-apa, jadi aman di lab yang komputernya dikunci. Kalau lab-nya bebas install,
> boleh VS Code + Live Server biar preview-nya auto-refresh, tapi itu bonus, bukan syarat.

---

## 3. Pra-Proker (Persiapan, H-1)

### Checklist Pembimbing
- [ ] Repo template **https://github.com/Tiyouw/portfolio** Public
- [ ] Repo sudah ditandai **template repository** (tombol "Use this template" muncul)
- [ ] Bagikan link repo ke grup **SEBELUM hari-H** + minta peserta **daftar GitHub
      dan verifikasi email duluan** (ini penghemat waktu terbesar)
- [ ] Siapkan koneksi internet cadangan (hotspot)
- [ ] Bagikan `PANDUAN_PESERTA.md` (versi digital)
- [ ] Kalau ada peserta < 13 tahun (batas umur GitHub): siapkan akun organisasi
      sekolah dan dampingi
- [ ] Cek: apakah `tiyouw.github.io/portfolio` bisa diakses dari jaringan lab?
      Kalau diblokir, siapkan screenshot demo offline

### Batasan yang perlu diantisipasi

| Masalah | Solusi |
|---|---|
| Email verifikasi tidak masuk | Cek folder spam; daftar ulang pakai email lain |
| Lab tidak bisa install apa pun | Aman — semua alur browser-only |
| GitHub lambat di jaringan sekolah | Web editor ringan; hindari Codespaces massal |
| Peserta lupa klik "Commit changes" | Ingatkan tiap 5 menit |

---

## 4. Struktur Sesi Praktikum (90 menit, versi yang disarankan)

| Menit | Aktivitas | Praktik di Panduan |
|---|---|---|
| 00–10 | Pembukaan: tunjukkan live demo, motivasi — "1 jam lagi URL ini punya kalian" | — |
| 10–13 | Ambil template dari repo | Praktik 0 |
| 13–28 | Nama, peran, deskripsi, foto profil | Praktik 1 |
| 28–38 | Daftar hobi / prestasi / cita-cita (`<ul>`, `<li>`) | Praktik 2 |
| 38–50 | Warna tema (blok `:root`) | Praktik 3 |
| 50–60 | Tipografi (`font-family`, `font-size`) | Praktik 4 |
| 60–65 | Publish ke GitHub Pages | Praktik 5 |
| 65–80 | Cek hasil, debugging 404, tugas tambahan | Praktik 6 |
| 80–90 | Share: 2–3 peserta buka URL di depan, screenshot dokumentasi | — |

---

## 5. Poin Materi yang Ditarik Sambil Peserta Edit

Hubungkan aksi peserta ke teori dari sesi materi:

1. **Ganti "Nama Kamu"** → struktur HTML: tag `<h1>`, `<p>`, `<a>`, semantic tags
   (`<nav>`, `<section>`, `<footer>`).
2. **Tambah `<li>`** → konsep daftar bersarang (nested element), hubungan induk–anak.
3. **Ganti warna `:root`** → CSS variable, hex color, dan konsep *satu nilai dipakai
   berkali-kali* (DRY).
4. **Ganti `background-color` navbar** → CSS selector (`.navbar`), property vs value.
5. **Ganti `font-family`** → font stack, fallback, satuan `rem`.
6. **Saat publish** → sambil lalu singgung konsep git: commit = simpan + riwayat,
   repo = folder proyek di cloud.
7. **Buka di HP** → responsive design & media query (demonstrasi Ctrl+Shift+M di DevTools).

---

## 6. Troubleshooting Cepat

| Gejala | Penyebab umum | Fix |
|---|---|---|
| Tombol "Use this template" tidak muncul | Peserta login akun salah / repo bukan template | Mentor cek Settings repo → centang "Template repository" |
| 404 setelah publish | Build belum selesai / branch salah / repo Private | Tunggu 3 menit; cek Settings → Pages; cek visibility |
| Edit tidak tersimpan | Lupa klik "Commit changes" | Selalu commit sebelum pindah file |
| Foto profil tidak muncul | Nama file beda (mis. `Foto.JPG` vs `profil.jpg`) | Nama harus **persis** `profil.jpg`, huruf kecil |
| CSS tidak berubah | Edit di file salah / cache browser | Pastikan edit `css/style.css`, hard refresh Ctrl+F5 |
| Website tidak update setelah edit | Build Pages jalan 1–3 menit | Tunggu lalu refresh; cek tab **Actions** di repo |
| Halaman putih total | Tag HTML terhapus tidak sengaja | Minta peserta cek diff lewat tab **History**, atau ambil ulang dari template |

---

## 7. Setelah Proker

- [ ] Kumpulkan link portfolio semua peserta (Google Form 1 field URL)
- [ ] Sertifikat bisa mencantumkan link portfolio peserta
- [ ] Dokumentasi: screenshot hasil + testimoni peserta
- [ ] Follow-up: peserta lanjut sendiri — JavaScript, custom domain, dsb.

---

## 8. File di Repo Ini

| File | Fungsi |
|---|---|
| `index.html` | Halaman utama — konten yang diedit peserta |
| `css/style.css` | Styling — warna & tampilan yang diedit peserta |
| `assets/profil.jpg` | Foto profil placeholder (ditimpa peserta) |
| `README.md` | Deskripsi repo (untuk publik) |
| `PANDUAN_PESERTA.md` | Langkah demi langkah untuk peserta |
| `PANDUAN_MENTOR.md` | File ini |
