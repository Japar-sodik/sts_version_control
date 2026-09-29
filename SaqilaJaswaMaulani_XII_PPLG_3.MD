1. Keuntungan pembatasan branch main
Menurut saya, keuntungan dari branch main yang tidak boleh dipakai utuk commit langsung adalah supaya kode utama tidak gampang error. Kalo ada anggota yang sedang membuat fitur baru, sebaiknya membuat branch sendiri terlebih dahulu. Jadi kalo ternyata fiturnya masih ada kesalahan, tidak langsung mengganggu kode yg ada di main. Selain itu, perubahan bisa dicek dan dilihat dulu melalui pull request sebelum digabungkan ke main. Dengan cara ini kemungkinan website mengalami error atau production crash bisa dikurangi

2. perintah git yang digunakan
clone repository dari github
https://github.com/saqilajaswaam-lalalaniie/sts_version_control.git
masuk ke folder repo
cd sts_version_control
membuat branch baru
git switch -c jawaban-SaqilaJaswaMaulani_XIIPPLG3
mengecek branch yang sedang digunakan
git branch
mengisi jawaban lalu cek perubahan
git status
menambahkan file ke staging
git add .
membuat commit
git commit -m "Menambahkan jawaban STS version control"
mengirim branch ke github
git push -u origin jawaban-SaqilaJaswaMaulani_XIIPPLG3

setelah berhasil dipush, saya membuka repository di github lalu membuat pull Request ke repository utama milik guru. dengan begitu, jawaban saya bisa diperiksa terlebih dahulu sebelum digabungkan ke branch main.