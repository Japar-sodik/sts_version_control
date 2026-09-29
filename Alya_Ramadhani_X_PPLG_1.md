Jawaban Studi Kasus

1. Keuntungan Pembatasan Branch main
- Mencegah sistem crash/rusak di production.
- Ada proses code review lewat Pull Request sebelum kode digabung.
- Pengembang fokus bikin fitur di branch masing-masing tanpa mengganggu tim lain.

2. Perintah Git
```bash
git checkout main
git pull origin main
git checkout -b feature/mfa-auth
git status
git add .
git commit -m "feat: tambah fitur MFA"
git push -u origin feature/mfa-auth