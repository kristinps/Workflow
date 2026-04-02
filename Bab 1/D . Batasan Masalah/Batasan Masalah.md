# Batasan Masalah

Berdasarkan kebutuhan pengguna dan implementasi sistem pada folder `Program`, batasan masalah dalam penelitian ini adalah sebagai berikut:

1. Penelitian ini mencakup pengembangan sistem pendaftaran dan manajemen Kursus Persiapan Pernikahan (KPP) berbasis web pada lokus Biara Loresa SCJ dengan dua domain layanan (publik dan admin), dan tidak mencakup pengembangan untuk multi-instansi atau lembaga lain di luar lokus penelitian.

2. Penelitian ini mencakup penggunaan domain layanan yang sudah ditetapkan pada sistem, yaitu domain publik `biaraloresa.my.id` dan domain admin `admin.biaraloresa.my.id`, dan tidak mencakup penggunaan domain lain, multi-domain dinamis, atau konfigurasi domain lintas instansi.

3. Penelitian ini mencakup implementasi pada lingkungan server aplikasi web dengan sistem operasi Ubuntu 24.04 yang mendukung PHP/Laravel, basis data, storage dokumen, dan konfigurasi layanan pembayaran/notifikasi sesuai kebutuhan operasional sistem, dan tidak mencakup perancangan infrastruktur high-availability tingkat enterprise (cluster, auto-scaling, multi-region, failover otomatis, atau disaster recovery penuh) maupun pengujian lintas berbagai distribusi sistem operasi server lainnya.

4. Penelitian ini mencakup pengguna dengan peran user, admin, dan super admin sesuai kontrol akses sistem, dan tidak mencakup peran tambahan seperti operator keuangan khusus, auditor independen, atau pengajar eksternal dengan hak akses terpisah.

5. Penelitian ini mencakup pendaftaran online melalui formulir biodata, unggah dokumen persyaratan digital, validasi data masukan, serta alur verifikasi dokumen oleh admin termasuk persetujuan, penolakan, dan perbaikan dokumen oleh peserta, dan tidak mencakup pendaftaran manual/offline, legalisasi fisik dokumen, verifikasi biometrik, integrasi validasi identitas nasional eksternal, atau verifikasi otomatis berbasis machine learning/OCR.

6. Penelitian ini mencakup pembayaran non-tunai melalui QRIS terintegrasi Midtrans beserta proses pembuatan QR, pengecekan status transaksi, callback, dan pembaruan status pembayaran, dan tidak mencakup metode pembayaran lain (tunai, transfer manual bank, virtual account terpisah) maupun rekonsiliasi akuntansi otomatis lintas sistem keuangan eksternal.

7. Penelitian ini mencakup manajemen operasional kursus berupa pengelolaan periode (buat, ubah, buka/tutup, hapus), penempatan peserta ke periode, pengelolaan materi, pengiriman informasi materi dan tautan Zoom, serta pengelolaan kehadiran, dan tidak mencakup penjadwalan otomatis berbasis algoritma, fitur video conference bawaan di aplikasi, absensi berbasis geolokasi/QR lokasi, atau integrasi perangkat IoT.

8. Penelitian ini mencakup manajemen administrasi layanan KPP berupa pengelolaan biaya tambahan, pengelolaan sertifikat kelulusan (buat, ubah, lihat, hapus, unduh), dashboard peserta untuk pemantauan status layanan, notifikasi email, serta fitur profil dan perubahan kata sandi pengguna, dan tidak mencakup modul akuntansi penuh, tanda tangan digital tersertifikasi, verifikasi sertifikat berbasis blockchain, personalisasi dashboard lanjutan, notifikasi multikanal (WhatsApp API resmi/push notification/SMS gateway), maupun federated identity seperti Single Sign-On (SSO).

9. Penelitian ini mencakup halaman publik pendukung (profil, berita, galeri, kontak) sebagai pelengkap informasi layanan, dan tidak mencakup manajemen konten tingkat enterprise dengan alur editorial kompleks.

10. Penelitian ini mencakup implementasi sistem pada platform web yang diakses melalui browser, dan tidak mencakup pengembangan aplikasi mobile native (Android/iOS) atau desktop application.

11. Penelitian ini mencakup pengelolaan data yang berkaitan langsung dengan layanan KPP, dan tidak mencakup pengolahan data di luar konteks layanan yang tidak relevan dengan tujuan penelitian.

12. Penelitian ini mencakup evaluasi melalui pengujian fungsional alur utama serta pengukuran usability menggunakan System Usability Scale (SUS), dan tidak mencakup pengujian non-fungsional mendalam (stress test skala besar, penetration test komprehensif, benchmarking performa rinci) atau metode evaluasi usability lain sebagai metode utama.
