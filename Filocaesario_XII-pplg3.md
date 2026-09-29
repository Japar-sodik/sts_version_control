Laporan Studi Kasus: Penerapan Feature Branch Workflow

Nama: Filocaesario  

Kelas:XII-PPLG 3  

Studi Kasus:Penerapan Fitur Autentikasi Multi-faktor (MFA)



\---



1\. Keuntungan Utama Pembatasan Branch Main

Menjamin Stabilitas Sistem Produksi (Production Safety): Mencegah kode eksperimental, belum teruji, atau berpotensi merusak langsung masuk ke branch utama aplikasi operasional UMKM.

Standarisasi Peninjauan Kode (Code Review):\*\* Mewajibkan setiap kode baru diperiksa dan disetujui melalui Pull Request sebelum dapat diintegrasikan.

Otomasi Pengujian Mutu (CI/CD):Memastikan pipeline otomatis (pengujian unit, integrasi, dan linter) lulus sebelum penggabungan kode disetujui.

Mencegah Kerusakan Riwayat Git:Melindungi branch dari tindakan destruktif seperti penimpaan riwayat secara paksa (`git push --force`) atau penghapusan branch secara tidak sengaja.

Pemisahan Tanggung Jawab (Isolation):Memungkinkan pengembang bekerja secara terisolasi pada fitur masing-masing tanpa mengganggu sistem utama.



\---



\### 2. Seluruh Perintah Git Penerapan Fitur Baru (MFA)



```bash

\# 1. Memastikan branch main lokal sinkron dengan remote

git checkout main

git pull origin main



\# 2. Membuat dan langsung berpindah ke branch fitur baru

git checkout -b feat/mfa-authentication



\# (Lakukan pengerjaan kode/fitur MFA di teks editor)



\# 3. Memeriksa status file yang telah diubah atau ditambahkan

git status



\# 4. Memasukkan seluruh perubahan file ke Staging Area

git add .



\# 5. Menyimpan perubahan secara berkala dengan format Conventional Commits

git commit -m "feat(auth): implement core logic for multi-factor authentication"



\# 6. Mengirim (push) branch fitur ke remote repository di GitHub

git push -u origin feat/mfa-authentication

