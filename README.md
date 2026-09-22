# Portofolio & Service Portal — Adithya Silaban

**Nama:** Adithya Philip Jona Putra Silaban
**NIM:** 12S24029
**Kelas:** 13SI1
**Mata Kuliah:** Pemrograman dan Pengujian Web (12S3101)
**Live demo:** _(isi link GitHub Pages setelah deploy)_

## Ringkasan Pembaruan Minggu 3

Merefaktor portofolio Minggu 2 (HTML5 semantik + CSS murni) menjadi terintegrasi dengan
Bootstrap 5.3.3 dan Bootstrap Icons, tanpa menghilangkan struktur semantik maupun palet
warna neo-brutalist yang sudah dibangun sebelumnya.

Perubahan utama:
- Navbar diubah menjadi `navbar-expand-lg` dengan toggle hamburger responsif
- Ditambahkan section **Portofolio** baru: grid 4 kartu proyek (`row-cols-1 row-cols-md-2 row-cols-lg-3 g-4`) dengan badge teknologi dan tombol yang membuka **4 modal detail** berbeda
- Formulir konsultasi dimodernisasi dengan Floating Labels, Input Group berikon, dan validasi visual (`invalid-feedback` / `was-validated`)
- Hero section ditambahkan dua tombol CTA
- Seluruh komponen Bootstrap direkolorasi lewat CSS custom properties di `:root` (bukan warna default Bootstrap) — nol penggunaan `!important`

## Tabel Komparasi: Sebelum vs Sesudah

| Aspek | Sebelum (Minggu 2) | Sesudah (Minggu 3) |
|---|---|---|
| CSS Framework | CSS murni, tanpa framework | Bootstrap 5.3.3 (CDN) + Bootstrap Icons |
| Navigasi | Daftar tautan flat, tidak collapsible | Navbar `sticky-top` + toggle hamburger di layar mobile |
| Hero Section | Teks profil tanpa CTA | Teks profil + 2 tombol CTA (Portofolio, Konsultasi) |
| Showcase Proyek | Tidak ada (hanya tabel riwayat) | 4 kartu proyek grid responsif + 4 modal detail |
| Formulir | Input polos + fieldset/legend | Floating Labels, Input Group berikon, validasi visual Bootstrap |
| Theming | Variabel CSS di `:root` (10+) | Variabel CSS dipertahankan, dipakai untuk override warna Bootstrap |
| Penggunaan `!important` | 0 | 0 |

## Struktur Berkas

```
├── index.html
├── style.css
└── README.md
```

## Cara Deploy

```bash
git checkout -b week3-bootstrap
git add .
git commit -m "feat(week3): refactor portfolio to bootstrap 5 grid and modern components"
git push -u origin week3-bootstrap
```

Lalu aktifkan GitHub Pages: **Settings → Pages → Source: branch `week3-bootstrap`**.

> Catatan: file `foto-profil.jpg` yang direferensikan di `index.html` perlu ditambahkan
> ke folder proyek — foto ini tidak termasuk dalam paket refactor ini.
