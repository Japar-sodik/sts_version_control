1. Keuntungan Utama Pembatasan Branch main 
•	Stabilitas Sistem: Mencegah kode yang rusak, bug, atau belum siap tayang masuk ke lingkungan produksi (live website UMKM).
•	Tinjauan Kode (Code Review): Memastikan anggota tim lain atau ketua tim dapat memeriksa kualitas dan keamanan kode (misalnya fitur MFA) melalui Pull Request (PR) sebelum digabungkan.
•	Isolasi Fitur: Pengembangan fitur baru tidak akan mengganggu anggota tim lain yang sedang bekerja di branch masing-masing.
2. Urutan Perintah Git (Feature Branch Workflow) 💻
Berikut alur perintah Git standar untuk mengerjakan fitur baru hingga siap di-review:
1.	Membuat dan berpindah ke branch fitur baru:
Bash
git checkout -b feature/mfa-authentication
2.	Memeriksa status perubahan file:
Bash
git status
3.	Menambahkan file yang diubah ke staging area:
Bash
git add .
4.	Menyimpan progres ke repository lokal (commit):
Bash
git commit -m "feat: add multi-factor authentication (MFA) feature"
5.	Mengirimkan branch fitur ke remote repository (GitHub):
Bash
git push -u origin feature/mfa-authentication
Setelah langkah ke-5, Anda tinggal membuka repository di GitHub dan membuat Pull Request (PR) ke branch main
