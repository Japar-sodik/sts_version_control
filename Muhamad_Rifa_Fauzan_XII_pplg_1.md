```markdown
# Jawaban Studi Kasus Version Control

## 1. Keuntungan Utama Pembatasan Branch Main
- **Menjaga Kestabilan Sistem (Production Stability):** Menjamin kode di branch `main` selalu stabil, bersih, dan siap dirilis (*production-ready*).
- **Mencegah System Crash:** Mencegah terjadinya kegagalan sistem operasional akibat terdorongnya kode yang belum teruji atau masih bug.
- **Memaksa Proses Code Review:** Memastikan setiap perubahan harus ditinjau dan disetujui tim melalui *Pull Request* (PR) sebelum dimasukkan ke branch utama.
- **Isolasi Fitur Baru:** Anggota tim dapat mengembangkan fitur secara independen di branch terpisah tanpa mengganggu alur kerja utama.

## 2. Perintah Git (Feature Branch Workflow)

1. Memastikan berada di branch main dan memperbarui kode terbaru:
   ```bash
   git checkout main
   git pull origin main

```

2. Membuat dan berpindah ke branch fitur baru (MFA):
```bash
git checkout -b feature/mfa-authentication

```


3. Memeriksa status perubahan file:
```bash
git status

```


4. Menambahkan seluruh perubahan ke staging area:
```bash
git add .

```


5. Menyimpan perubahan secara lokal dengan pesan commit terstruktur:
```bash
git commit -m "feat: add multi-factor authentication (MFA) feature"

```


6. Mengirimkan branch fitur baru ke remote repository (GitHub):
```bash
git push -u origin feature/mfa-authentication
