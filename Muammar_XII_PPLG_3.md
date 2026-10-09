# Version Control: Penerapan Fitur Baru (Feature Branch Workflow)

**Nama:** [Muammar Khadafi Al-Ghazali]
**Kelas:** [XII PPLG III]

## 1. Keuntungan Pembatasan Branch Main

Branch main itu isinya kode yang lagi jalan di production. Kalau anggota tim dilarang commit langsung ke sana, keuntungannya:

- **Main tetap stabil.** Kode yang belum dites atau masih ada bug nggak langsung masuk, jadi website UMKM nggak gampang crash.
- **Ada proses review.** Setiap perubahan lewat Pull Request dulu, jadi anggota lain bisa cek kodenya sebelum digabung.
- **Kerja tim nggak bentrok.** Tiap orang punya branch sendiri, jadi nggak saling timpa kode.
- **Gampang rollback.** Kalau ada masalah, tinggal batalin branch fitur atau PR-nya tanpa ngerusak main.
- **Riwayat lebih rapi.** Kelihatan jelas siapa ngerjain fitur apa.

## 2. Perintah Git yang Digunakan

### a. Pindah ke main dan update dulu
```bash
git checkout main
git pull origin main
```

### b. Bikin branch fitur baru
```bash
git checkout -b feature/mfa-authentication
```

### c. Cek status file yang berubah
```bash
git status
```

### d. Simpan progres lokal (staging + commit)
```bash
git add .
git commit -m "feat: tambah autentikasi multi-faktor (MFA)"
```

Kalau ngerjainnya bertahap, boleh commit beberapa kali:
```bash
git add auth/mfa.js
git commit -m "feat: tambah verifikasi kode OTP"
```

### e. Kirim branch ke GitHub
```bash
git push -u origin feature/mfa-authentication
```

### f. Buat Pull Request
Buka repository di GitHub, klik **Compare & pull request**, isi judul dan deskripsi, lalu submit supaya ketua tim bisa review sebelum digabung ke main.