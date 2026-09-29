# STS Mahfuza Zahirah-XII_PPLG-1

Mahfuza Zahirah
XII-PPLG1
1. Keuntungan utamaa pembatasan Branch main
   mencegah terjadinya sistem error karena kode yg blum selesai
   memudahkan code review memastikan kode ditinjau oleh ktua tim atau rekan tim melalui Reques sblum digabungkan
   pengembangan bisa fokus membuat fitur baru dib branch terpisah tanpa ganggu tim lain.

2. membuat dan berpindah ke branch baru
   git checkout -b feature/autentikasi-mfa

   Menambahkan perubahan ke staging area
   git add.

   menyimpan progres lokal dengan pesan commit
   git commit -m "feat: menambahkan fitur Autentikasi Multi-faktor (MFA)"

   Mengirimkan branch ke GitHub agar bisa ditinjau lewat Pull Request
   git push origin feature/autentikasi-mfa
