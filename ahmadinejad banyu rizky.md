1.Agar branch main tetap aman dan tidak terganggu oleh perubahan yang belum diuji. Setiap fitur dikerjakan di branch sendiri, sehingga lebih mudah dicek, diperbaiki, dan direview sebelum digabung ke main

2.# Clone repository
git clone https://github.com/[username]/version_control.git
cd version_control

# Membuat branch fitur
git checkout -b fitur-mfa

# Membuat file jawaban
touch [nama_kelas].md

# Cek perubahan
git status

# Menambahkan file
git add [nama_kelas].md

# Commit
git commit -m "feat: menambahkan jawaban studi kasus MFA"

# Push ke GitHub
git push -u origin fitur-mfa