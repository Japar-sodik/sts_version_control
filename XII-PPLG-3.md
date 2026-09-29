# Version Control
## Penerapan Fitur Baru (Feature Branch Workflow)

### 1. Keuntungan membatasi branch main

Menurut saya, pembatasan branch main berguna untuk menjaga agar kode yang belum selesai atau masih memiliki error tidak langsung masuk ke branch utama. Dengan begitu, risiko website mengalami error atau crash saat digunakan bisa dikurangi.

Selain itu, anggota tim bisa mengerjakan fitur masing-masing di branch yang berbeda. Setelah selesai, hasilnya bisa diperiksa terlebih dahulu melalui Pull Request sebelum digabungkan ke branch main.

### 2. Perintah Git yang digunakan

Berikut perintah Git yang digunakan mulai dari membuat branch fitur, menyimpan perubahan, sampai mengirim branch ke GitHub:

```bash
git checkout -b fitur-mfa
git status
git add .
git commit -m "feat: tambah fitur autentikasi multi-faktor"
git push -u origin fitur-mfa