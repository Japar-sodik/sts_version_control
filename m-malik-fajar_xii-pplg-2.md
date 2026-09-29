\# Jawaban STS Version Control



Nama: M. Malik Fajar

Kelas: XII PPLG 2



1\. Keuntungan Pembatasan Branch Main



Keuntungan utamanya adalah branch main menjadi lebih aman dan stabil karena anggota tim tidak bisa langsung memasukkan perubahan ke dalamnya. Setiap fitur baru dikerjakan di branch terpisah, kemudian diperiksa terlebih dahulu melalui Pull Request. Dengan begitu, kesalahan pada fitur baru tidak langsung mengganggu website yang sedang berjalan.



2\. Perintah Git yang digunakan:



\-git checkout -b fitur-mfa

\-git add .

\-git commit -m "Menambahkan fitur MFA"

\-git push -u origin fitur-mfa



Setelah itu, branch fitur-mfa sudah ada di GitHub dan bisa dibuat Pull Request untuk diperiksa.

