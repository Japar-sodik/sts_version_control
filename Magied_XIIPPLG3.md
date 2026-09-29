1. Keuntungan pembatasan branch main
Branch main menjadi lebih aman karena anggota tidak bisa langsung mengubah kode utama. fitur baru diuji dulu dengan pull request, sehingga resiko error lebih kecil

2. Perintah Git yang digunakan
-Clone repository
git clone https://github.com/Japar-sodik/sts_version_control.git
cd sts_version_control

- Membuat branch fitur
git checkout -b jawaban-[nama-siswa_kelas]

- Membuat dan mengerjakan file:
buat file [nama_kelas].md
lalu isi jawaban tugas di dalam file

- save perubahan
git status
git add .
git commit -m "feat: tambah autentikasi MFA"

- mengirim branch ke githup
git push -u origin jawaban-[nama-siswa_kelas]

- buka repository di GitHub, pilih branch yang dibuat, klik Compare & pull request, buat pull request ke branch main
