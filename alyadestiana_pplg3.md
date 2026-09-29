# Lembar Jawaban Soal Ujian KK-2 

## 1. Keuntungan Pembatasan Branch Main

Pembatasan branch main berguna untuk menjaga agar kode utama tetap aman dan stabil. 
Dengan menggunakan branch terpisah, setiap anggota tim dapat mengerjakan fitur atau 
perubahan tanpa mengganggu kode yang ada di branch main. Selain itu, penggunaan branch membuat proses kerja lebih teratur karena perubahan dapat diperiksa terlebih dahulu melalui Pull Request sebelum digabungkan ke branch main.

## 2. Perintah Git yang Digunakan

Pertama, saya melakukan clone repository dari GitHub ke komputer menggunakan perintah git clone. Setelah repository berhasil di-clone, saya masuk ke folder project menggunakan perintah cd. Selanjutnya, saya membuat branch baru dengan nama jawaban-alyadestiana_pplg3 agar pengerjaan tugas tidak dilakukan langsung pada branch main. Setelah membuat file alyadestiana_pplg3.md dan mengisi jawaban di dalamnya, saya mengecek perubahan menggunakan git status. Kemudian file tersebut ditambahkan ke staging menggunakan git add. Setelah itu, saya menyimpan perubahan dengan melakukan commit menggunakan pesan:
git commit -m "docs: tambah jawaban tugas"
Selanjutnya, branch yang sudah dibuat dikirim ke GitHub menggunakan:
git push -u origin jawaban-alyadestiana_pplg3

Setelah berhasil di-push ke GitHub, saya membuat Pull Request dari branch tersebut menuju branch main pada repository utama agar jawaban dapat ditinjau oleh guru.