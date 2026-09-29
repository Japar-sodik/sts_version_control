# Jawaban STS Version Control

**Nama:** Tegar Revaldi Akbar
**Kelas:** XII PPLG 1

---

### 1. Keuntungan Utama Pembatasan Branch Main

- **Mencegah Perubahan Langsung (_Direct Push_):** Menjaga agar branch utama tidak secara tidak sengaja tertimpa kode yang rusak atau belum diuji.
- **Menjaga Kestabilan Kode (_Production-Ready_):** Memastikan kode di branch `main` selalu siap digunakan dan terbebas dari bug.
- **Mewajibkan _Code Review_:** Memaksa seluruh tim melakukan pemeriksaan kode bersama melalui Pull Request sebelum digabungkan.

---

### 2. Perintah Git yang Digunakan

```bash
# 1. Membuat dan berpindah ke branch fitur jawaban
git checkout -b jawaban-Tegar_Revaldi_XII_PPLG_1

# 2. Menambahkan file jawaban ke staging area
git add Tegar_Revaldi_XII_PPLG_1.md

# 3. Menyimpan progres lokal dengan pesan commit terstruktur
git commit -m "feat: tambah file jawaban STS Tegar Revaldi XII PPLG 1"

# 4. Mengirimkan branch jawaban ke repository GitHub milik sendiri
it push -u origin jawaban-Tegar_Revaldi_XII_PPLG_1
```
 