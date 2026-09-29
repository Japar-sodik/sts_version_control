## 1. Alasan Utama Membatasi Branch Main
Tujuan utama melarang commit langsung ke branch `main` adalah untuk menjaga keamanan dan kestabilan website yang sedang berjalan. Branch `main` ibarat versi final yang siap dipakai oleh klien. Kalau semua orang bebas memasukkan kode ke sana, risiko terjadinya *error* atau web *down* (*production crash*) sangat besar karena kodenya belum diuji coba. Dengan adanya pembatasan ini, setiap pekerjaan baru wajib melewati proses Pull Request agar bisa dicek dan di-*review* dulu kelayakannya oleh tim sebelum digabung ke kode utama.

## 2. Urutan Perintah Git untuk Pembuatan Fitur MFA
Skenarionya adalah membuat fitur Autentikasi Multi-faktor. Berikut adalah langkah-langkah *command* Git yang dieksekusi:

1. Membuat branch khusus untuk pengerjaan fitur tersebut dan langsung berpindah ke dalamnya:
`git checkout -b fitur-mfa`

2. Memasukkan semua perubahan file yang baru saja dikerjakan agar siap di-commit (*staging*):
`git add .`

3. Menyimpan riwayat perubahan di komputer lokal dengan pesan commit yang jelas:
`git commit -m "feat: membuat sistem autentikasi multi-faktor"`

4. Mengirim branch tersebut ke GitHub agar selanjutnya bisa diajukan untuk tahap Pull Request:
`git push -u origin fitur-mfa`