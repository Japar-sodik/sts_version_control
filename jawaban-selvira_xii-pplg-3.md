  
### 1. Keuntungan Utama dari Pembatasan Branch Main
Keuntungan utamanya itu buat jaga-jaga supaya aplikasi utama yang lagi jalan (*production*) gak tiba-tiba error atau *crash* gara-gara kode yang belum fix. Karena commit ke main dilarang, kita jadi wajib bikin *Pull Request*, otomatis kode kita bakal dicek dan di review dulu sama ketua tim atau teman yang lain sebelum digabungin. Selain itu, kerja kelompok juga jadi lebih aman soalnya kita bisa ngoding bareng-bareng di branch masing-masing tanpa takut kodenya saling bentrok atau ketimpa.

### 2. Urutan Perintah Git untuk Fitur MFA
```bash
# 1. Membuat branch fitur terpisah dan berpindah ke branch tersebut
git checkout -b feature/mfa

# 2. Menyimpan progres lokal (memasukkan file ke staging area)
git add .

# 3. Menyimpan perubahan secara permanen dengan pesan yang terstruktur
git commit -m "feat: menambahkan fitur Autentikasi Multi-faktor (MFA)"

# 4. Mengirimkan branch fitur ke repository GitHub agar siap ditinjau (Pull Request)
git push -u origin feature/mfa
```
