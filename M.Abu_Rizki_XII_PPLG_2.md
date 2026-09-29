1. Keuntungan Utama Pembatasan Branch Main
Pembatasan commit langsung ke branch main memiliki beberapa keuntungan krusial bagi tim pengembang:

Stabilitas Sistem Operasional (Mencegah Crash): Branch main bertindak sebagai representasi dari versi produksi yang sedang berjalan (live). Dengan melarang direct commit, risiko memasukkan kode yang rusak (bug) secara tidak sengaja ke sistem operasional dapat dihindari.

Memaksa Adanya Code Review: Pembatasan ini mengharuskan developer menggunakan Pull Request (PR). Proses ini memberi ruang bagi lead atau anggota tim lain untuk memeriksa kualitas kode, logika, dan keamanan fitur baru (seperti MFA) sebelum digabungkan.

Kolaborasi Paralel yang Bersih: Anggota tim dapat bekerja pada fitur yang berbeda-beda secara bersamaan di branch masing-masing (terisolasi) tanpa khawatir pekerjaan mereka saling menimpa atau membuat konflik langsung di kode utama.

2. 
# 1. Clone repository yang sudah kamu fork ke komputer lokal
git clone https://github.com/username-github-kamu/sts_version_control.git

# Masuk ke dalam direktori proyek
cd sts_version_control

# 2. Membuat branch baru sesuai format tugas dan langsung pindah ke branch tersebut
git checkout -b M.Abu_Rizki_XII_PPLG_2

# 3. (Tahap ini membuat file M.Abu_Rizki_XII_PPLG_2.md di root folder dan mengisi jawaban)
touch M.Abu_Rizki_XII_PPLG_2.md

# 4. Menyimpan progres file yang baru dibuat ke staging area
git add .

# Menyimpan perubahan ke dalam versi lokal (commit) dengan pesan terstruktur
git commit -m "feat: Menambahkan jawaban studi kasus implementasi fitur MFA"

# Mengirimkan branch lokal beserta isinya ke repository GitHub milikmu (origin)
git push -u origin M.Abu_Rizki_XII_PPLG_2