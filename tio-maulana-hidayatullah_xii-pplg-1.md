1. Keuntungan Pembatasan Branch `main`

 Menjaga stabilitas sistem agar tidak *crash* di produksi.
 Memudahkan *code review* sebelum kode digabung.
 Mencegah konflik antar anggota tim saat bekerja paralel.

2.Perintah Git

bash
git checkout main
git pull origin main
git checkout -b jawaban-nama_kelas
git add .
git commit -m "feat: menambahkan jawaban studi kasus mfa"
git push origin jawaban-nama_kelas
