# Jawaban Ujian KK-2 PPLG

## Studi Kasus Version Control

### 1. Keuntungan Pembatasan Branch Main

Keuntungan utama dari pembatasan branch `main` adalah menjaga kestabilan kode utama agar tidak langsung terkena perubahan yang belum diuji.

Setiap anggota tim mengerjakan fitur pada branch masing-masing. Setelah selesai, perubahan dapat diperiksa dan ditinjau melalui Pull Request sebelum digabungkan ke branch utama.

Dengan cara ini, risiko terjadinya error dan production crash dapat dikurangi serta proses pengembangan menjadi lebih aman dan terorganisir.

### 2. Perintah Git

Berikut perintah Git yang digunakan mulai dari membuat branch fitur, menyimpan progres, hingga mengirim branch ke GitHub:

```bash
git checkout -b MuhamadDavinIlham_XII_PPLG_1
git status
git add MuhamadDavinIlham_XII_PPLG_1.md
git commit -m "feat: menambahkan jawaban studi kasus MFA"
git push -u origin MuhamadDavinIlham_XII_PPLG_1