# Jawaban Studi Kasus Version Control System

## 1. Keuntungan Utama Pembatasan Branch Main
- **Biar Aplikasi Enggak Gampang Crash:** Biar kode yang ada di branch `main` tetap aman dan siap pakai, tanpa risiko ketumpuk kode baru yang masih belum stabil atau masih ada bug-nya.
- **Bisa Dicek Bareng-Bareng Dulu:** Setiap perubahan wajib di-review dulu sama ketua tim atau teman lewat Pull Request (PR) sebelum kodenya digabung. Jadi kalau ada yang keliru, bisa langsung ketahuan.
- **Kerja Masing-Masing Jadi Lebih Tenang:** Kita bisa bebas ngubah fitur baru di branch sendiri tanpa perlu khawatir bikin error fitur lain yang udah jadi.

## 2. Urutan Perintah Git yang Dipakai
1. Bikin branch baru untuk fitur MFA dan langsung pindah ke sana:
   `git checkout -b feature/autentikasi-baru`
2. Cek file mana aja yang habis kita ubah:
   `git status`
3. Menandai/menyiapkan semua file perubahan untuk disimpan:
   `git add .`
4. Menyimpan riwayat perubahan di lokal pakai pesan yang jelas:
   `git commit -m "feat: menambahkan fitur autentikasi tambahan"`
5. Mengirimkan branch fitur tersebut ke repository GitHub:
   `git push origin feature/autentikasi-baru`