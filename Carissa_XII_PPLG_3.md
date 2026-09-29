
1. Keuntungan pembatasan branch main
Branch main itu isinya kode yang dipakai di sistem asli. Kalau semua anggota bisa commit langsung ke main, kode yang belum dites bisa bikin website error. Jadi fitur dikerjakan di branch sendiri dulu, terus digabung lewat Pull Request setelah dicek tim. Dengan begitu main tetap stabil dan aman.

2. Perintah git
git clone https://github.com/carissa2009hs/sts_version_control.git
cd sts_version_control
git checkout -b jawaban-carissa_XII-PPLG-3
git add .
git commit -m "feat: menambahkan fitur autentikasi multi-faktor (MFA)"
git push origin jawaban-carissa_XII-PPLG-3
Setelah push, buka GitHub lalu klik Compare & pull request untuk mengajukan Pull Request ke repo guru.