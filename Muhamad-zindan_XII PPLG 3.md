# Jawaban Studi Kasus - Feature Branch Workflow (MFA)

**Nama:** Muhamad Zindan  
**Kelas:** XII PPLG 3  

---

### 1. Keuntungan Utama Pembatasan Branch Main
* **Mencegah Production Crash:** Menjaga agar kode yang belum teruji atau mengandung bug tidak langsung merusak sistem utama yang sedang berjalan secara live.
* **Memastikan Review Kode (Quality Control):** Memaksa seluruh perubahan kode diperiksa terlebih dahulu oleh tim/ketua lewat *Pull Request* (PR) sebelum digabungkan.
* **Pengembangan Terisolasi:** Setiap pengembang dapat mengerjakan fitur baru tanpa khawatir mengganggu atau bentrok dengan pekerjaan anggota tim lainnya.
* **Riwayat Commit yang Terstruktur:** Menjaga riwayat (*history*) pada branch `main` tetap bersih, stabil, dan mudah ditelusuri jika terjadi masalah.

---

### 2. Seluruh Perintah Git yang Digunakan

Berikut adalah urutan perintah Git dari membuat branch fitur hingga siap ditinjau lewat PR:

1. **Membuat dan berpindah ke branch fitur baru (MFA):**
   ```bash
   git checkout -b feature/autentikasi-mfa