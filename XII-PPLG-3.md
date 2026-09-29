# Studi Kasus Version Control

## 1. Keuntungan Pembatasan Branch Main

Pembatasan branch main berguna untuk menjaga branch utama tetap aman dan stabil. Fitur baru dikerjakan pada branch terpisah sehingga kesalahan tidak langsung memengaruhi sistem utama. Perubahan juga dapat diperiksa terlebih dahulu melalui Pull Request sebelum digabungkan ke branch main.

## 2. Perintah Git

```bash
git clone https://github.com/aprambudihidayat/sts_version_control.git
cd sts_version_control
git checkout -b jawaban-adi_xii-pplg3
git status
git add .
git commit -m "feat: menambahkan jawaban studi kasus MFA"
git push -u origin jawaban-adi_xii-pplg3
```
