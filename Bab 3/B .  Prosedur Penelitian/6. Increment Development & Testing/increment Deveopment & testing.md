# Increment Development and Testing

Tahap Increment Development and Testing merupakan proses pengembangan fitur secara bertahap pada setiap sprint, kemudian diikuti pengujian untuk memastikan setiap hasil pengembangan (increment) berjalan sesuai kebutuhan. Tahap ini dilaksanakan berdasarkan prioritas backlog dan kebutuhan pengguna yang dihimpun pada `Kebutuhan user`, serta implementasi modul pada tahap pengembangan sistem informasi.

## Strategi Increment Development

Pengembangan increment dilakukan dari fitur inti menuju fitur pendukung. Setiap sprint menghasilkan peningkatan sistem yang dapat digunakan dan dievaluasi, sehingga tim dapat memastikan kualitas fungsi sebelum melanjutkan ke sprint berikutnya.

## Rincian Increment dan Pengujian


| Sprint   | Increment yang Dikembangkan                                        | Jenis Pengujian                                                  | Indikator Keberhasilan                                                       |
| -------- | ------------------------------------------------------------------ | ---------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| Sprint 1 | Autentikasi pengguna, pendaftaran online, dan upload dokumen       | Uji fungsional form, validasi input, dan penyimpanan data        | Pengguna dapat login, mendaftar, dan mengunggah dokumen tanpa error utama    |
| Sprint 2 | Verifikasi dokumen admin, pembayaran QRIS, dan status pendaftaran  | Uji fungsional alur verifikasi, transaksi, dan perubahan status  | Dokumen dapat diverifikasi, pembayaran tercatat, dan status peserta terbarui |
| Sprint 3 | Manajemen periode, materi, dan kehadiran peserta                   | Uji fungsional CRUD data periode/materi dan pencatatan kehadiran | Data operasional kursus dapat dikelola konsisten per periode                 |
| Sprint 4 | Biaya tambahan, sertifikat, dashboard, notifikasi, dan profil akun | Uji integrasi modul dan uji end-to-end alur layanan              | Seluruh modul utama dan pendukung berjalan terpadu dan siap digunakan        |


## Ringkasan Fokus dan Tujuan Increment


| Sprint   | Fokus Increment                                   | Tujuan Hasil Increment                                                                                                                 |
| -------- | ------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| Sprint 1 | Fondasi akses pengguna dan pendaftaran digital    | Menghasilkan alur awal sistem yang memungkinkan pengguna login, mendaftar, dan mengunggah dokumen secara valid.                        |
| Sprint 2 | Verifikasi administratif dan transaksi pembayaran | Menghasilkan proses verifikasi dokumen dan pembayaran yang terintegrasi agar status pendaftaran peserta dapat dipantau dengan akurat.  |
| Sprint 3 | Operasional kursus per periode                    | Menghasilkan modul pengelolaan periode, materi, dan kehadiran yang stabil untuk mendukung pelaksanaan kursus.                          |
| Sprint 4 | Penyempurnaan layanan dan finalisasi sistem       | Menghasilkan integrasi fitur pendukung (biaya, sertifikat, dashboard, notifikasi, profil) yang siap digunakan sebagai increment akhir. |

## Rincian Increment Development

| Sprint | Rincian Tujuan Increment Development |
| --- | --- |
| Sprint 1 | Increment Sprint 1 menghasilkan fondasi aplikasi yang stabil melalui pemisahan akses peserta dan admin, autentikasi berbasis peran, serta validasi input utama pada alur pendaftaran. Pada sprint ini juga terbentuk proses pendaftaran online beserta unggah dokumen persyaratan, sehingga sistem memiliki alur inti layanan KPP yang dapat langsung digunakan untuk tahap awal operasional. |
| Sprint 2 | Increment Sprint 2 menghasilkan modul verifikasi administratif dan pembayaran yang saling terintegrasi. Sistem mampu memproses verifikasi dokumen per item oleh admin, mencatat pembayaran QRIS melalui Midtrans, serta memperbarui status pendaftaran peserta secara konsisten, sehingga transparansi proses layanan menjadi lebih terukur dan mudah dipantau pengguna. |
| Sprint 3 | Increment Sprint 3 menghasilkan modul operasional kursus per periode yang lebih terstruktur. Hasil sprint ini memperkuat pengelolaan periode, materi, jadwal, dan kehadiran peserta, sehingga pelaksanaan kursus dapat dikendalikan secara rapi per angkatan dan data operasional tersimpan lebih konsisten untuk kebutuhan monitoring layanan. |
| Sprint 4 | Increment Sprint 4 menghasilkan penyempurnaan layanan melalui integrasi fitur biaya tambahan, sertifikat, dashboard monitoring, notifikasi, dan pengelolaan profil akun. Pada tahap ini dilakukan final testing end-to-end agar seluruh modul utama dan pendukung berjalan terpadu, sehingga sistem siap digunakan sebagai hasil akhir pengembangan. |


## Metode Testing

Pengujian pada penelitian ini menggunakan pendekatan black-box testing untuk menilai kesesuaian fungsi tanpa melihat struktur kode program. Fokus pengujian diarahkan pada kesesuaian input, proses, dan output pada sisi peserta maupun admin.

Ruang lingkup pengujian meliputi:
1. Pengujian fungsional per modul pada setiap sprint (autentikasi, pendaftaran, verifikasi dokumen, pembayaran, periode, materi, kehadiran, biaya, sertifikat, dan profil).
2. Pengujian integrasi antar modul untuk memastikan perubahan status data berjalan konsisten, khususnya pada alur verifikasi dan pembayaran.
3. Pengujian end-to-end dari pendaftaran peserta sampai penerbitan sertifikat untuk memastikan alur layanan KPP berjalan utuh.

Hasil pengujian setiap sprint digunakan sebagai dasar perbaikan increment berikutnya agar kualitas sistem meningkat secara bertahap.

## Hasil Tahap Increment Development & Testing

Melalui tahapan ini, setiap increment pada sistem informasi yang dikembangkan dapat divalidasi secara bertahap dan diperbaiki segera ketika ditemukan kendala. Hasil pengujian menunjukkan bahwa sistem telah memenuhi kebutuhan inti layanan yang dihimpun dari `Kebutuhan user`, terutama pada digitalisasi pendaftaran, verifikasi dokumen, dan pembayaran QRIS.