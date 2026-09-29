keuntungan pembatasan branch main membuat kode utama lebih aman karena anggota tim tidak bisa langsung memasukkan perubahan yang belum diuji. Setiap fitur dikerjakan di branch terpisah, kemudian ditinjau dan diuji melalui Pull Request sebelum digabungkan ke main. Hal ini dapat mengurangi risiko error atau production crash.
git checkout main
git pull origin main
git checkout -b jawaban-rizkyputrahadiatama-xiipplg2
git status
git add .
git commit -m "Menambahkan jawaban studi kasus version control Rizky Putra Hadiatama"
git push -u origin jawaban-rizkyputrahadiatama-xiipplg2