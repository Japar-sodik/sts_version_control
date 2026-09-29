# Version Control

## 1. Keuntungan pembatasan branch main

Supaya branch main tetap aman dan tidak langsung terkena kesalahan dari anggota tim. Setiap fitur bisa dicek dulu sebelum digabung ke main.

## 2. Perintah Git

```bash
git clone https://github.com/Kyliee-stack/sts_version_control.git
cd sts_version_control
git checkout -b jawaban-Atika_XII_PPLG_2
git add .
git commit -m "Menambahkan jawaban tugas"
git push origin jawaban-Atika_XII_PPLG_2