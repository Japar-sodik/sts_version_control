Keuntungan Utama Pembatasan Branch Main:
Pembatasan (protection) pada branch main mencegah terjadinya production crash akibat kode yang belum teruji atau rusak secara tidak sengaja terdorong (push) ke lingkungan produksi. Kebijakan ini memastikan seluruh perubahan kode wajib melalui mekanisme peninjauan (code review) dan tes otomatis via Pull Request (PR) sebelum digabungkan.

 1. Membuat dan berpindah ke branch fitur baru:
git checkout -b feature/mfa-authentication

 2. Memeriksa status perubahan file setelah mengembangkan fitur MFA:
git status

 3. Menambahkan perubahan ke staging area:
git add .

 4. Menyimpan progres secara lokal dengan pesan commit terstruktur:
git commit -m "feat: add multi-factor authentication (MFA) feature"

 5. Mengirimkan branch fitur ke remote repository (GitHub):
git push -u origin feature/mfa-authentication