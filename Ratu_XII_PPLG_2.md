Jawaban Studi Kasus: Feature Branch Workflow



Nama  : Ratu ritz calton kalendara 

Kelas : XII PPLG 2



1\. Keuntungan Pembatasan Branch main



\- Menjaga stabilitas: branch main hanya berisi kode yang sudah teruji, sehingga website UMKM tidak crash.

\- Ada proses review: setiap perubahan harus lewat Pull Request agar bug ketahuan sebelum digabung.

\- Kerja tim lebih aman: anggota mengerjakan fitur masing-masing tanpa saling menimpa.

\- Riwayat rapi: mudah melacak siapa mengubah apa dan mudah rollback jika ada masalah.



2\. Perintah Git untuk Fitur MFA



git checkout main

git pull origin main

git checkout -b feature/mfa-authentication

git add .

git commit -m "feat: tambah autentikasi multi-faktor (MFA)"

git push -u origin feature/mfa-authentication



Setelah itu, buat Pull Request dari feature/mfa-authentication ke main agar ditinjau ketua tim.

