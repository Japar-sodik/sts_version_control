Jawaban sts Version Control

1. Keuntungan Utama Pembatasan Branch main

Pembatasan branch main membuat kode utama lebih aman karena anggota tim tidak bisa langsung memasukkan perubahan yang belum diuji setiap fitur dikerjakan di branch terpisah, kemudian ditinjau dan diuji melalui Pull Request sebelum digabungkan ke main hal ini dapat mengurangi risiko error.

2. Perintah Git Feature Branch Workflow

- Pindah ke branch main dan mengambil versi terbaru
git checkout main
git pull origin main

- Membuat branch khusus untuk fitur MFA
git checkout -b feature/mfa

- Mengecek perubahan yang sudah dilakukan
git status

- Menambahkan perubahan ke staging
git add .

- Menyimpan progres dengan commit
git commit -m "Menambahkan fitur autentikasi MFA"

- Mengirim branch fitur ke GitHub
git push -u origin feature/mfa