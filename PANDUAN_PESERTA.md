# 📖 PANDUAN PESERTA — Bikin Portfolio Online Kamu

Ikuti urutan di bawah. Semua dilakukan di browser, **tidak perlu install aplikasi apa pun**.

> ⏱️ Estimasi: 60–75 menit (termasuk daftar GitHub + publish)

---

## PERSIAPAN (dilakukan SEBELUM hari praktik)

### Daftar Akun GitHub
1. Buka **https://github.com/signup**
2. Isi email, password, username.
   - ⚠️ **Username jadi bagian URL portfoliomu:** `username.github.io/portfolio`
   - Pilih yang rapi, contoh: `budi setiawan` → `budisetiawan24`
3. Verifikasi email (buka inbox, klik tombol verify).
4. Sudah punya akun? Lanjut ke Praktik 0.

> Kenapa duluan? Proses daftar + verifikasi email bisa makan 10–15 menit dan bikin
> sesi praktik habis cuma buat nunggu. Selesaikan di rumah.

---

## PRAKTIK 0 — Ambil Template (2 menit)

1. Buka **https://github.com/Tiyouw/portfolio**
2. Klik tombol hijau **"Use this template"** → **"Create a new repository"**
3. Isi:
   - Repository name: `portfolio` (WAJIB `portfolio` biar URL-nya rapi)
   - Visibility: **Public** (wajib, biar bisa publish gratis)
4. Klik **"Create repository from template"**

Sekarang kamu punya salinan sendiri. 🎉

**Cara edit file:**
1. Klik nama file (`index.html` atau `css/style.css`)
2. Klik ikon **pensil ✏️** (kanan atas — "Edit this file")
3. Ubah isinya, lalu scroll bawah → klik **"Commit changes"** (ini = tombol simpan)

> ⚠️ Edit tidak akan tersimpan kalau lupa klik **Commit changes**.

---

## PRAKTIK 1 — Identitas Utama (15 menit) · file `index.html`

### 1a. Ganti nama
Cari tulisan `Nama Kamu`. Ada **2 tempat**:
- di bagian `hero` (nama besar)
- di bagian `footer` (paling bawah)

Ganti keduanya dengan nama kamu.

### 1b. Ganti status/peran
Cari `Frontend Developer` → ganti misal `Siswa RPL` atau `Pelajar`.

### 1c. Ganti deskripsi diri
Cari tag `<p>` di bagian `hero-desc` — paragraf pembuka. Ganti dengan cerita singkatmu.

Di bagian `about` juga ada 2 tag `<p>` (biodata). Ganti juga.

### 1d. Ganti foto profil
1. Siapkan foto kamu, ubah nama file jadi **`profil.jpg`** (huruf kecil semua).
2. Di repo, buka folder **`assets`**.
3. Klik **"Add file" → "Upload files"**, upload `profil.jpg` kamu.
4. Karena namanya sama, GitHub akan menimpa file placeholder lama.

Foto otomatis muncul di bagian hero. Kalau foto tidak muncul, hard refresh (Ctrl+F5).

---

## PRAKTIK 2 — Daftar Hobi / Prestasi / Cita-cita (10 menit) · file `index.html`

Di bagian `about` ada 3 kotak daftar. Daftar di HTML ditulis dengan:

```html
<ul class="list">
    <li>Bermain game</li>
    <li>Membaca komik</li>
</ul>
```

- `<ul>` = **ul**iste = wadah daftar
- `<li>` = **l**ist **i**tem = satu isi daftar

### Tugas
1. Ganti isi tiap `<li>` dengan hobi/prestasi/cita-citamu sendiri.
2. Mau **menambah** item? Copy satu baris `<li>...</li>`, tempel di bawahnya, ganti isinya.
3. Mau **menghapus** item? Hapus seluruh baris `<li>...</li>`.

Contoh hasil:
```html
<div class="list-block">
    <h4>🎯 Hobi</h4>
    <ul class="list">
        <li>Futsal</li>
        <li>Main gitar</li>
        <li>Ngoding santai</li>
    </ul>
</div>
```

---

## PRAKTIK 3 — Warna Tema (12 menit) · file `css/style.css`

Buka folder **`css`** → klik **`style.css`**.

Di baris paling atas ada daftar warna bernama `:root`:

```css
:root {
    --warna-utama: #00d4ff;        /* warna aksen (tombol, judul kecil) */
    --warna-utama-hover: #00b8e6;  /* warna aksen saat kursor di atasnya */
    --warna-bg: #0a0a0a;           /* background halaman */
    --warna-bg-alt: #0e0e0e;       /* background section selang-seling */
    --warna-kartu: #111111;        /* background kartu */
    --warna-garis: #1a1a1a;        /* garis pembatas */
    --warna-judul: #ffffff;        /* warna judul */
    --warna-teks: #e0e0e0;         /* warna tulisan utama */
    --warna-teks-redup: #888888;   /* tulisan sekunder */
}
```

### Tugas
Ganti kode warna (`#00d4ff` dsb). Satu baris diubah → **seluruh website** ikut berubah.

**Pilihan warna siap pakai:**
| Warna | Hex |
|---|---|
| Merah | `#ff6b6b` |
| Kuning | `#ffd93d` |
| Hijau | `#6bff8d` |
| Ungu | `#b36bff` |
| Pink | `#ff6bd6` |
| Biru tua | `#1a365d` |

**Contoh tema terang (pagi):**
```css
--warna-bg: #f5f5f5;
--warna-bg-alt: #ffffff;
--warna-kartu: #ffffff;
--warna-garis: #dddddd;
--warna-judul: #111111;
--warna-teks: #222222;
--warna-teks-redup: #666666;
```

> Mau ubah warna navbar saja? Cari komentar `✏️ PRAKTIK 3` di `.navbar`,
> ubah baris `background-color: rgba(10, 10, 10, 0.95);`
> (angka `0.95` = tingkat transparansi, dari `0` tembus pandang sampai `1` pekat).

---

## PRAKTIK 4 — Tipografi (10 menit) · file `css/style.css`

1. **Jenis huruf** — cari komentar `✏️ PRAKTIK 4` di bagian `body`:
   ```css
   font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
   ```
   Ganti dengan misal: `Arial, sans-serif` atau `'Times New Roman', serif`.

2. **Ukuran judul nama** — cari `.hero-name`, ubah `font-size: 3.5rem;`
   (`rem` = satuan ukuran; makin besar angkanya makin besar tulisannya).

3. **Kontras tulisan** — kalau tulisan susah dibaca, atur ulang `--warna-teks`
   dan `--warna-bg` supaya beda terang/gelapnya jelas.

---

## PRAKTIK 5 — Publish ke Internet (5 menit)

1. Di repo kamu, klik tab **"Settings"**
2. Menu kiri → **"Pages"**
3. Bagian **"Build and deployment"**:
   - Source: **"Deploy from a branch"**
   - Branch: **`main`** → folder **`/ (root)`** → klik **Save**
4. Tunggu 1–3 menit, refresh halaman.
5. 🎉 URL portfoliomu muncul:
   **`https://username-kamu.github.io/portfolio/`**

Buka di HP juga — tampilannya otomatis menyesuaikan.

### Kalau muncul 404
- Tunggu 2–3 menit lagi (build belum selesai), refresh
- Pastikan repo **Public**, bukan Private
- Pastikan branch terpilih `main`, bukan `master`

---

## PRAKTIK 6 — Hias Proyek (tugas tambahan, kalau selesai duluan)

Di bagian `portfolio` ada 3 kartu proyek. Setiap kartu punya:
- `<h3>` = judul proyek
- `<p>` = deskripsi
- `<span class="tag">` = label teknologi
- emoji di `<span class="project-placeholder">` = gambar sementara

**Tugas:**
1. Ganti judul & deskripsi dengan proyekmu sendiri.
2. Ganti emoji placeholder jadi emoji lain (contoh: 🔥 🚀 💡 🎨 🎧 🎵).
3. Ganti link `Live Demo` dan `GitHub` (`href="#"` → link asli).
4. Skill di bagian Skills: ubah angka `style="width: 90%"` dan teks `90%`.

---

## 🏆 Selesai!

Portfoliomu online dan bisa dibagikan lewat link.
Setiap kali kamu edit file dan klik **Commit changes**, website otomatis update
(dalam 1–3 menit).

Ada kendala? Angkat tangan, panggil pembimbing. 🙋
