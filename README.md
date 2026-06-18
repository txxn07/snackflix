# 🍿 SnackFlix TianTiwi

**Sistem Pemesanan Makanan & Minuman Cinema Room Berbasis Web**

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-gold.svg)
![Platform](https://img.shields.io/badge/platform-Web%20Mobile-brightgreen.svg)

---

## 📋 Daftar Isi

- [Tentang Proyek](#tentang-proyek)
- [Fitur Utama](#fitur-utama)
- [Teknologi](#teknologi)
- [Struktur Proyek](#struktur-proyek)
- [Instalasi](#instalasi)
- [Konfigurasi](#konfigurasi)
- [Penggunaan](#penggunaan)
- [Panduan Deployment](#panduan-deployment)
- [Keamanan & Ketentuan](#keamanan--ketentuan)
- [Lisensi](#lisensi)
- [Kontak](#kontak)

---

## 🎯 Tentang Proyek

**SnackFlix TianTiwi** adalah aplikasi pemesanan makanan dan minuman berbasis web yang dirancang khusus untuk lingkungan cinema room. Aplikasi ini memungkinkan penonton untuk memesan snack dan minuman langsung dari perangkat mobile mereka tanpa perlu meninggalkan ruangan.

Sistem ini dibangun dengan fokus pada:
- **Kemudahan penggunaan** — antarmuka intuitif yang mudah digunakan
- **Keamanan transaksi** — sistem persetujuan dan verifikasi pemesanan
- **Efisiensi operasional** — mengurangi antrian dan meningkatkan layanan

---

## ✨ Fitur Utama

### 🎬 Halaman Utama
- **Now Playing Section** — menampilkan informasi film yang sedang tayang (judul, aktor, sutradara, durasi, genre)
- **Sinopsis Film** — popup detail film dengan poster resolusi tinggi
- **Slideshow Banner** — menampilkan 15 gambar menu makanan dan minuman

### 🍔 Menu Makanan
| Menu | Varian | Harga |
|------|--------|-------|
| **Mie Instan** | Ayam Bawang, Rendang, Ayam Geprek, Soto | Rp 6.000 |
| **Pentol** | Kuah / Bumbu Kacang | Rp 1.000/biji (min 5) |
| **Sosis Bakar** | Pedas, Mayo, Saus Tomat | Rp 6.000/pcs |
| **Popcorn** | Manis, Asin, Pedas, Keju | Rp 5.000 |

### 🥤 Menu Minuman
| Menu | Varian | Harga |
|------|--------|-------|
| **Teh Sisri** | 8 varian rasa | Rp 2.000 |
| **Marimas** | 11 varian rasa | Rp 3.000 |
| **Teh Jus Gula Batu** | 5 varian | Rp 2.000 |
| **Minuman Spesial** | Teh Tarik, Teh Solo, Chocolatos, Matcha, Vanilla Latte | Rp 4.000 |
| **Pop Ice** | 7 varian rasa | Rp 5.000 |

### 🛒 Sistem Keranjang
- **Grouping otomatis** — item dengan spesifikasi sama digabung
- **Edit inline** — ubah telur, pedas, bumbu, mayo, saus, hangat/dingin per item
- **Quantity control** — tambah/kurang jumlah langsung dari keranjang
- **Minimal order Pentol** — tidak bisa kurang dari 5 biji
- **Subtotal per kategori** — Mie, Snack, Minuman

### 💳 Sistem Pembayaran
- **QRIS** — scan QR code untuk pembayaran
- **Dana** — transfer via aplikasi Dana
- **GoPay** — transfer via aplikasi GoPay
- **SeaBank** — transfer via SeaBank
- **Bank BCA** — transfer via BCA Mobile/ATM
- **ShopeePay** — transfer via ShopeePay

### 📲 Integrasi WhatsApp
- Template pesan otomatis dengan format profesional
- Konfirmasi pemesanan langsung ke admin
- Format pesan mencakup: nama pemesan, daftar pesanan, total, metode pembayaran

### 🔐 Sistem Keamanan & Ketentuan
- **Input nama pemesan** — wajib diisi sebelum mengakses menu
- **Ketentuan pemesanan** — 6 poin ketentuan yang harus disetujui
- **Ceklis persetujuan** — tidak bisa lanjut tanpa menyetujui ketentuan
- **Deteksi harian** — ketentuan muncul kembali setiap hari atau jika nama berubah
- **Template pernyataan** — di WhatsApp mencakup pernyataan kesungguhan memesan
- **Sanksi pemesanan palsu** — penggantian 2x nilai total pesanan

---

## 🔧 Teknologi

| Teknologi | Keterangan |
|-----------|------------|
| **HTML5** | Struktur halaman |
| **CSS3** | Styling dengan CSS Variables & Flexbox/Grid |
| **JavaScript (Vanilla)** | Logika aplikasi tanpa framework |
| **LocalStorage API** | Penyimpanan data keranjang dan user |
| **Iconify API** | Icon SVG gratis untuk UI |
| **Google Fonts (Poppins)** | Tipografi modern |
| **TMDB Image API** | Gambar poster film |

---

## 📁 Struktur Proyek

```

snackflix-tiantiwi/
├── index.html              # File utama aplikasi
├── README.md               # Dokumentasi proyek
└── img/                    # Folder gambar (opsional)
├── popcorn.svg
├── mie.svg
├── drink.svg
├── sosis.svg
└── cart.svg

```

---
## 🚀 Instalasi

### Metode 1: Local File
1. Download file `index.html`
2. Buka langsung di browser (Chrome/Safari/Firefox)
3. Tidak memerlukan server

### Metode 2: Web Server
```bash
# Clone repository (jika menggunakan Git)
git clone https://github.com/username/snackflix-tiantiwi.git

# Atau copy file ke web server
cp index.html /var/www/html/

# Buka di browser
http://localhost/snackflix-tiantiwi/
```

Metode 3: GitHub Pages

1. Upload index.html ke repository GitHub
2. Aktifkan GitHub Pages di Settings
3. Akses via https://username.github.io/snackflix-tiantiwi/

---

⚙️ Konfigurasi

1. Nomor WhatsApp Admin

Edit di file index.html, cari 628XXXXXXXXXX dan ganti:

```javascript
window.open(`https://wa.me/6288905185901?text=...`, '_blank');
```

2. Gambar Slideshow

Edit array SLIDESHOW_IMAGES:

```javascript
const SLIDESHOW_IMAGES = [
  'URL_GAMBAR_1',
  'URL_GAMBAR_2',
  // ... 15 gambar
];
```

3. QR Code Pembayaran

Ganti URL placeholder di setiap fungsi pembayaran:

```javascript
<img src="https://placehold.co/400x400/white/000?text=QRIS+CODE" alt="QRIS">
// Ganti dengan URL QR code asli
```

4. Informasi Film

Edit objek currentMovie:

```javascript
const currentMovie = {
  title: "Judul Film",
  cover: "URL_POSTER_KECIL",
  poster: "URL_POSTER_BESAR",
  release: "2024",
  duration: "2 jam 7 menit",
  actor: "Nama Aktor",
  director: "Nama Sutradara",
  genre: "Action, Comedy",
  synopsis: "Sinopsis film..."
};
```

5. Harga Menu

Edit di fungsi addMie(), addPentol(), dll:

```javascript
const price = (q * 6000) + (e * 3000); // Mie
const price = q * 1000;                  // Pentol
const price = q * 6000;                  // Sosis
const price = q * 5000;                  // Popcorn
```

---

📱 Penggunaan

Alur Pengguna

1. Buka aplikasi → muncul modal input nama
2. Isi nama → klik "Lanjutkan"
3. Baca ketentuan → ceklis persetujuan → klik "Saya Setuju & Lanjutkan"
4. Pilih menu → tab Makanan atau Minuman
5. Pilih varian → atur jumlah → klik "Tambah"
6. Review keranjang → klik badge keranjang
7. Edit/hapus item → gunakan tombol ✎ atau ✕
8. Klik ORDER → pilih metode pembayaran
9. Konfirmasi → kirim pesan WhatsApp

Tips

· Keranjang disimpan otomatis di browser
· Refresh halaman akan mereset keranjang
· Pentol minimal 5 biji per pesanan
· Item dengan varian sama akan otomatis digabung

---

🌐 Panduan Deployment

Netlify (Gratis)

1. Buat akun di netlify.com
2. Drag & drop folder proyek
3. Selesai — dapat URL publik

Vercel (Gratis)

1. Buat akun di vercel.com
2. Import repository atau upload file
3. Deploy otomatis

Hosting Berbayar

1. Upload via FTP ke public_html/
2. Akses via domain Anda

---

🔒 Keamanan & Ketentuan

Perlindungan Data

· Data pengguna disimpan di LocalStorage browser
· Tidak ada data yang dikirim ke server eksternal
· Data keranjang otomatis ter-reset saat browser di-refresh

Ketentuan Pemesanan

1. Layanan hanya untuk penonton yang benar-benar akan membeli
2. Dilarang membuat pesanan palsu atau iseng
3. Pesanan akan segera diproses oleh petugas
4. Pembatalan harus melalui WhatsApp sebelum diproses
5. Tombol "Saya Setuju" menyatakan itikad baik
6. Pemesanan palsu dikenakan sanksi 2x nilai total pesanan

Batasan

· Aplikasi berjalan sepenuhnya di client-side
· Tidak ada autentikasi server
· Cocok untuk penggunaan internal cinema room

---
📄 Lisensi

```
MIT License

Copyright (c) 2024 txxn

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

📞 Kontak

Kanal Detail
WhatsApp 62 889-0518-5901
Email txxn@snackflix.com
Instagram @snackflix.tiantiwi

---

🙏 Kredit

· Dikembangkan oleh: txxn
· Desain UI/UX: txxn
· Icon: Iconify
· Font: Google Fonts - Poppins
· Gambar Film: TMDB

---

<p align="center">
  <b>© 2024 SnackFlix TianTiwi. All rights reserved.</b><br>
  <sub>Made with ❤️ by <b>txxn</b></sub>
</p>
```
