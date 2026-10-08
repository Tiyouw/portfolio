# 📖 PANDUAN PESERTA — Bikin Website Portofolio Online Kamu

Kegiatan **HIMASIF Mengajar 2026** · SMA Negeri 1 Jember

Tools yang dipakai: **VS Code + akun GitHub**. Semua langkah di bawah ikuti urutan.

> ⏱️ Sesi praktik: 60 menit + 13 menit buffer. Bawa laptop kalau ada — kalau
> tidak, pakai komputer lab (asalkan VS Code & Git sudah terinstall).

---

## PERSIAPAN — PR SEBELUM HARI-H (WAJIB)

Kalau ini belum selesai, praktik akan tertinggal jauh dari teman sekelas.
Selesaikan di rumah, butuh ~30 menit.

### ✅ Checklist PR

- [ ] **1. Daftar akun GitHub** di https://github.com/signup
      - Pakai email yang aktif (Gmail pribadi lebih aman daripada email sekolah)
      - Cek folder **spam** kalau email verifikasi tidak masuk
      - ⚠️ **Username penting!** Nanti jadi alamat websitemu:
        `username.github.io/portfolio`
        Contoh: nama "Budi Setiawan" → username `budisetiawan26`
- [ ] **2. Install Git** dari https://git-scm.com/downloads
      (saat install, pilih Next terus saja / default)
- [ ] **3. Install VS Code** dari https://code.visualstudio.com/download
- [ ] **4. Install 3 extension di VS Code** (buka VS Code → ikon kotak di sidebar
      kiri → cari nama extension → klik Install):
      1. **Live Server** — biar lihat hasil website langsung tiap kali save
      2. **Color Highlight** — kode warna langsung tampil sebagai blok warna
      3. **Auto Rename Tag** — mencegah error saat ganti tag HTML
- [ ] **5. Siapkan foto profil** — foto bagus, simpan di laptop, beri nama `profil.jpg`

> 📌 File yang perlu kamu siapkan **hanya `profil.jpg`**. Kartu Portfolio &
> Prestasi diisi pakai tulisan (tidak butuh upload gambar).

---

## PRAKTIK 0 — Ambil Template ke Komputer (8 menit)

### 0a. Duplikat template ke akun GitHub-mu
1. Buka **https://github.com/Tiyouw/portfolio**
2. Klik tombol hijau **"Use this template"** → **"Create a new repository"**
3. Isi:
   - Repository name: **`portfolio`** (WAJIB nama ini biar URL-nya rapi)
   - Visibility: **Public** (wajib, biar bisa publish gratis)
4. Klik **"Create repository from template"**

### 0b. Clone (download) template ke laptop
1. Di halaman repo yang barusan dibuat, klik tombol hijau **"< > Code"** → copy
   link yang muncul (contoh: `https://github.com/budisetiawan26/portfolio.git`)
2. Buka **VS Code**
3. Menu **View → Command Palette** (atau tekan `Ctrl+Shift+P`), ketik
   `Git: Clone`, Enter
4. Tempel (paste) link tadi → Enter → pilih folder untuk menyimpan (misalnya
   `Documents`)
5. Popup login GitHub muncul → klik **"Allow"** → login di browser → kembali ke
   VS Code → klik **"Open"**

Sekarang kamu bisa lihat file `index.html` di sidebar kiri VS Code. 🎉

### 0c. Kenalkan dirimu ke Git (sekali saja, per laptop)
Buka menu **Terminal → New Terminal**, ketik dua baris ini (ganti namamu),
tekan Enter setiap baris:

```bash
git config --global user.name "Budi Setiawan"
git config --global user.email "email-github-kamu@gmail.com"
```

> Tanpa langkah ini, commit nanti akan error. Hanya perlu sekali per komputer.

### 0d. Nyalakan Live Server
1. Klik file **`index.html`** di sidebar kiri
2. Cari tulisan **"Go Live"** di pojok kanan bawah jendela VS Code → klik
3. Browser terbuka menampilkan websitemu. Setiap kali kamu save (`Ctrl+S`),
   tampilan otomatis ter-update. **Jendela ini biarkan tetap terbuka sepanjang praktik.**

---

## PRAKTIK 1 — Identitas Utama (15 menit) · file `index.html`

Edit di VS Code, lihat hasilnya di jendela Live Server.

### 1a. Ganti nama
Cari tulisan `Nama Kamu` (pakai `Ctrl+F`). Ada **2 tempat**:
- di bagian hero (nama besar)
- di bagian footer (paling bawah)

Ganti keduanya dengan nama kamu, **jangan lupa save** (`Ctrl+S`).

### 1b. Ganti status/peran
Cari `Frontend Developer` → ganti, misal: `Pelajar` atau `Siswa SMA N 1 Jember`.

### 1c. Ganti deskripsi diri
Tag `<p>` adalah paragraf. Ganti isi paragraf pembuka dan 2 paragraf di bagian
"Siapa saya?" dengan cerita kamu sendiri.

### 1d. Ganti foto profil
1. Siapkan foto kamu yang sudah dinamai **`profil.jpg`**
2. Di VS Code, copy foto itu ke folder **`assets`** (buka folder lewat File
   Explorer, atau drag & drop ke sidebar VS Code)
3. Karena namanya sama dengan foto placeholder, foto lama otomatis tertimpa.
4. Lihat Live Server — foto kamu sudah tampil. Kalau belum, refresh (`Ctrl+F5`).

### 1e. Simpan pekerjaan pertamamu (commit + push)
Sekarang kamu belajar cara "menyimpan ke internet". Ini yang bikin websitemu
online nanti:

1. Klik ikon **Source Control** di sidebar kiri (ikon seperti garis bercabang)
2. Klik tombol **"+"** (Stage All Changes)
3. Ketik pesan singkat di kotak atas, misal: `ganti nama dan foto`
4. Klik **"Commit"** → kalau muncul tanya "publish branch?", klik **"Yes"**

Sekarang buka GitHub-mu di browser, refresh repo. File yang berubah sudah ada
di sana. Setiap selesai satu praktik, ulangi langkah ini (commit + push).

---

## PRAKTIK 2 — Daftar Hobi / Prestasi / Cita-cita (10 menit) · file `index.html`

Di bagian `about` ada 3 kotak daftar. Daftar di HTML ditulis dengan:

```html
<ul class="list">
    <li>Bermain game</li>
    <li>Membaca komik</li>
</ul>
```

- `<ul>` = wadah daftar
- `<li>` = satu isi daftar

### Tugas
1. Ganti isi tiap `<li>` dengan hobi/prestasi/cita-cita kamu sendiri.
2. Mau **menambah** item? Coba trik Emmet: ketik `li*3` lalu tekan **Tab** —
   VS Code otomatis bikin 3 baris `<li></li>`. Isi satu per satu.
3. Mau **menghapus** item? Hapus seluruh baris `<li>...</li>`.

### 💡 Trik: Auto Rename Tag
Coba klik tag `<h4>` di salah satu judul daftar, ganti jadi `<h3>` — tag
penutupnya ikut berganti otomatis. Ini gunanya extension Auto Rename Tag.

Jangan lupa **commit + push** setelah selesai.

---

## PRAKTIK 2B (OPSIONAL) — Section Prestasi · file `index.html`

Template sudah punya section **Prestasi** (posisinya di bawah Portfolio, di atas
Contact) berisi 3 kartu prestasi. Bagian ini **opsional** — kalau kamu belum
punya prestasi, lewati saja.

### Cara mengisi kartu prestasi
Strukturnya **sama persis** dengan kartu Portfolio:

- `<h3>` = nama lomba / kegiatan
- `<p>` = penjelasan singkat (tingkat, penyelenggara, tahun)
- `<span class="tag">` = label kecil (peringkat / tahun / tingkat)
- emoji di `<span class="project-placeholder">` = ikon sementara
  (contoh: 🥇 🥈 🥉 🏅 📜 🎖️)

### Tugas (kalau ada prestasi)
1. Ganti nama lomba, penjelasan, dan label di tiap kartu dengan punyamu.
2. Kartu kelebihan? Hapus satu blok `<div class="project-card">...</div>`.
   Kurang? Copy satu blok penuh lalu tempel di bawahnya.

### ⚠️ Kalau kamu TIDAK punya prestasi
Hapus **dua** hal ini (kalau hanya hapus salah satu, menunya jadi error):
1. Seluruh section `<section id="prestasi" class="prestasi"> ... </section>`
2. Baris link navbar: `<li><a href="#prestasi" class="nav-link">Prestasi</a></li>`

Jangan lupa **commit + push** setelah selesai.

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

Ganti satu baris → **seluruh website** ikut berubah. Inilah gunanya CSS variable.

### 💡 Dua cara milih warna di VS Code

1. **Color Picker bawaan VS Code**: arahkan mouse ke kotak kecil di atas kode
   warna (misal kotak cyan di atas `#00d4ff`) → klik → muncul jendela color
   picker. Geser bolanya buat pilih warna, selesai.
2. **Color Highlight extension**: semua kode hex langsung tampil sebagai blok
   warna, jadi kamu langsung tahu warna apa itu sebelum dibuka di browser.

### Ide warna siap pakai
| Tema | `--warna-utama` |
|---|---|
| Cyan (bawaan) | `#00d4ff` |
| Merah | `#ff6b6b` |
| Kuning | `#ffd93d` |
| Hijau | `#6bff8d` |
| Ungu | `#b36bff` |
| Pink | `#ff6bd6` |

Bonus (kalau sempat): coba ubah `--warna-bg` dan `--warna-judul` untuk bikin
**tema terang** (background putih, tulisan gelap).

Jangan lupa **commit + push**.

---

## PRAKTIK 4 — Tipografi (10 menit) · file `css/style.css`

1. **Jenis huruf** — cari komentar `✏️ PRAKTIK 4` di bagian `body`:
   ```css
   font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
   ```
   Ganti, misal: `Arial, sans-serif` atau `'Times New Roman', serif`.
   Lihat Live Server — font langsung berubah.

2. **Ukuran nama** — cari `.hero-name`, ubah angkanya:
   ```css
   font-size: 3.5rem;   /* coba ganti jadi 2.5rem atau 5rem */
   ```

3. **Kelebihan kontras** — kalau tulisan susah dibaca, jauhkan warna teks dan
   background (yang terang makin terang, yang gelap makin gelap).

Jangan lupa **commit + push**.

---

## PRAKTIK 5 — Publish ke Internet (5 menit) 🎉

Ini momen paling penting — websitemu jadi punya **alamat sendiri** di internet.

1. Pastikan semua perubahan sudah di-commit + push (lihat ikon Source Control —
   harusnya tidak ada lagi angka biru di tombolnya)
2. Buka repo kamu di browser: `https://github.com/username-kamu/portfolio`
3. Klik tab **"Settings"** → menu kiri **"Pages"**
4. Bagian **"Build and deployment"**:
   - Source: **"Deploy from a branch"**
   - Branch: **`main`** → folder **`/ (root)`** → klik **Save**
5. Tunggu 1–3 menit, refresh halaman Settings → Pages.
6. 🎉 Alamat websitemu muncul di atas:
   **`https://username-kamu.github.io/portfolio/`**

Buka alamat itu di HP juga — tampilannya otomatis menyesuaikan (responsive).

### Kalau muncul 404 (halaman tidak ditemukan)
- Tunggu 2–3 menit lagi, refresh (build masih berjalan)
- Pastikan repo **Public**, bukan Private
- Pastikan branch terpilih `main`, bukan `master`

---

## PRAKTIK 6 — Hias Karyamu (tugas tambahan, kalau selesai duluan)

Di bagian `portfolio` ada 3 kartu proyek. Setiap kartu punya:
- `<h3>` = judul proyek
- `<p>` = deskripsi
- `<span class="tag">` = label teknologi
- emoji di `<span class="project-placeholder">` = gambar sementara

**Tugas:**
1. Ganti judul & deskripsi dengan proyek/karya kamu sendiri.
2. Ganti emoji placeholder jadi emoji lain (contoh: 🔥 🚀 💡 🎨 🎧 🎵).
3. Ubah persentase skill di bagian Skills: `style="width: 90%"` dan teks `90%`.
4. Coba tambah 1 kartu skill baru: copy blok `<div class="skill-card">...</div>`
   satu kali, tempel di bawahnya, ganti isinya.

Jangan lupa **commit + push** lagi!

---

## 🏆 Selesai!

Websitemu sekarang **online 24 jam** dan bisa dibagikan ke siapa saja lewat link.
Setiap kali edit + commit + push, website otomatis ter-update dalam 1–3 menit.

Ada kendala? Angkat tangan, panggil pendamping. 🙋
