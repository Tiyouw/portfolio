# 🧑‍🏫 PANDUAN MENTOR — HIMASIF Mengajar 2026

Kustomisasi website portofolio dengan HTML & CSS · SMA Negeri 1 Jember
Sabtu, 10 Oktober 2026 · 20 peserta (ekstrakurikuler Code Master)

> Dokumen ini disinkronkan dengan proposal resmi (rundown Lampiran 1) dan
> keputusan panitia: **jalur VS Code**, akun GitHub per siswa, publish wajib.

---

## 1. Keputusan Teknis (final)

| Keputusan | Pilihan |
|---|---|
| Editor | **VS Code** (bukan browser-only) |
| Version control | Git + akun GitHub **masing-masing siswa** |
| Hosting | GitHub Pages — tiap siswa punya URL sendiri |
| Preview | Extension **Live Server** |
| Backup | Akun HIMASIF bersama, kalau ada siswa yang gagal buat akun |

Alasan deploy wajib: momen **Apresiasi Karya (11.50–12.05)** paling hidup kalau
siswa membuka **URL live sendiri**, dan URL jadi bukti karya yang bisa dikumpulkan
panitia untuk LPJ (screenshot / daftar link).

---

## 2. Tools & Extension — Rekomendasi untuk Pembelajaran

### Wajib (dipasang di PR sebelum hari-H)

| Extension | Kenapa penting untuk pembelajaran |
|---|---|
| **Live Server** (Ritwick Dey) | Preview website yang **auto-refresh tiap kali save**. Siswa melihat konsekuensi langsung: edit → Ctrl+S → tampilan berubah. Ini terasosiasi terkuat antara kode dan hasil — inti dari belajar HTML/CSS |
| **Color Highlight** (naumovs) | Kode hex (`#00d4ff`) langsung tampil sebagai blok warna di editor. Siswa yang belum hafal kode warna tetap bisa "membaca" palet websitenya |
| **Auto Rename Tag** (Jun Han) | Saat mengganti `<h3>` → `<h2>`, tag penutup ikut berubah otomatis. Mencegah error paling umum pemula: lupa menutup tag |

### Fitur bawaan VS Code — ajarin sambil praktik (tanpa install)

| Fitur | Cara pakai | Dipakai di praktik |
|---|---|---|
| **Color Picker bawaan** | Hover kode hex → klik kotak kecil → color picker visual muncul. Geser untuk memilih warna tanpa menghafal hex | Praktik 3 (warna) |
| **Emmet** | Ketik `li*3` + `Tab` → langsung jadi 3 baris `<li></li>`. Juga `h1` + Tab, `ul>li` + Tab | Praktik 2 (daftar) |
| **Multi-cursor** | `Ctrl+D` untuk pilih kata berikutnya yang sama — ganti beberapa tempat sekaligus | Praktik 1 (nama muncul 2x) |
| **Format document** | `Shift+Alt+F` merapikan indentasi kode | Kapan saja |

### Opsional (kalau kuota waktu ekstension berjalan lancar)

| Extension | Fungsi |
|---|---|
| **Prettier** | Auto-format kode (`Shift+Alt+F` sudah bawaan tanpa Prettier untuk HTML/CSS — Prettier lebih konsisten) |
| **HTML CSS Support** | Autocomplete class CSS di HTML |
| **Material Icon Theme** | Kosmetik sidebar — biar folder terlihat enak dibaca |

> Jangan tambah extension lain hari-H. Semakin sedikit tools, semakin besar
> porsi kognitif siswa terserap ke materi HTML/CSS, bukan ke tools.

---

## 3. Pra-Acara (H-1 dan sebelumnya)

### Checklist panitia — PR siswa

Kirim ke grup kelas / dibacakan saat ekstrakurikuler, paling lambat H-3:

- [ ] Daftar akun GitHub + verifikasi email (**pakai Gmail pribadi**, cek spam)
- [ ] Install **Git** (git-scm.com) dan **VS Code** (code.visualstudio.com)
- [ ] Install 3 extension: **Live Server, Color Highlight, Auto Rename Tag**
- [ ] Siapkan foto, dinamai persis: `profil.jpg` (wajib) + opsional
      `proyek-1..3.jpg` dan `prestasi-1..3.jpg` untuk gambar kartu
- [ ] (Disarankan) coba sendiri langkah Praktik 0 dari `PANDUAN_PESERTA.md`

PR ini adalah **penghemat waktu terbesar**: daftar akun + install + verifikasi
bisa memakan 30–45 menit per siswa — tidak muat di sesi 60 menit.

### Checklist panitia — internal

- [ ] Repo template https://github.com/Tiyouw/portfolio — status Public + template
- [ ] Folder `assets/` berisi: `profil.jpg` + 6 SVG placeholder
      (`proyek-1..3.svg`, `prestasi-1..3.svg`) — jangan sampai terhapus
- [ ] Cek akses `tiyouw.github.io/portfolio` (demo) dari jaringan sekolah.
      Kalau diblokir, siapkan screenshot offline
- [ ] Siapkan hotspot cadangan (panitia)
- [ ] Siapkan **akun HIMASIF bersama** (kalau ada siswa gagal bikin akun →
      jalankan fallback, lihat bagian 6)
- [ ] Komputer lab: pastikan bisa install VS Code + Git (kalau terkunci admin,
      koordinasi dengan sekolah jauh hari)
- [ ] Print / bagikan `PANDUAN_PESERTA.md` versi digital
- [ ] Briefing pendamping: baca panduan peserta sampai bisa memandu Praktik 0–5

---

## 4. Mapping Rundown Resmi → Timeline Praktik

Rundown resmi (Lampiran 1 proposal):

| No | Acara | Waktu | Durasi |
|---|---|---|---|
| 8 | Sesi Praktik | 10.37–11.37 | 60 menit |
| 9 | Buffer | 11.37–11.50 | 13 menit |
| 10 | Apresiasi Karya | 11.50–12.05 | 15 menit |

### Timeline internal sesi praktik (60 menit)

| Jam | Durasi | Praktik di panduan | Output siswa |
|---|---|---|---|
| 10.37–10.45 | 8 m | **Praktik 0** — Use this template + clone + git config + Go Live | Repo sendiri, file terbuka di VS Code, Live Server jalan |
| 10.45–11.00 | 15 m | **Praktik 1** — nama, peran, deskripsi, foto profil, **commit+push pertama**. (Praktik 1B — ganti gambar kartu — opsional, tawarkan ke siswa yang cepat) | Identitas terganti, perubahan masuk GitHub |
| 11.00–11.10 | 10 m | **Praktik 2** — `<ul>/<li>` hobi, prestasi, cita-cita (+ trik Emmet). Section **Prestasi** (2B) = opsional, tidak masuk alur wajib | Daftar pribadi |
| 11.10–11.22 | 12 m | **Praktik 3** — warna via `:root` + Color Picker | Tema warna pilihan sendiri |
| 11.22–11.32 | 10 m | **Praktik 4** — `font-family`, `font-size`, kontras | Tipografi khas |
| 11.32–11.37 | 5 m | **Praktik 5** — push terakhir + **aktifkan GitHub Pages** | URL `username.github.io/portfolio` dibuat |
| 11.37–11.50 | 13 m | **Buffer resmi** — pastikan SEMUA URL live; bantu yang 404 / commit gagal; siswa cepat kerjakan Praktik 6 | Semua siswa punya URL hidup |
| 11.50–12.05 | 15 m | **Apresiasi Karya** — siswa maju buka URL-nya sendiri di depan | Showcase |

**Aturan emas: sebelum 11.50 semua URL harus sudah hidup.** Praktik 6 tidak
pernah boleh mengalahkan Praktik 5.

### Section Prestasi (Praktik 2B) — opsional

Template punya section **Prestasi** sendiri (di bawah Portfolio) berisi 3 kartu,
strukturnya identik dengan kartu Portfolio (`.project-card`). Ini menjawab
permintaan ketua pelaksana agar siswa bisa menampilkan prestasi lomba.

Aturan pendamping:
- **Jangan jadikan wajib.** Tidak semua siswa punya prestasi. Cukup tawarkan
  saat siswa selesai Praktik 2 atau di buffer.
- **Kalau siswa hapus section-nya, ingatkan hapus juga** link `<li>Prestasi</li>`
  di navbar — kalau tidak, klik menunya tidak mengarah ke mana-mana.
- Inilah tempat pertama siswa mempraktikkan **copy-paste blok HTML** (menambah
  atau mengurangi kartu) — bagus untuk mengajarkan struktur berulang.

### Gambar pada kartu (Praktik 1B)

Baik kartu Portfolio maupun Prestasi memakai `<img src="assets/xxx.jpg">`.
Selama file `.jpg` belum ada, JS fallback menampilkan `assets/xxx.svg`
(placeholder bertuliskan "FOTO PROYEK 1", dst.) supaya **tidak ada ikon rusak**.

Poin yang perlu ditekankan ke pendamping:
- Ganti gambar = **timpa file** di folder `assets`, **tidak perlu edit HTML**.
  Nama file harus persis (`proyek-1.jpg`, `prestasi-2.jpg`, dst., huruf kecil).
- Ini analogi bagus untuk "HTML menunjuk lokasi file, bukan menyimpan gambar".
- Ingatkan ukuran file < 1 MB (kuota GitHub Pages & kecepatan lab).
- Bagian ini menghemat waktu: siswa yang belum punya screenshot proyek tidak
  perlu apa-apa — placeholder sudah rapi sejak awal.

### Pembagian peran pendamping saat praktik

- **1 pendamping di depan** — sinkron dengan pemateri, memandu langkah per langkah
- **2–3 pendamping keliling** — fokus ke siswa yang diam > 2 menit (indikator macet)
- Masalah di lingkungan siswa (clone gagal, auth gagal) ditangani pendamping
  keliling, **jangan** memotong alur pemateri di depan

---

## 5. Poin Materi yang Ditarik Sambil Praktik

Hubungkan aksi siswa ke teori sesi pemaparan materi:

1. **Ganti "Nama Kamu"** → struktur HTML: `<h1>`, `<p>`, `<a>`, semantic tags
   (`<nav>`, `<section>`, `<footer>`); heading = hierarki judul.
2. **Emmet `li*3`** → repetisi elemen; `<ul>` vs `<ol>`; relasi parent-child.
3. **Color Picker + `:root`** → CSS variable = satu nilai dipakai berkali-kali;
   hex color; selector class (`.hero-name`) vs tag (`body`).
4. **Ganti `font-family`** → font stack & fallback; satuan `rem`.
5. **Live Server refresh** → alur edit–save–refresh = siklus kerja developer.
6. **Commit & push** → analogi: commit = titik simpan game; push = upload
   titik simpan ke cloud; repo = folder proyek di cloud.
7. **GitHub Pages** → website statis = file HTML/CSS yang disajikan server;
   URL = identitas.
8. **Buka URL di HP** → responsive design; tunjukkan media query di DevTools
   (`Ctrl+Shift+M`) kalau ada waktu.

---

## 6. Fallback & Troubleshooting

### Fallback akun GitHub
Siswa yang **gagal** membuat akun setelah semua usaha (email tertolak, HP tidak
ada, dll): pakai **akun HIMASIF bersama** di satu komputer, bikin 1 repo
`himameng26-namasiswa` per siswa. URL jadi
`himasif.github.io/himameng26-namasiswa` — tetap ada nama siswa, tetap bisa
ditunjukkan di Apresiasi. Setelah acara, file dikirim ke siswa untuk dipindah
ke akun pribadi kalau nanti berhasil daftar.

### Tabel troubleshooting cepat

| Gejala | Penyebab umum | Fix |
|---|---|---|
| Clone gagal / tidak muncul popup auth | Git belum terinstall | Cek `git --version` di terminal; install dari git-scm.com |
| Popup auth GitHub tidak terbuka | Popup diblokir / komputer lab terkunci | Login via browser, salin kode perangkat (VS Code menawarkan opsi ini) |
| Commit gagal "Please tell me who you are" | `git config` belum diisi | Jalankan 2 perintah `git config --global` di Praktik 0c |
| Foto tidak muncul | Nama file tidak persis `profil.jpg` (mis. `Foto.JPG`, `profil (1).jpg`) | Rename persis, huruf kecil semua |
| Kartu proyek/prestasi masih placeholder | File `.jpg` belum ada di folder `assets` | Normal & bukan error. Taruh `proyek-1.jpg` dst. di `assets/` |
| Gambar kartu jadi ikon rusak (▯) | File ada tapi salah folder / nama salah | Cek: harus di dalam `assets/`, nama persis, huruf kecil |
| Gambar kartu tidak ganti-ganti walau sudah di-push | Cache browser | Hard refresh `Ctrl+F5`; tunggu build Pages 1–3 menit |
| CSS tidak berubah | Edit file salah / belum save / cache | Cek judul tab editor (titik = belum save); hard refresh `Ctrl+F5` di Live Server |
| "Go Live" tidak ada | Extension Live Server belum terinstall | Install dulu, restart VS Code |
| 404 di URL Pages | Build belum selesai / branch salah / repo Private | Tunggu 3 menit; Settings → Pages harus `main` + `/ (root)`; cek visibility |
| Website tidak update setelah push | Build 1–3 menit | Tunggu, refresh; cek tab **Actions** di repo |
| Tombol "Use this template" tidak ada | Belum login / membuka repo lain | Pastikan login akun siswa & buka URL template yang benar |
| Halaman putih total | Tag terhapus tidak sengaja | `git checkout -- index.html` (kembalikan versi terakhir) atau revert lewat tab History di GitHub |

---

## 7. Setelah Acara

- [ ] Kumpulkan URL portfolio semua siswa (Google Form 1 field URL) — bukti
      indikator kinerja untuk LPJ
- [ ] Screenshot hasil karya terbaik untuk dokumentasi
- [ ] Kirim file/repo milik siswa yang fallback akun bersama ke akun pribadi mereka
- [ ] Follow-up materi: JavaScript dasar, custom domain, dsb. (keberlanjutan
      program, sesuai bagian I proposal)

---

## 8. File di Repo Ini

| File | Fungsi |
|---|---|
| `index.html` | Halaman utama — konten yang diedit siswa |
| `css/style.css` | Styling — warna di `:root`, tipografi beranotasi |
| `assets/profil.jpg` | Foto placeholder — ditimpa foto siswa |
| `assets/proyek-1..3.svg`, `assets/prestasi-1..3.svg` | Gambar placeholder kartu — otomatis dipakai kalau `.jpg` belum ada. **Jangan dihapus.** |
| `PANDUAN_PESERTA.md` | Langkah demi langkah siswa (PR + Praktik 0–6) |
| `PANDUAN_MENTOR.md` | File ini |
| `README.md` | Deskripsi repo publik |
