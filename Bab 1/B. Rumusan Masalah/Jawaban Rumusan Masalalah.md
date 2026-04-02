# Jawaban Rumusan Masalalah

Berdasarkan pertanyaan pada `Rumusan Masalah.md` dan implementasi sistem pada folder `Program`, jawaban disusun dengan format pertanyaan dan jawaban berikut.

## 1) Rumusan Masalah 1

**Pertanyaan:**  
Bagaimana kebutuhan pengguna terhadap sistem pendaftaran dan manajemen Kursus Persiapan Pernikahan (KPP) berbasis web di Biara Loresa SCJ?

**Jawaban dalam bentuk proses cara:**  
Proses cara pemenuhan kebutuhan pengguna dilakukan melalui tahapan berikut:

1. **Identifikasi aktor pengguna**
   - Aktor utama ditetapkan menjadi dua, yaitu peserta KPP dan administrator.
2. **Inventarisasi kebutuhan peserta**
   - Peserta membutuhkan pendaftaran daring, pengisian biodata, unggah dokumen, pembayaran QRIS, pemantauan status, akses jadwal, akses biaya, dan unduh sertifikat.
3. **Inventarisasi kebutuhan administrator**
   - Administrator membutuhkan fitur verifikasi pendaftaran/dokumen, pemberian catatan perbaikan, penetapan periode, pengelolaan materi, kehadiran, biaya tambahan, sertifikat, dan notifikasi.
4. **Pemetaan kebutuhan ke fitur sistem**
   - Setiap kebutuhan diterjemahkan menjadi fitur operasional pada modul pendaftaran, pembayaran, dashboard peserta, dan dashboard admin.
5. **Validasi pemenuhan kebutuhan melalui alur layanan**
   - Alur dijalankan dari pendaftaran, pembayaran, verifikasi, penjadwalan, hingga penyelesaian layanan.

Hasil proses menunjukkan kebutuhan pengguna telah terlayani dari tahap awal pendaftaran sampai tahap akhir pasca-kursus.

## 2) Rumusan Masalah 2

**Pertanyaan:**  
Bagaimana perancangan dan implementasi sistem pendaftaran serta manajemen KPP berbasis web yang sesuai dengan kebutuhan pengguna?

**Jawaban dalam bentuk proses cara:**  
Proses cara perancangan dan implementasi sistem dilakukan melalui urutan berikut:

1. **Menentukan arsitektur aplikasi**
   - Sistem ditetapkan sebagai aplikasi web berbasis Laravel dengan pendekatan modular.
2. **Menetapkan peran dan hak akses**
   - Peran publik, peserta, admin, dan super admin dipisahkan.
   - Keamanan akses diterapkan dengan middleware autentikasi dan otorisasi berbasis peran.
3. **Merancang alur bisnis utama**
   - Alur dirancang berurutan: pendaftaran -> pembayaran -> verifikasi dokumen -> penjadwalan periode -> pelaksanaan kursus -> sertifikat.
4. **Mengimplementasikan modul inti**
   - Modul pendaftaran: input dan validasi biodata/dokumen.
   - Modul pembayaran: integrasi Midtrans QRIS, cek status, callback.
   - Modul dashboard peserta: pemantauan status, biaya, jadwal, sertifikat, dan perbaikan dokumen.
   - Modul dashboard admin: verifikasi, assign periode, materi, kehadiran, biaya tambahan, dan sertifikat.
5. **Mengintegrasikan antar-modul**
   - Data dan status antar-modul dihubungkan agar proses berjalan end-to-end.
6. **Melakukan pengujian alur operasional**
   - Alur diuji dari tahap pendaftaran hingga keluaran sertifikat.

Hasil proses membuktikan sistem telah terimplementasi sesuai kebutuhan pengguna dan dapat digunakan secara operasional.

## 3) Rumusan Masalah 3

**Pertanyaan:**  
Bagaimana hasil evaluasi sistem pendaftaran dan manajemen KPP berbasis web menggunakan metode System Usability Scale (SUS)?

**Jawaban dalam bentuk proses cara:**  
Proses cara evaluasi sistem dilakukan dalam dua jalur, yaitu evaluasi fungsional dan evaluasi usability SUS.

1. **Evaluasi fungsional sistem**
   - Mengecek keberhasilan penyimpanan pendaftaran dan validasi data.
   - Mengecek alur unggah, verifikasi, dan perbaikan dokumen.
   - Mengecek proses pembayaran QRIS hingga status lunas.
   - Mengecek tampilan progres pada dashboard peserta.
   - Mengecek pengelolaan operasional kursus pada dashboard admin.
2. **Evaluasi usability dengan SUS**
   - Menyusun kuesioner SUS 10 butir.
   - Menetapkan responden peserta dan admin.
   - Melakukan uji pakai fitur utama lalu mengisi kuesioner.
   - Menghitung skor SUS per responden dan skor rata-rata.
   - Menginterpretasikan hasil ke tingkat kelayakan usability.
3. **Penarikan kesimpulan evaluasi**
   - Hasil fungsional menyatakan sistem berjalan sesuai alur utama.
   - Hasil SUS digunakan sebagai dasar kuantitatif untuk kesimpulan akhir kualitas usability.

Dengan proses tersebut, evaluasi sistem menjadi terstruktur, terukur, dan dapat dipertanggungjawabkan secara akademik.
