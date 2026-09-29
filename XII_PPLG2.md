Version Control

Nama: Muhammad Revan Arista  
Kelas: XII PPLG 2

 1. Keuntungan membatasi branch main

Membatasi anggota agar tidak melakukan commit langsung ke branch main berguna untuk menjaga kode utama tetap aman setiap fitur baru dikerjakan di branch terpisah terlebih dahulu

Setelah selesai, hasil pekerjaan dapat diperiksa melalui Pull Request sebelum digabungkan ke branch main

2. Perintah Git yang digunakan

Pertama, melakukan clone repository:

bash
git clone https://github.com/unseulbutr/sts_version_control.git
cd sts_version_control
Membuat branch baru untuk mengerjakan fitur:
git checkout -b jawaban-MuhammadRevanArista_XIIPPLG2
Mengecek perubahan yang sudah dibuat:git status
Menambahkan file jawaban:git add XII_PPLG2.md
Menyimpan perubahan dengan commit:git commit -m "feat: menambahkan jawaban STS"
Mengirim branch ke GitHub:git push -u origin jawaban-MuhammadRevanArista_XIIPPLG2
