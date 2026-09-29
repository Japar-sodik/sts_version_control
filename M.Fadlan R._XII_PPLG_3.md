# Jawaban STS Version Control

## 1. Keuntungan Utama Pembatasan Branch Main
* **Menjaga Stabilitas Sistem:** Menjaga branch main tetap stabil dan bebas bug, sehingga website tidak pernah mengalami crash saat diakses pengguna.
* **Memudahkan Code Review:** Tim bisa memeriksa dan menguji kode baru terlebih dahulu lewat Pull Request sebelum digabungkan ke main.
* **Mencegah Bentrok Kode:** Meminimalkan risiko merge conflict karena tiap anggota mengerjakan fiturnya di ruang terisolasi masing-masing.

## 2. Perintah Git Fitur Baru
```bash
# 1. Membuat dan berpindah ke branch fitur terpisah
git checkout -b feature/mfa-auth

# 2. Memeriksa status perubahan file
git status

# 3. Menambahkan semua perubahan ke staging area
git add .

# 4. Menyimpan progres perubahan ke lokal commit
git commit -m "feat: menambah fitur autentikasi multi-faktor (MFA)"

# 5. Mengirimkan branch fitur ke repository remote di GitHub
git push origin feature/mfa-auth