# Laporan Studi Kasus: Penerapan Feature Branch Workflow

## A. Keuntungan Utama Pembatasan Branch `main`

1. **Menjaga Stabilitas Sistem (Production Stability):** Mencegah kode yang belum selesai atau _error_ merusak sistem utama yang sedang berjalan.
2. **Keamanan Kolaborasi:** Memungkinkan setiap anggota tim mengerjakan fitur spesifik secara terisolasi tanpa merusak pekerjaan anggota tim lainnya.
3. **Mekanisme _Code Review_:** Memastikan setiap perubahan kode diperiksa terlebih dahulu lewat Pull Request sebelum digabung.
4. **Kemudahan Pelacakan:** Mempermudah pencarian sumber masalah jika terjadi _error_, karena setiap fitur (seperti MFA) dikerjakan pada _branch_ terpisah.

## B. Daftar Perintah Git yang Digunakan

1. `git checkout -b jawaban-airlangga_xii_pplg_2` (Membuat dan beralih ke branch baru).
2. `git add M.Airlangga_XII_PPLG_2.md` (Menyimpan file ke staging area).
3. `git commit -m "docs: menambahkan jawaban studi kasus version control MFA"` (Menyimpan perubahan ke repositori lokal).
4. `git push origin jawaban-airlangga_xii_pplg_2` (Mengunggah branch fitur ke GitHub).
