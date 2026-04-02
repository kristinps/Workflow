# Daily Scrum

Daily Scrum merupakan pertemuan harian singkat yang dilakukan selama sprint untuk memantau progres pekerjaan, menyelaraskan aktivitas tim, dan mengidentifikasi hambatan sedini mungkin. Pelaksanaan Daily Scrum pada penelitian ini berpedoman pada backlog yang telah disusun, kebutuhan pengguna pada `Kebutuhan user`, serta target implementasi fitur pada tahap pengembangan sistem informasi.

## Fungsi Daily Scrum

Daily Scrum dalam penelitian ini berfungsi sebagai pertemuan harian singkat untuk memantau progres sprint, memastikan pekerjaan sesuai Sprint Backlog, dan mengidentifikasi hambatan yang perlu segera diatasi agar target pengembangan sistem informasi tetap tercapai.

## Format Pelaporan Harian

Setiap sesi Daily Scrum membahas tiga poin utama:

1. Apa yang sudah dikerjakan sejak pertemuan sebelumnya.
2. Apa yang akan dikerjakan pada hari ini.
3. Hambatan yang dihadapi selama pengerjaan.

## Ringkasan Pelaksanaan Daily Scrum


| Sprint   | Fokus Utama Daily Scrum                     | Aktivitas Harian Utama                                                                                             | Hambatan yang Dipantau                                                                                          |
| -------- | ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------- |
| Sprint 1 | Fondasi akses dan pendaftaran               | Sinkronisasi progres autentikasi, form pendaftaran, unggah dokumen, dan uji alur awal.                             | Validasi input belum konsisten, struktur data awal belum seragam, serta bug pada alur registrasi-dokumen.       |
| Sprint 2 | Verifikasi administratif dan pembayaran     | Pemantauan pengerjaan verifikasi dokumen admin, integrasi QRIS Midtrans, dan halaman status pendaftaran.           | Ketidaksesuaian status dokumen dan pembayaran, keterlambatan callback transaksi, serta error notifikasi status. |
| Sprint 3 | Operasional kursus per periode              | Koordinasi harian modul periode, materi/jadwal, kehadiran, dan pengujian fungsional modul operasional.             | Bentrok jadwal per periode, relasi data peserta-kehadiran belum stabil, dan inkonsistensi data materi.          |
| Sprint 4 | Penyempurnaan layanan dan finalisasi sistem | Monitoring penyelesaian biaya tambahan, sertifikat, dashboard, notifikasi, profil, serta final testing end-to-end. | Perbedaan hasil tampilan dashboard, ketidaksesuaian output sertifikat, dan temuan bug minor saat retest akhir.  |

Diagram berikut menyajikan **Daily Scrum dalam bentuk pohon berakar** berdasarkan isi tabel, lalu memetakan fokus aktivitas harian ke implementasi pada folder `Program`.

```mermaid
flowchart TB
    ROOT(("Daily Scrum"))

    ROOT --> S1["Sprint 1"]
    ROOT --> S2["Sprint 2"]
    ROOT --> S3["Sprint 3"]
    ROOT --> S4["Sprint 4"]

    S1 --> F1["Fokus: Fondasi akses dan pendaftaran"]
    F1 --> A1["Aktivitas: autentikasi, form pendaftaran, upload dokumen, uji alur awal"]
    A1 --> P1["Program: Auth/LoginController, KursusPendaftaranController, views auth/login, user/pendaftaran, user/dokumen"]
    A1 --> H1["Hambatan: validasi input, struktur data awal, bug alur registrasi-dokumen"]

    S2 --> F2["Fokus: Verifikasi administratif dan pembayaran"]
    F2 --> A2["Aktivitas: verifikasi dokumen admin, integrasi QRIS, pemantauan status pendaftaran"]
    A2 --> P2["Program: Admin/DokumenController, PembayaranController, views admin/pendaftaran, user/pembayaran, user/status-pendaftaran"]
    A2 --> H2["Hambatan: sinkronisasi status dokumen-pembayaran, callback transaksi, notifikasi"]

    S3 --> F3["Fokus: Operasional kursus per periode"]
    F3 --> A3["Aktivitas: manajemen periode, materi-jadwal, kehadiran, uji modul operasional"]
    A3 --> P3["Program: Admin/PeriodeController, Admin/MateriKursusController, Admin/KehadiranController, views admin/periode, dashboard/materi-periode, dashboard/kehadiran-periode"]
    A3 --> H3["Hambatan: bentrok jadwal, relasi data peserta-kehadiran, konsistensi data materi"]

    S4 --> F4["Fokus: Penyempurnaan layanan dan finalisasi sistem"]
    F4 --> A4["Aktivitas: biaya tambahan, sertifikat, dashboard, notifikasi, profil, final testing"]
    A4 --> P4["Program: Admin/BiayaController, Admin/SuratKelulusanController, Admin/DashboardController, UserProfileController, views admin/biaya, admin/sertifikat, emails"]
    A4 --> H4["Hambatan: ringkasan dashboard, output sertifikat, bug minor saat retest"]
```


## Hasil Daily Scrum

Melalui Daily Scrum, tim dapat menjaga ritme kerja sprint, mendeteksi hambatan lebih awal, dan memastikan pengembangan sistem informasi tetap selaras dengan `Kebutuhan user`.