# 🧑‍🏫 PANDUAN MENTOR — Setup & Jalankan Praktikum

Panduan untuk pembimbing proker pengajaran HTML/CSS.

---

## Pra-Proker (Persiapan, H-1)

### Checklist Pembimbing
- [ ] Repo template **https://github.com/Tiyouw/portfolio** sudah Public
- [ ] Repo sudah ditandai sebagai **template repo** (tombol "Use this template" muncul)
- [ ] Bagikan link repo template ke grup peserta SEBELUM hari-H,
      minta mereka **daftar akun GitHub dan verifikasi email duluan**
      (menghemat waktu sesi, karena signup + verifikasi email bisa makan 10–15 menit per orang)
- [ ] Siapkan koneksi internet cadangan (hotspot) — lab sering lemot
- [ ] Print/copy `PANDUAN_PESERTA.md` atau bagikan versi digitalnya

### Batasan yang perlu diantisipasi
| Masalah | Solusi |
|---|---|
| Peserta belum 13 tahun (batas umur GitHub) | Pakai akun milik sekolah/org dengan bimbingan mentor |
| Email verifikasi gak masuk | Cek folder spam; atau daftar ulang pakai email lain |
| Lab komputer tidak bisa install apa pun | Aman — semua alur hanya pakai browser |
| Github lambat di jaringan sekolah | Web editor GitHub ringan; hindari buka Codespaces massal |

---

## Struktur Sesi Praktikum (contoh 90 menit)

| Menit | Aktivitas |
|---|---|
| 00–10 | Pembukaan: tunjukkan live demo hasil akhir (`tiyouw.github.io/portfolio`), motivational — "1 jam lagi URL ini punya kalian" |
| 10–20 | Peserta duplikat template (Langkah 2 di PANDUAN_PESERTA) |
| 20–45 | Edit `index.html`: nama, role, deskripsi, skills, proyek |
| 45–60 | Edit `css/style.css`: ganti warna aksen, eksperimen |
| 60–70 | Deploy GitHub Pages (Langkah 4) |
| 70–85 | Cek hasil, debugging 404, tugas tambahan untuk yang selesai duluan |
| 85–90 | Sesi share: 2–3 peserta buka URL-nya di depan, foto screenshot buat dokumentasi proker |

---

## Poin Materi yang Bisa Ditarik Saat Peserta Edit

Sambil praktik, hubungkan ke teori sesi materi:

1. **Saat ganti "Nama Kamu"**: tunjukkan struktur `index.html` — tag `<h1>`, `<p>`, `<a>`, semantic tags (`<nav>`, `<section>`, `<footer>`)
2. **Saat ganti warna `#00d4ff`**: jelaskan CSS selector & property — `.hero-name { color: ... }`, format hex color, class vs tag selector
3. **Saat deploy**: singgung konsep git sambil lalu — edit → commit = save dengan history; repo = folder proyek di cloud
4. **Saat buka dari HP**: jelaskan responsive design & media query (buka DevTools → toggle device toolbar, Ctrl+Shift+M)

---

## Troubleshooting Cepat

| Gejala | Penyebab umum | Fix |
|---|---|---|
| Tombol "Use this template" tidak muncul | Repo belum jadi template / peserta login akun salah | Mentor buka Settings repo → checkbox "Template repository" |
| 404 setelah deploy | Build belum selesai / branch salah / repo Private | Tunggu 3 menit; cek Settings → Pages; cek visibility repo |
| Edit tidak tersimpan | Lupa klik "Commit changes" | Biasakan selalu commit sebelum pindah file |
| CSS tidak berubah | Edit di file salah / cache browser | Pastikan edit `css/style.css`, hard refresh (Ctrl+F5) |
| Website tidak update setelah edit | Build Pages jalan 1–3 menit | Tunggu lalu refresh; cek tab Actions repo |

---

## Setelah Proker

- [ ] Kumpulkan link portfolio semua peserta (bikin Google Form satu field URL)
- [ ] Sertifikat / e-certificate bisa dicantumkan link portfolio peserta
- [ ] Follow-up: peserta bisa lanjut belajar sendiri — JavaScript, hosting domain sendiri

---

## File di Repo Ini

| File | Fungsi |
|---|---|
| `index.html` | Halaman utama — konten yang diedit peserta |
| `css/style.css` | Styling — warna & tampilan yang diedit peserta |
| `README.md` | Deskripsi repo (untuk publik) |
| `PANDUAN_PESERTA.md` | Langkah demi langkah untuk peserta |
| `PANDUAN_MENTOR.md` | File ini |
