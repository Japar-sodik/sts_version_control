# Jawaban Studi Kasus: Feature Branch Workflow

## 1. Keuntungan Pembatasan Branch `main`

Menjaga `main` tetap stabil sehingga risiko *production crash* berkurang, karena setiap perubahan harus ditinjau lewat Pull Request sebelum digabung.

## 2. Perintah Git

```bash
git clone https://github.com/andininr/sts_version_control.git
cd sts_version_control
git checkout -b jawaban-Andini_Nurhayati_XII_PPLG_1
touch Andini_Nurhayati_XII_PPLG_1.md
git add Andini_Nurhayati_XII_PPLG_1.md
git commit -m "docs: tambah jawaban studi kasus feature branch workflow"
git push -u origin jawaban-Andini_Nurhayati_XII_PPLG_1
```

## 3. Pull Request

Buka repo fork di GitHub, klik **Compare & pull request** ke repo guru (`main`), lalu **Create pull request** dan kirim linknya.