1. Keuntungan Utama Pembatasan Branch `main`
* Mencegah Bug & Production Crash: Branch `main` tetap bersih dan stabil karena kode yang belum diuji tidak langsung bercampur di lingkungan produksi.
* Proses Review Kode (Code Review): Semua perubahan wajib melewati Pull Request (PR) terlebih dahulu agar ketua tim dapat meninjau kualitas kode dan keamanan.
* Isolasi Fitur: Setiap pengembang bekerja di area aman masing-masing. Jika terjadi kesalahan pada fitur MFA, branch `main` tidak terpengaruh.
* Histori Commit yang Rapi: Riwayat perubahan menjadi terstruktur dan memudahkan proses *rollback* jika terjadi masalah.

2. Perintah Git (Feature Branch Workflow - MFA)
```bash
# 1. Pindah ke branch main dan perbarui kode lokal
git checkout main
git pull origin main
# 2. Buat dan berpindah ke branch fitur baru
git checkout -b feature/multi-factor-authentication

# 3. Cek status perubahan
git status

# 4. Tambahkan file ke staging area
git add .

# 5. Simpan perubahan dengan pesan commit terstruktur
git commit -m "feat(auth): implementasi fitur Multi-Factor Authentication (MFA)"

# 6. Unggah branch fitur ke repositori remote (GitHub)
git push -u origin feature/multi-factor-authentication