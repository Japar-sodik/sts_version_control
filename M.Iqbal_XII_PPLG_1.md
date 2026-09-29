1. Keuntungan Utama Pembatasan Branch Main
Keuntungan utamanya adalah menjaga kestabilan sistem operasional mencegah production crash. Dengan melarang commit langsung ke branch main, tim memastikan bahwa:
- Branch main selalu berisi source code final yang bersih, stabil, dan siap deploy.
- Setiap fitur baru wajib dikerjakan di branch terpisah, sehingga tidak mengganggu jalannya sistem utama jika terjadi error.
- Setiap kode yang akan masuk ke main harus melalui proses peninjauan (code review melalui Pull Request) dan pengujian (testing) terlebih dahulu.
- Mencegah terjadinya konflik kode (merge conflict) akibat beberapa developer yang mengubah file yang sama secara bersamaan.

2. Perintah Git untuk Feature Branch Workflow
Berikut adalah urutan perintah Git dari pembuatan branch hingga pengiriman ke GitHub:

Langkah 1: Membuat dan langsung berpindah ke branch fitur baru
git checkout -b feature/mfa

Langkah 2: Menambahkan semua perubahan file ke staging area
git add .

Langkah 3: Menyimpan progres secara lokal dengan pesan commit terstruktur
git commit -m "feat: menambahkan fitur autentikasi multi-faktor (MFA)"

Langkah 4: Mengirimkan branch fitur lokal ke repository GitHub (remote)
git push -u origin feature/mfa