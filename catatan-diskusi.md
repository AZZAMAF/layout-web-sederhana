# Catatan Diskusi Selasa - Layout Web Sederhana

## Tag HTML yang dipakai dan fungsinya

- `<!DOCTYPE html>` - deklarasi tipe dokumen HTML5.
- `<html lang="id">` - root dokumen, atribut lang menunjukkan bahasa Indonesia.
- `<head>` - metadata halaman (charset, viewport, title, link CSS).
- `<meta charset="UTF-8">` - set encoding karakter.
- `<meta name="viewport">` - agar layout responsif di perangkat mobile.
- `<title>` - judul tab browser.
- `<link rel="stylesheet">` - menyambungkan file CSS eksternal.
- `<body>` - isi halaman yang ditampilkan.
- `<header>` - bagian atas halaman (logo + nav).
- `<div class="logo">` - pembungkus logo (bukan semantik, untuk styling).
- `<nav>` - menu navigasi.
- `<a>` - tautan/hyperlink.
- `<main>` - konten utama halaman.
- `<section>` - bagian konten yang jelas terpisah (beranda, tentang, fitur).
- `<h1>`, `<h2>`, `<h3>` - judul/heading dengan hierarki.
- `<p>` - paragraf teks.
- `<footer>` - bagian bawah halaman (3 kolom).

## Properti CSS untuk menyusun header dan footer

Header:
- `display: flex` - membuat logo dan nav sejajar horizontal.
- `justify-content: space-between` - logo di kiri, nav di kanan.
- `align-items: center` - vertikal rata tengah.
- `position: sticky; top: 0` - header menempel saat scroll.

Footer:
- `display: flex` - membuat 3 kolom sejajar.
- `justify-content: space-between` - kolom tersebar merata.
- `flex-wrap: wrap` - kolom turun ke baris baru jika layar sempit.
- `flex: 1 1 200px` pada `.footer-col` - tiap kolom fleksibel dengan lebar minimum 200px.

## Kesulitan yang dihadapi dan cara mengatasinya

1. Logo dan nav tidak sejajar vertikal -> ditambah `align-items: center` pada `.header`.
2. Nav terlalu rapat di layar kecil -> ditambah `flex-wrap: wrap` dan media query.
3. Footer 3 kolom tidak rata di layar sempit -> ditambah `flex-wrap: wrap` dan `flex: 1 1 200px` pada kolom.
4. Warna teks header/footer sulit terbaca -> gunakan warna kontras (ink #0D1410, teks #F5F6F4) dan accent #15803D untuk tautan.