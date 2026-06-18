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
