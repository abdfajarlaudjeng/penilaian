# Sistem Informasi Penilaian Peserta Didik (Sederhana)

## Struktur File
- `login.html` — Halaman login, autentikasi berdasarkan username dan password pada Google Spreadsheet.
- `index.html` — Dashboard/menu utama yang hanya dapat diakses setelah login.
- `penilaian.html` — Halaman input, tampilan, dan ekspor data penilaian siswa (keterbatasan: data hanya tersimpan di browser/localStorage).
- (Opsional) `README.md` — Petunjuk pemakaian.

## Alur Sistem
1. **Login**  
   Pengguna harus login menggunakan username dan password yang didaftarkan pada Google Spreadsheet (`users` sheet).

2. **Akses Dashboard**  
   Setelah login, pengguna diarahkan ke `index.html`, yang berisi menu navigasi.

3. **Kelola Data Penilaian**  
   - Input data penilaian (kelas, nama, mapel, nilai harian, nilai semester).
   - Data dapat dihapus baris per baris.
   - Data dapat diunduh sebagai file CSV.
   - Semua data tersimpan di browser (`localStorage`). *(Butuh integrasi lebih lanjut jika ingin langsung terhubung ke Google Sheets.)*

4. **Logout**  
   Pengguna dapat keluar dari sistem agar akun tetap aman.

## Catatan
- Ganti `SPREADSHEET_ID` dan `SHEET_API_KEY` di `login.html` sesuai milik Anda.
- Sheet `users` di Google Sheets harus memiliki kolom A: username, kolom B: password, header di baris 1, data mulai baris 2.
- Data penilaian hanya tersimpan di browser (`localStorage`). Untuk integrasi ke Google Sheets, perlu pengembangan lebih lanjut (misal via Google Apps Script Web Apps).

## Cara Menjalankan
- Upload semua file ini ke hosting atau jalankan lokal.
- Pastikan API Google Sheets sudah diaktifkan dan API Key diizinkan untuk akses publik (atau gunakan Google Apps Script untuk proteksi lebih baik).
