Nama: M. Aqilla Kesuma



Kelas: XII-PPLG 3



Studi Kasus: Pengembangan Fitur Autentikasi Multi-faktor (MFA)



1\. Keuntungan Utama Pembatasan Branch Main

Pembatasan direct push ke branch main (Branch Protection Rules) merupakan standar industri yang krusial bagi keberlangsungan proyek perangkat lunak, dengan keuntungan utama sebagai berikut:



Menjamin Ketersediaan Layanan Bisnis (Zero Downtime): Branch main berfungsi sebagai representasi langsung (production environment) dari website UMKM yang diakses oleh pelanggan setiap hari. Pembatasan ini mencegah masuknya kode setengah matang (untested/work-in-progress code) yang dapat memicu crash dan menghentikan transaksi operasional UMKM.



Filter Keamanan dan Standarisasi Kode (Quality \& Security Gate): Fitur sensitif seperti Autentikasi Multi-faktor (MFA) memerlukan pengawasan ketat. Melalui kewajiban Pull Request, ketua tim dan rekan pengembang dapat membedah logika kode, memverifikasi tidak adanya kebocoran celah keamanan (security vulnerability), serta memastikan arsitektur kode mematuhi standar tim.



Isolasi Fitur yang Memudahkan Mitigasi Masalah: Mengerjakan fitur di cabangnya sendiri memisahkan siklus hidup fitur tersebut dari sistem inti. Apabila fitur MFA mengalami kegagalan fungsi saat pengujian, cabang fitur dapat dibatalkan atau ditunda tanpa mengganggu jadwal peluncuran fitur lain yang sudah siap rilis.



Meminimalisir Konflik Kode yang Kompleks (Merge Conflict): Karena branch main hanya menerima kode yang telah diverifikasi dan disetujui, alur penggabungan antar-fitur yang dikerjakan oleh anggota tim yang berbeda menjadi lebih terstruktur dan tidak saling menimpa secara acak.



2\. Rangkaian Perintah Git Pengembangan Fitur MFA

Berikut adalah seluruh perintah Git yang dijalankan di terminal lokal, mulai dari sinkronisasi branch, isolasi fitur, pencatatan perubahan, hingga pengunggahan ke GitHub:



Bash

\# 1. Pastikan branch utama lokal berada di versi paling mutakhir dari remote

git checkout main

git pull origin main



\# 2. Buat dan langsung beralih ke branch baru khusus fitur MFA

\# (Dapat menggunakan perintah 'git switch -c' atau 'git checkout -b')

git switch -c feat/mfa-authenticator-flow



\# --- \[Proses penulisan kode fitur autentikasi MFA di editor] ---



\# 3. Periksa status berkas untuk memastikan file mana saja yang berubah

git status



\# 4. Daftarkan seluruh file yang telah dimodifikasi ke Staging Area

git add -A



\# 5. Buat commit terstruktur yang menjelaskan fungsionalitas yang ditambahkan

git commit -m "feat(security): integrasi modul validasi MFA dan verifikasi kode OTP"



\# 6. Unggah branch fitur ke repositori remote di GitHub

git push -u origin feat/mfa-authenticator-flow

