# STS Version Control

**Nama:** Muhammad Fathir Chairil
**Kelas:** XII PPLG 1

## 1. Keuntungan utama pembatasan branch main

Branch main berisi kode yang sudah stabil. Kalau anggota tim commit langsung ke main, kode yang belum selesai atau error bisa merusak sistem yang sedang berjalan (production crash). Dengan membatasi main, semua perubahan harus lewat Pull Request dan ditinjau dulu oleh tim, jadi kode di main tetap aman.

## 2. Perintah Git untuk fitur MFA

```bash
git checkout main
git pull origin main
git checkout -b feature/mfa-authentication
git add .
git commit -m "feat(auth): tambah fitur Autentikasi Multi-faktor (MFA)"
git push -u origin feature/mfa-authentication
```
