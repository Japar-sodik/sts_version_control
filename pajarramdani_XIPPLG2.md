markdown
### keuntungan utama pembatasan branch main
- kode di branch utama tetap aman, stabil, dan ga gampang error
- mencegah programmer push kode langsung tanpa izin atau ga sengaja
- mewajibkan kode ditinjau bareng-bareng lewat pull request sebelum digabung


### perintah git (step by step)

# 1. pindah ke main dan update kode terbaru dari github

git checkout main
git pull origin main

# 2. buat dan pindah ke branch fitur baru

git checkout -b fitur-baru

# 3. masukkan semua file perubahan ke staging

git add .

# 4. simpan perubahan ke commit lokal

git commit -m "menambahkan fitur baru"

# 5. kirim branch baru ke github

git push -u origin fitur-baru

