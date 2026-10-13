JAWABAN:

================================================================================
NOMOR 1 — Keuntungan Utama dari Pembatasan Branch Main dalam Tim Pengembang
================================================================================

Dalam proyek akhir Pembuatan Website untuk UMKM, ketua tim melarang anggota
melakukan commit langsung ke branch main. Berikut keuntungan utamanya:

  1. Mencegah Production Crash
     ─────────────────────────
     Tidak seorang pun boleh langsung menulis kode ke branch main yang sudah
     berjalan di production. Cukup satu commit yang bermasalah, seluruh sistem
     operasional (website UMKM) bisa lumpuh. Dengan membatasi akses ke main,
     setiap perubahan harus melewati proses review terlebih dahulu.

  2. Menjaga Stabilitas Kode di Lingkungan Production
     ──────────────────────────────────────────────────
     Branch main mewakili kode yang sedang aktif digunakan oleh pengguna.
     Jika setiap anggota menulis langsung ke main, tidak ada yang mengawasi
     kualitas kode secara menyeluruh. Dengan demikian, potensi bug, error, atau
     bahkan kehilangan data dapat diminimalkan.

  3. Mewujudkan Pola Kerja Kolaboratif yang Teratur
     ────────────────────────────────────────────────
     Setiap fitur baru (seperti Autentikasi Multi-faktor / MFA) dikembangkan
     di branch fitur masing-masing. Artinya, работу распределены — tidak ada
     bentrok antar anggota. Setiap orang bekerja di branch terpisah, kemudian
     menggabungkan pekerjaannya melalui mekanisme Pull Request.

  4. Memungkinkan_code Review Sebelum Kode Masuk Production
     ───────────────────────────────────────────────────────
     Pull Request (PR) mewajibkan setiap perubahan ditinjau oleh minimal satu
     anggota tim lain. Ini adalah checkpoint kualitas terakhir sebelum kode
     benar-benar diterapkan. Tim dapat menemukan bug, menyarankan perbaikan,
     atau menolak perubahan yang belum layak.

  5. Memudahkan Pelacakan dan Pembalikan Perubahan (Rollback)
     ─────────────────────────────────────────────────────────
     Karena setiap commit di-main sudah terverifikasi dan tercatat rapi,
     jika terjadi masalah, tim dapat melacak siapa yang mengubah apa dan
     dengan mudah mengembalikan (revert) perubahan tanpa harus mencari-cari
     di antara puluhan commit acak.

  6. Mendukung Workflow Pengembangan Berkelanjutan (Git Flow)
     ─────────────────────────────────────────────────────────
     Dengan branch fitur → branch development → branch main, tim memiliki
     alur kerja yang jelas dan terstruktur. Setiap tahap pengembangan memiliki
     kualitas standar sendiri, sehingga质量问题 tidak menumpuk sampai ke
     lingkungan production.

KESIMPULAN:
  Branch main adalah "garis merah" dalam pengembangan perangkat lunak tim.
  Pembatasan commit langsung ke main memastikan bahwa setiap kode yang sampai
  ke production sudah melewati tahap pengembangan, pengujian, dan review yang
  должным образом. Ini adalah praktik standar dalam pengembangan perangkat
  lunak profesional, terutama untuk sistem yang menangani data dan operasional
  bisnis secara langsung.


================================================================================
NOMOR 2 — Seluruh Perintah Git dari Membuat Branch Fitur hingga Pull Request
================================================================================

Diketahui:
  • Fitur baru     : Autentikasi Multi-faktor (MFA)
  • Branch utama   : main
  • Repository     : remote (GitHub)

--------------------------------------------------------------------------------
LANGKAH 1 — Pastikan Branch Main Lokal Bersih dan Terbaru
--------------------------------------------------------------------------------
  git checkout main
  git pull origin main

  → Beralih ke branch main, lalu menarik perubahan terbaru dari remote.

--------------------------------------------------------------------------------
LANGKAH 2 — Membuat Branch Fitur Baru (Feature Branch)
--------------------------------------------------------------------------------
  git checkout -b fitur/mfa-autentikasi

  → Membuat branch baru bernama "fitur/mfa-autentikasi" dan langsung
    berpindah ke branch tersebut. Penamaan branch yang konsisten
    (misal: fitur/, fix/, hotfix/) membantu tim memahami jenis perubahan.

--------------------------------------------------------------------------------
LANGKAH 3 — Mengembangkan Fitur MFA
--------------------------------------------------------------------------------
  [Pada titik ini, anggota tim menulis kode fitur MFA pada file-file проекта.
   Setiap kali menyelesaikan satu tahap atau satu file, lakukan commit.]

--------------------------------------------------------------------------------
LANGKAH 4 — Menambahkan Perubahan ke Staging Area
--------------------------------------------------------------------------------
  git add .

  → Menambahkan semua file yang berubah ke staging area.
    Alternatif lain:
      git add nama-file.js       → menambahkan file tertentu saja
      git add *.js               → menambahkan semua file .js
      git add -A                 → menambahkan semua perubahan termasuk
                                   file yang dihapus

--------------------------------------------------------------------------------
LANGKAH 5 — Menyimpan Progres dengan Commit
--------------------------------------------------------------------------------
  git commit -m "feat: tambah komponen input OTP untuk MFA"

  → Menyimpan snapshot perubahan ke repository lokal.
    Format commit message yang baik:
      feat:  → fitur baru
      fix:   → perbaikan bug
      docs:  → perubahan dokumentasi
      style: → format kode, tidak mengubah logika
      refactor: → restrukturisasi kode tanpa mengubah fitur
      test:  → menambah atau memperbaiki tes

  Jika ingin menambahkan deskripsi lebih detail dalam satu baris:
  git commit -m "feat: tambah komponen input OTP untuk MFA" \
             -m "Menambahkan form verifikasi dua langkah dengan kode 6 digit."

--------------------------------------------------------------------------------
LANGKAH 6 — Menambahkan Commit Lainnya (Jika Diperlukan)
--------------------------------------------------------------------------------
  [Setelah menyelesaikan setiap bagian fitur MFA, ulangi LANGKAH 4 dan 5]

  git add .
  git commit -m "feat: tambah fungsi generate kode OTP"
  git add .
  git commit -m "feat: tambah endpoint verifikasi OTP di backend"
  git add .
  git commit -m "fix: perbaiki validasi input kode OTP"

--------------------------------------------------------------------------------
LANGKAH 7 — Sebelum Push, Selalu Sinkronkan dengan Branch Main
--------------------------------------------------------------------------------
  git checkout main
  git pull origin main
  git checkout fitur/mfa-autentikasi
  git merge main

  → Pastikan branch fitur tidak tertinggal dari branch main.
    Jika ada konflik saat merge, selesaikan secara manual, lalu:
      git add .
      git commit -m "merge: selesaikan konflik dengan main"

--------------------------------------------------------------------------------
LANGKAH 8 — Push Branch Fitur ke Repository Remote (GitHub)
--------------------------------------------------------------------------------
  git push origin fitur/mfa-autentikasi

  → Mengunggah branch lokal "fitur/mfa-autentikasi" ke repository remote
    di GitHub. Branch ini sekarang bisa dilihat oleh seluruh anggota tim.

--------------------------------------------------------------------------------
LANGKAH 9 — Membuka Pull Request (PR) di GitHub
--------------------------------------------------------------------------------
  Melalui GitHub (GUI):
    1. Buka repository di GitHub.
    2. Klik tombol "Compare & pull request" pada notifikasi branch baru.
    3. Pilih base branch: main  ←  compare branch: fitur/mfa-autentikasi
    4. Isi judul PR, misalnya: "feat: implementasi Autentikasi Multi-faktor"
    5. Tambahkan deskripsi yang menjelaskan:
         - Apa yang diubah
         - Mengapa perubahan ini diperlukan
         - Langkah pengujian yang dilakukan
    6. Assign reviewer (anggota tim lain yang bertanggung jawab me-review).
    7. Klik "Create pull request."

  Melalui CLI (GitHub CLI):
    gh pr create --base main --head fitur/mfa-autentikasi \
                  --title "feat: implementasi Autentikasi Multi-faktor" \
                  --body "Menambahkan fitur MFA untuk meningkatkan keamanan..."

--------------------------------------------------------------------------------
LANGKAH 10 — Setelah PR Disetujui dan Di-merge
--------------------------------------------------------------------------------
  git checkout main
  git pull origin main

  → Branch main lokal diperbarui dengan kode fitur MFA yang sudah
    di-merge oleh reviewer melalui GitHub.


================================================================================
RINGKASAN PERINTAH GIT SECARA KESELURUHAN
================================================================================

  1.  git checkout main
  2.  git pull origin main
  3.  git checkout -b fitur/mfa-autentikasi
  4.  [mengembangkan fitur MFA...]
  5.  git add .
  6.  git commit -m "feat: tambah komponen input OTP untuk MFA"
  7.  [ulangi langkah 5-6 sesuai kebutuhan]
  8.  git checkout main
  9.  git pull origin main
 10.  git checkout fitur/mfa-autentikasi
 11.  git merge main
 12.  git push origin fitur/mfa-autentikasi
 13.  [buka Pull Request di GitHub]