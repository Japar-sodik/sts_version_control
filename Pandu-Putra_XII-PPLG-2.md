# KK RPL 2 - Version Control

## Studi Kasus

Penerapan Fitur Baru dengan Feature Branch Workflow

## Jawaban

### 1. Apa keuntungan utama dari pembatasan branch main dalam tim pengembang?

Keuntungan utama pembatasan branch main adalah menjaga kode utama agar tetap stabil dan mengurangi risiko terjadinya error pada sistem yang sudah berjalan. Anggota tim tidak langsung melakukan commit ke branch main, tetapi mengerjakan fitur baru di branch terpisah terlebih dahulu.

Dengan cara ini, setiap perubahan dapat diperiksa sebelum digabungkan ke branch main melalui Pull Request. Jika terdapat kesalahan, perbaikannya dapat dilakukan di branch fitur tanpa mengganggu versi utama yang sedang digunakan. Selain itu, riwayat perubahan juga menjadi lebih rapi dan mudah dilacak oleh anggota tim.

### 2. Tuliskan seluruh perintah Git yang digunakan mulai dari membuat branch fitur terpisah, menyimpan progres lokal, hingga mengirimkannya ke GitHub agar siap ditinjau lewat Pull Request.

Pertama, fork repository milik guru melalui GitHub, kemudian clone repository hasil fork ke komputer.

```bash
git clone https://github.com/japar-sodik/sts_version_control.git
```

Setelah proses clone selesai, masuk ke folder repository.

```bash
cd sts_version_control
```

Kemudian pastikan berada di branch main dan ambil versi terbaru dari repository.

```bash
git checkout String
git pull origin String
```

Setelah itu, buat branch baru khusus untuk mengerjakan jawaban.

```bash
git checkout -b jawaban-Pandu-Putra_XII-PPLG
```

Selanjutnya buat file jawaban di root folder project sesuai ketentuan.

```text
Pandu-Putra_XII-PPLG-2.md
```

Setelah jawaban selesai dikerjakan, cek perubahan yang ada pada repository.

```bash
git status
```

Tambahkan file yang sudah dibuat ke staging area.

```bash
git add Pandu-Putra_XII-PPLG-2.md
```

Kemudian simpan perubahan ke repository lokal menggunakan commit.

```bash
git commit -m "Menambahkan jawaban studi kasus version control Pandu Putra"
```

Setelah commit berhasil, kirim branch tersebut ke repository GitHub hasil fork.

```bash
git push -u origin jawaban-Pandu-Putra_XII-PPLG
```

Setelah branch berhasil dikirim ke GitHub, buka repository hasil fork. Selanjutnya buat Pull Request dari branch `jawaban-Pandu-Putra_XII-PPLG` menuju branch `String` pada repository utama milik guru.
