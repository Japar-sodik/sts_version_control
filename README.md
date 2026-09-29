HARUM ERILIA SUHANDI XII PPLG 3  

1. Apa keuntungan utama dari pembatasan branch main dalam tim pengembangan?
Jawaban:
Keuntungan utama pembatasan branch main adalah menjaga kode utama tetap aman dan stabil. Dengan menggunakan branch terpisah, fitur baru dapat dikerjakan dan diperiksa terlebih dahulu sebelum digabungkan ke branch main. Hal ini dapat mengurangi risiko kesalahan dan production crash.
2. Tuliskan seluruh perintah Git yang digunakan mulai dari membuat branch fitur terpisah, menyimpan progress lokal hingga mengirimkannya ke GitHub agar siap ditinjau melalui Pull Request.
Jawaban:
git switch -c jawaban-nama-siswa-kelas
git status
git add .
git commit -m "docs: add answer"
git push -u origin jawaban-nama-siswa-kelas
