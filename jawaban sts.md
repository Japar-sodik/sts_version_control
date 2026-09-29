# sts_version_control

1. Keuntungan utamanya yaitu mengurangi risiko website error atau rusak. Jadi, anggota tim tidak bisa langsung mengubah kode yang ada di main.

Setiap fitur baru dibuat di branch sendiri, lalu dicek dan ditinjau terlebih dahulu sebelum digabung ke main.

Dengan cara ini, kalau fitur MFA ternyata masih ada error, branch main tetap aman dan website yang sedang digunakan tidak ikut bermasalah.

1. git checkout main
2. git pull origin main
3. git checkout -b feature/mfa
4. git branch
5. git status
6. git add .
7. git commit -m "Menambahkan fitur autentikasi MFA"
8. git push -u origin feature/mfa
