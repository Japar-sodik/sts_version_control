# Jawaban Studi Kasus Version Control

Nama: Muhamad Faiz Bayu Pratama
Kelas: XII PPLG 2

---

## Studi Kasus

Dalam sebuah proyek website UMKM, ketua tim melarang anggota melakukan commit secara langsung ke branch `main` untuk menghindari terjadinya kerusakan pada kode utama atau production. Saya ditugaskan untuk membuat fitur MFA (Multi-Factor Authentication).

### 1. Apa keuntungan membatasi branch `main`?

Keuntungan membatasi branch `main` adalah menjaga kode utama agar tetap aman dan stabil. Setiap perubahan harus melalui proses review terlebih dahulu sehingga kode yang masih error atau belum selesai tidak langsung masuk ke `main`.

Selain itu, penggunaan Pull Request membuat anggota tim lain dapat memeriksa perubahan sebelum digabungkan.

### 2. Mengapa fitur MFA harus dikerjakan pada branch terpisah?

Fitur MFA sebaiknya dikerjakan pada branch terpisah agar proses pengembangan tidak mengganggu kode utama. Jika terjadi kesalahan saat membuat fitur, branch `main` tetap aman.

Branch terpisah juga memudahkan tim untuk melakukan review dan memperbaiki kode sebelum fitur digabungkan ke `main`.

### 3. Git Commands

Pertama, melakukan clone repository hasil fork dari GitHub:

```bash
git clone https://github.com/FaBa23/sts_version_control.git
```

Masuk ke folder repository:

```bash
cd sts_version_control
```

Membuat branch baru untuk mengerjakan tugas:

```bash
git checkout -b Jawaban-Muhamad_Faiz_Bayu_Pratama_XII_PPLG_2
```

Setelah membuat atau mengedit file jawaban, mengecek perubahan:

```bash
git status
```

Menambahkan perubahan ke staging:

```bash
git add .
```

Membuat commit:

```bash
git commit -m "feat: menambahkan jawaban studi kasus MFA"
```

Mengirim branch ke repository GitHub:

```bash
git push -u origin Jawaban-Muhamad_Faiz_Bayu_Pratama_XII_PPLG_2
```

### 4. Proses Pull Request

Setelah melakukan `git push`, branch akan muncul di repository GitHub.

Selanjutnya membuat Pull Request dari branch:

`Jawaban-Muhamad_Faiz_Bayu_Pratama_XII_PPLG_2`

menuju branch:

`main`

Pull Request digunakan agar perubahan dapat diperiksa terlebih dahulu oleh ketua tim atau guru sebelum digabungkan ke branch `main`.

### 5. Kesimpulan

Penggunaan branch terpisah dan Pull Request membuat proses kerja dalam tim menjadi lebih aman dan teratur. Branch `main` tetap terlindungi dari kode yang belum selesai atau masih memiliki error. Dengan melakukan commit, push, dan Pull Request, setiap perubahan dapat diperiksa terlebih dahulu sebelum masuk ke kode utama.
