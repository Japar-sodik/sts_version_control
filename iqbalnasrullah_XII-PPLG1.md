\# 1. Keuntungan Utama Pembatasan Branch `main`



\- Mencegah sistem crash. Branch `main` dipakai untuk versi website yang sedang berjalan. Kalau anggota tim bebas commit ke sana, kode yang belum dites bisa bikin website UMKM error dan pelanggan tidak bisa mengaksesnya.

\- Ada tahap pengecekan. Setiap perubahan harus lewat Pull Request dulu, jadi ketua tim bisa membaca kodenya sebelum digabung. Ini penting buat fitur MFA karena berhubungan dengan keamanan akun.

\- Pekerjaan tidak bentrok. Setiap anggota mengerjakan fitur di branch masing-masing, jadi hasil kerja teman tidak tertimpa.

\- Gampang buat dilacak. Kalau ada masalah, riwayat perubahan lebih jelas dan mudah dikembalikan ke versi sebelumnya.



\# 2. Perintah Git yang Digunakan



```bash

1\. Pindah ke main dan update ke versi terbaru

git checkout main

Mengambil perubahan terbaru dari repository

git pull origin main



2\. Buat branch baru untuk fitur MFA

git checkout -b feature/mfa-authentication



3\. Kerjakan fitur MFA di editor, lalu cek perubahannya

git status



4\. Masukkan perubahan ke staging

git add .



5\. Simpan progres di lokal dengan pesan commit

git commit -m "feat: menambahkan fitur autentikasi multi-faktor (MFA)"



6\. Upload branch ke GitHub

git push -u origin feature/mfa-authentication



7\. Di GitHub, klik "Compare \& pull request", isi judul dan deskripsi, lalu klik "Create pull request" supaya bisa direview

