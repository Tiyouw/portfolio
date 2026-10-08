# 🌐 Portfolio — Template Belajar HTML & CSS · HIMASIF Mengajar 2026

Template website portfolio sederhana, dibuat dengan **HTML + CSS vanilla**
(tanpa framework). Dipakai pada kegiatan **HIMASIF Mengajar 2026** di
**SMA Negeri 1 Jember**: peserta mengedit template ini di **VS Code** dan
mempublikasikannya sendiri ke **GitHub Pages** — tiap peserta pulang dengan
URL website portofolio sendiri.

## 📁 Struktur File

```
portfolio/
├── index.html          # Halaman utama (Home, About, Skills, Portfolio, Prestasi, Contact)
├── css/
│   └── style.css       # Semua styling (warna dikumpulkan di blok :root)
├── assets/
│   ├── profil.jpg      # Foto profil placeholder — timpa dengan fotomu
│   ├── proyek-1..3.svg # Placeholder gambar kartu proyek (dipakai kalau .jpg belum ada)
│   └── prestasi-1..3.svg # Placeholder gambar kartu prestasi
├── PANDUAN_PESERTA.md  # Langkah-langkah untuk peserta (PR + Praktik 0–6, 2B opsional)
├── PANDUAN_MENTOR.md   # Panduan pembimbing + timeline + troubleshooting
└── README.md
```

## 🚀 Cara Pakai (Peserta)

**PR sebelum hari-H:**
1. Daftar akun GitHub (https://github.com/signup) + verifikasi email
2. Install **Git** (git-scm.com) dan **VS Code** (code.visualstudio.com)
3. Install extension: **Live Server**, **Color Highlight**, **Auto Rename Tag**

**Hari-H (60 menit):**
1. Klik **"Use this template"** → repo baru bernama `portfolio` (Public)
2. Clone ke laptop lewat VS Code → edit `index.html` & `css/style.css`
3. Commit + push tiap selesai satu praktik
4. Publish: **Settings → Pages → Branch `main` → `/ (root)` → Save**
5. Website online di **`https://username-kamu.github.io/portfolio/`**

Detail lengkap: lihat **`PANDUAN_PESERTA.md`**.

## 🎨 Titik Edit Utama

| Yang mau diubah | Lokasi |
|---|---|
| Nama, peran, deskripsi | `index.html` — komentar `✏️ GANTI` / `✏️ PRAKTIK 1` |
| Foto profil | Timpa file `assets/profil.jpg` (nama harus persis) |
| Gambar kartu proyek/prestasi | Taruh `proyek-1..3.jpg` / `prestasi-1..3.jpg` di `assets/` — **tanpa edit HTML** |
| Daftar hobi/prestasi/cita-cita | `index.html` — blok `<ul class="list">` |
| Kartu prestasi lomba | `index.html` — section `id="prestasi"` (opsional, bisa dihapus) |
| Semua warna website | `css/style.css` — blok `:root` paling atas |
| Jenis & ukuran huruf | `css/style.css` — komentar `✏️ PRAKTIK 4` |

## 🎯 Fitur

- **Dark theme** modern, blok warna (`:root`) gampang diganti — ubah 1 baris,
  seluruh web ikut berubah
- **Responsive** — tampil bagus di HP dan desktop
- **6 section** — Home, About, Skills, Portfolio, Prestasi (opsional), Contact
- **Gambar kartu tinggal timpa file** — taruh `proyek-1.jpg` di `assets/`, kartu
  proyek 1 langsung berganti. Belum diisi? Otomatis pakai gambar placeholder
  (SVG) — tidak pernah muncul ikon gambar rusak
- **Vanilla JavaScript** — hamburger menu & highlight navbar saat scroll
- **Well-commented** — penanda `✏️ PRAKTIK n` biar peserta gampang nyari

## 🛠️ Teknologi & Tools

| Teknologi/Tools | Fungsi |
|---|---|
| HTML5 | Struktur halaman |
| CSS3 | Desain & styling (Flexbox, Grid, Media Query, CSS Variables) |
| JavaScript | Interaktivitas (menu & scroll) |
| VS Code | Editor — dengan Live Server, Color Highlight, Auto Rename Tag |
| Git & GitHub | Simpan versi + hosting GitHub Pages |

## 🌐 Live Demo

[https://tiyouw.github.io/portfolio](https://tiyouw.github.io/portfolio)

## 📄 License

MIT — silakan pakai dan modifikasi untuk belajar atau mengajar.
