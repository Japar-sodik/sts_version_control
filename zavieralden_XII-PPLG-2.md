1.alasan branch main dibatasi

Branch main sebaiknya hanya berisi kode yang sudah selesai dan sudah melalui pengecekan. Pembatasan ini dilakukan agar:



\-Mengurangi risiko error, karena kode yang belum selesai tidak langsung masuk ke versi utama website.

\- Menjaga keamanan, terutama karena fitur MFA berkaitan dengan proses login dan keamanan akun pengguna.

\- Memudahkan kerja tim, karena setiap anggota dapat mengembangkan fitur masing-masing tanpa mengganggu pekerjaan anggota lain.

\- Mempermudah proses review, karena perubahan dapat diperiksa terlebih dahulu melalui pull request sebelum digabungkan ke main.

\- Memudahkan perbaikan jika terjadi masalah, karena setiap perubahan tercatat dalam riwayat Git.



2\. Langkah dan Perintah Gitbash

\# Pindah ke branch main

git checkout main



\# Mengambil perubahan terbaru dari repository

git pull origin main



\# Membuat branch khusus untuk fitur MFA

git checkout -b feature/mfa



\# Setelah selesai mengerjakan fitur, cek perubahan

git status



\# Menambahkan file yang telah diubah

git add .



\# Membuat commit

git commit -m "Menambahkan fitur MFA"



\# Mengirim branch ke GitHub

git push -u origin feature/mfa





Setelah branch berhasil dikirim ke GitHub, anggota tim dapat membuat Pull Request dari branch feature/mfa menuju main. Selanjutnya perubahan diperiksa oleh ketua atau anggota tim lain. Jika tidak ditemukan masalah, Pull Request dapat di-merge ke branch main.

