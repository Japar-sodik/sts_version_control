# Jawaban STS Version Control

## Studi Kasus: Pembuatan Website untuk UMKM

### 1. Masalah utama yang dihadapi UMKM

Masalah utama yang dihadapi UMKM tersebut adalah jangkauan pemasaran yang masih terbatas. Selama ini pelanggan hanya mengetahui produk dari lingkungan sekitar sehingga sulit mendapatkan pelanggan baru. UMKM juga belum memanfaatkan media digital sebagai sarana promosi dan penjualan.

### 2. Fitur yang sebaiknya terdapat dalam website UMKM

Fitur yang diperlukan dalam website UMKM antara lain:

- Halaman beranda yang berisi informasi usaha dan produk unggulan.
- Katalog produk yang menampilkan foto, nama produk, deskripsi, dan harga.
- Fitur pemesanan melalui website atau terhubung dengan WhatsApp.
- Informasi kontak seperti nomor telepon, WhatsApp, dan media sosial.
- Lokasi toko menggunakan Google Maps.
- Halaman profil usaha.
- Testimoni pelanggan.
- Tampilan responsif agar mudah digunakan melalui HP.

### 3. Pendekatan Management Project yang tepat

Pendekatan yang cocok digunakan adalah Waterfall karena kebutuhan dari klien sudah jelas sejak awal. Tahapan pengerjaan dapat dilakukan secara berurutan mulai dari analisis kebutuhan, desain, pembuatan website, pengujian, hingga pemeliharaan.

Dengan metode ini, setiap tahap dapat didokumentasikan sehingga memudahkan tim dalam mengembangkan website.

---

# Version Control

## 1. Keuntungan pembatasan branch main

Pembatasan branch main bertujuan menjaga kestabilan sistem utama. Developer tidak langsung memasukkan kode ke branch main sehingga risiko kesalahan atau kerusakan sistem dapat dikurangi.

Setiap fitur baru dibuat pada branch terpisah, kemudian dilakukan pengecekan melalui Pull Request sebelum digabungkan ke branch main.

## 2. Perintah Git yang digunakan

Membuat branch fitur:

```bash
git checkout -b fitur-mfa