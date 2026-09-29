# Jawaban Studi Kasus: Penerapan Fitur Baru (Feature Branch Workflow)

## 1. Keuntungan Utama Pembatasan Branch Main
* **Menghindari Production Crash:** 
Mencegah kode yang belum stabil atau memiliki *bug* langsung masuk ke sistem utama yang sedang berjalan.
* **Mendukung Code Review:** 
Memungkinkan tim meninjau perubahan kode melalui *Pull Request* sebelum digabungkan (*merge*).
* **Kolaborasi yang Aman:** 
Memungkinkan developer bekerja secara bersamaan pada fitur berbeda tanpa mengganggu stabilitas kode utama.
* **Pelacakan Riwayat yang Jelas:** 
Mempermudah pelacakan perubahan kode spesifik per fitur jika terjadi kesalahan (*debugging*).

## 2. Perintah Git yang Digunakan
Berikut adalah rangkaian perintah Git mulai dari membuat branch fitur, menyimpan progres, hingga mengirimkannya ke GitHub:

```bash
# 1. Pindah ke branch main dan perbarui ke versi terbaru
git checkout main
git pull origin main

# 2. Membuat dan berpindah ke branch baru sesuai format
git checkout -b jawaban-[nama-siswa_kelas]

# 3. Mengecek status file yang telah dibuat atau diubah
git status

# 4. Menambahkan file ke staging area
git add .

# 5. Menyimpan progres lokal dengan pesan commit terstruktur
git commit -m "feat: menambahkan jawaban studi kasus autentikasi multi-faktor"

# 6. Mengirimkan branch ke repository remote di GitHub
git push origin jawaban-[nama-siswa_kelas]