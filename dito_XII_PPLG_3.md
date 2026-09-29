# Jawaban STS Version Control

- **Nama:** Dito Arkhan Araffi
- **Kelas:** XII PPLG 3

1. Keuntungan utama pembatasan brench main bisa menjaga kestabilan sistem, Mengembangkan fitur tanpa takut bentrok, ada juga mekanisme review kode

2. - Pastikan branch utama lokal sinkron dengan yang terbaru
git checkout main
git pull origin main

setelah itu
git checkout -b feature/mfa-authentication

terus
git add .

kemudian
git commit -m "feat(auth): implementasi multi-factor authentication (MFA)"

setelahnya
git push -u origin feature/mfa-authentication