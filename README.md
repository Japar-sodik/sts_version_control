1. Jawaban:
- Menjaga kestabilan source code utama di branch main agar selalu bersih, aman, dan siap rilis/deploy tanpa takut ada error (production crash).
- Memudahkan proses code review melalui Pull Request, jadi anggota tim lain atau ketua bisa mengecek dan mengetes kodenya terlebih dahulu sebelum digabungkan.
- Mencegah konflik kode (merge conflict) langsung di branch utama jika beberapa anggota mengerjakan fitur berbeda secara bersamaan.
- Memudahkan pelacakan riwayat commit dan fitur jika sewaktu-waktu terjadi bug dan perlu di-rollback.

2. Jawaban:
1. Memastikan posisi ada di branch main dan kodenya paling update:
   git checkout main
   git pull origin main

2. Membuat branch fitur baru dan langsung berpindah ke branch tersebut:
   git checkout -b feature/mfa-auth

3. Memeriksa status perubahan file setelah koding:
   git status

4. Menambahkan seluruh perubahan file ke staging area:
   git add .

5. Menyimpan perubahan ke repository lokal dengan commit message terstruktur:
   git commit -m "feat: implementasi fitur autentikasi multi-faktor (mfa)"

6. Mengirim branch fitur baru ke remote repository (GitHub):
   git push -u origin feature/mfa-auth
   
