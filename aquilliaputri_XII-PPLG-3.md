Jawaban Version Control.



* &#x20;Version Control: Feature Branch Workflow (Fitur MFA)



1. Keuntungan utama pembatasan branch 'main'
* Main jadi aman dan stabil. Branch main itu isinya kode yang udah jalan dan di pake beneran (production). Kalo semua anggota boleh commit langsung kesana, satu kode yg error aja bisa bikin websitenya crash
* Kodenya dicek dulu sebelum masuk. Lewat Pull Request, ketua tim atau anggota lain bisa ngereview kodenya. Jadi kalau ada bug atau celah keamanan apalagi di fitur MFA, ketahuan sebelum masuk ke main
* Kerja tim jadi lebih rapi
* Gampang dilacak kalau ada masalah, riwayat di `main` tetap bersih. Jadi kalau ada error, lebih gampang nyari penyebabnya dan balikin ke versi sebelumnya



2\. Perintah Git dari awal sampai Pull Request

* bash

&#x20;        1. Pindah ke main, terus ambil kode terbaru biar ga ketinggalan

&#x20;           git checkout main

&#x20;           git pull origin main

&#x20;        2. Bikin branch baru khusus fitur MFA, sekalian pindah ke situ

&#x20;           git checkout -b feature/mfa-authentication

&#x20;        3. Kerjain fitur MFA di editor (VS Code, dll)

&#x20;        4. Cek file apa aja yang berubah

&#x20;           git status

&#x20;        5. Masukin semua perubahan ke staging area

&#x20;           git add .

&#x20;        6. Simpen progres di lokal pakai pesan commit yang jelas

&#x20;           git commit -m "feat(auth): tambah fitur autentikasi multi-faktor (MFA) dengan OTP"

&#x20;        7. Upload branch fitur ke GitHub

&#x20;           git push -u origin feature/mfa-authentication

&#x20;        8. Buka GitHub, klik "Compare \& pull request"

&#x20;           - pastiin base: main <- compare: feature/mfa-authentication,

&#x20;           - isi deskripsi singkat, lalu klik "Create pull request"

&#x20;           - biar fiturnya bisa direview sama tim

