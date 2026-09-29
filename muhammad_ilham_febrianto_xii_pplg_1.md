# Jawaban Soal Ujian KK-2 PPLG (Version Control)
**Nama:** Muhammad Ilham Febrianto  
**Kelas:** XII PPLG 1  

---

### 1. Keuntungan Utama Pembatasan Branch `main`
* **Menjaga Stabilitas Aplikasi (Production Stability):** Menghindari masuknya kode yang belum diuji (*untested code*) atau *bug/error* secara langsung ke lingkungan *production*, sehingga mencegah terjadinya kegagalan sistem (*system crash*).
* **Proses Review Kode Terstruktur (Code Review & Quality Control):** Memastikan setiap perubahan atau fitur baru ditinjau terlebih dahulu oleh ketua tim atau rekan tim melalui *Pull Request* (PR) sebelum digabungkan (*merge*).
* **Isolasi Fitur & Kolaborasi Lancar:** Setiap pengembang dapat bekerja pada fitur masing-masing di branch terpisah tanpa mengganggu pekerjaan pengembang lain atau merusak kode dasar proyek.

---

### 2. Alur Perintah Git yang Digunakan

```bash
# 1. Clone repository hasil fork ke lokal
git clone [https://github.com/muhammadilham21427-debug/sts_version_control.git](https://github.com/muhammadilham21427-debug/sts_version_control.git)

# 2. Masuk ke folder proyek
cd sts_version_control

# 3. Membuat dan berpindah ke branch fitur baru
git checkout -b jawaban-muhammad-ilham-febrianto-xii-pplg-1

# 4. Menambahkan file perubahan ke staging area
git add .

# 5. Menyimpan perubahan ke repository lokal (Commit)
git commit -m "feat: tambahkan jawaban studi kasus MFA dan version control"

# 6. Mengirimkan branch baru ke repository GitHub (Push)
git push -u origin jawaban-muhammad-ilham-febrianto-xii-pplg-1