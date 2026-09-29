## 1. Keuntungan Pembatasan Branch Main
Keuntungan utama membatasi branch `main` adalah untuk mencegah terjadinya production crash atau sistem error. Dengan melarang commit langsung ke branch `main`, setiap kode atau fitur baru yang dibuat oleh anggota tim harus dicek dan di-review terlebih dahulu melalui Pull Request. Hal ini dilakukan agar kode di server utama tetap stabil, aman, dan meminimalisir masuknya bug sebelum benar-benar digabungkan.

## 2. Perintah Git untuk Fitur MFA
Sesuai dengan skenario pembuatan fitur Autentikasi Multi-faktor (MFA), dan di bawah ini adalah urutan perintah Git yang digunakan dari awal hingga siap di-review:

1. Membuat branch baru khusus fitur MFA sekaligus pindah ke branch tersebut:
`git checkout -b fitur-mfa`

2. Menyimpan semua perubahan file ke staging area:
`git add .`

3. Menyimpan progres di lokal dengan pesan commit yang terstruktur:
`git commit -m "feat: menambahkan fitur autentikasi MFA"`

4. Mengirim branch fitur tersebut ke repository GitHub agar siap ditinjau lewat Pull Request:
`git push -u origin fitur-mfa`