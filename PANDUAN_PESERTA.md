# 📖 PANDUAN PESERTA — Bikin Portfolio Online Kamu

Ikuti langkah-langkah di bawah ini dengan urutan. Semua dilakukan di browser,
tidak perlu install aplikasi apa pun.

> ⏱️ Estimasi waktu: 30–45 menit

---

## Langkah 1 — Bikin Akun GitHub (5 menit)

1. Buka **https://github.com/signup**
2. Isi email, password, dan username.
   - ⚠️ **Username penting!** Nanti jadi bagian dari URL portfoliomu:
     `username.github.io/portfolio`
   - Pilih username yang rapi, contoh: `budi setiawan` → `budisetiawan24`
3. Verifikasi email (cek inbox, klik tombol verify).

---

## Langkah 2 — Duplikat Repo Template (2 menit)

1. Buka repo template: **https://github.com/Tiyouw/portfolio**
2. Klik tombol hijau **"Use this template"** → **"Create a new repository"**
3. Isi:
   - Repository name: `portfolio` (WAJIB nama ini, biar URL konsisten)
   - Visibility: **Public** (wajib public biar GitHub Pages gratis)
4. Klik **"Create repository from template"**

Sekarang kamu punya salinan repo sendiri di akunmu. 🎉

---

## Langkah 3 — Edit Kode di Browser (20 menit)

### 3a. Buka file untuk diedit
1. Di repo kamu, klik file **`index.html`**
2. Klik ikon **pensil ✏️** (pojok kanan atas, tulisan "Edit this file")
3. Edit isinya (lihat daftar di bawah)
4. Setelah selesai, scroll ke bawah → tulis pesan commit singkat,
   contoh: `ganti nama jadi Budi` → klik **"Commit changes"**

### 3b. Yang wajib kamu ganti di `index.html`

| Cari teks ini | Ganti dengan |
|---|---|
| `Nama Kamu` | Nama lengkap kamu (muncul 2x: di Hero dan Footer) |
| `Frontend Developer` | Role kamu, contoh: `Siswa RPL` |
| `Halo, nama saya` | Boleh dibiarkan atau ganti sapaan lain |
| `Siswa SMK yang suka bikin website...` | Deskripsi singkat kamu |
| `email@kamu.com` | Email kamu (di bagian Contact) |
| `https://instagram.com/` | Link Instagram kamu |
| Persentase skill (`90%`, `80%`, dst.) | Skill kamu yang asli |
| Nama proyek (`Landing Page`, `To-Do List App`, dst.) | Proyek kamu sendiri |

### 3c. Edit tampilan di `css/style.css`

1. Buka folder **`css`** → klik **`style.css`** → ikon pensil ✏️
2. Hal seru yang bisa diubah:
   - **Warna aksen**: cari semua `#00d4ff` (warna cyan), ganti dengan warna lain.
     Pilihan warna: `#ff6b6b` (merah), `#ffd93d` (kuning), `#6bff8d` (hijau),
     `#b36bff` (ungu), `#ff6bd6` (pink)
   - **Background**: cari `#0a0a0a` (hitam pekat) → ganti `#1a1a2e` (biru gelap) atau `#0f0f0f`
   - **Font besar nama**: cari `.hero-name` → ubah `font-size`

### 3d. Ganti foto (opsional)

1. Di halaman utama repo kamu, klik **"Add file" → "Upload files"**
2. Drag & drop foto kamu (contoh: `foto.jpg`) — WAJIB nama file `foto.jpg`
3. Commit.
4. Edit `index.html`, cari bagian `hero-avatar`, ganti isinya jadi:
   ```html
   <img src="foto.jpg" alt="Foto saya" class="avatar-img">
   ```
5. Edit `css/style.css`, tambahkan di paling bawah:
   ```css
   .avatar-img {
       width: 100%;
       height: 100%;
       object-fit: cover;
       border-radius: 20px;
   }
   ```

---

## Langkah 4 — Deploy ke GitHub Pages (2 menit)

1. Di repo kamu, klik tab **"Settings"** (menu atas repo)
2. Menu kiri → **"Pages"** (bagian Code and automation)
3. Bagian **"Build and deployment"**:
   - Source: **"Deploy from a branch"**
   - Branch: pilih **`main`** → folder **`/ (root)`** → klik **Save**
4. Tunggu 1–3 menit, refresh halaman.
5. 🎉 URL portfoliomu muncul di atas:
   **`https://username-kamu.github.io/portfolio/`**

---

## Langkah 5 — Cek Hasil

Buka URL kamu di browser (bisa juga di HP).

Kalau muncul error 404:
- Tunggu 2–3 menit lagi (build belum selesai), refresh
- Pastikan repo **Public**, bukan Private
- Pastikan branch yang dipilih `main`, bukan `master`

---

## 🏆 Selesai!

Portfoliomu sekarang online dan bisa dibagikan ke siapa saja lewat link.
Setiap kali kamu edit kode di GitHub dan commit, website otomatis update.

**Tugas tambahan (kalau sudah selesai duluan):**
- Ganti semua warna jadi tema favoritmu
- Tambah 1 skill card baru di bagian Skills (copy-paste blok `skill-card`)
- Tambah 1 proyek baru di bagian Portfolio (copy-paste blok `project-card`)
- Ganti emoji placeholder proyek jadi emoji lain

Ada kendala? Angkat tangan, panggil pembimbing. 🙋
