1. Keuntungan utama nge-lock branch main:
Biar website yang udah live (lagi dipakai user) nggak tiba-tiba hancur atau error gara-gara ada kode baru yang masih nge-bug. Branch main itu ibarat versi final yang harus selalu stabil dan aman. Dengan ngerjain di branch terpisah, kode kita bisa dites dan di-review dulu sama tim. Kalau udah bener-bener aman, baru deh digabungin.

2. Urutan perintah Git-nya:
Nah, karena kita mau bikin fitur MFA di branch terpisah, ini urutan command Git dari awal sampai siap di-review:

Pertama, bikin branch baru khusus fitur ini dan langsung pindah ke branch-nya:
git checkout -b fitur-mfa

Setelah kamu selesai coding fitur MFA-nya, tambahin semua file yang berubah biar siap disimpan:
git add .

Simpan progres di komputer lokalmu dan kasih pesan yang jelas:
git commit -m "menambahkan fitur autentikasi MFA"

Terakhir, kirim branch ini ke GitHub biar bisa dibikin Pull Request dan di-review sama ketua tim:
git push -u origin fitur-mfa