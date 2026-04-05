# Daily Scrum

*Daily Scrum* merupakan pertemuan sinkronisasi singkat yang dijadwalkan setiap hari kerja selama *Sprint* berlangsung. Peserta memeriksa kemajuan pekerjaan terhadap *Sprint Backlog* dan sasaran *Sprint* dengan pola tiga pertanyaan utama mengenai pekerjaan yang telah selesai sejak pertemuan terakhir, rencana kerja hingga pertemuan berikutnya, serta hambatan yang menghalangi kelancaran tugas. Frekuensi harian membantu mendeteksi penyimpangan alur, kegagalan integrasi, maupun ketidakkonsistenan data sejak dini sehingga penyesuaian dapat dilakukan tanpa menunggu akhir iterasi.

Penelitian ini mengimplementasikan sistem informasi pendaftaran untuk Kursus Persiapan Perkawinan, selanjutnya disebut KPP, di Biara Loresa SCJ SP3 pada proyek aplikasi berbasis Laravel. Tabel berikut menyusun rumusan *Daily Scrum* per *Sprint* yang diselaraskan dengan butir *product backlog* aktif sesuai dokumen *Sprint Planning* dan *Sprint Backlog*, sehingga pemantauan harian mengikuti modul yang sedang dikembangkan pada rentang April 2026. Catatan dari sesi dapat mendokumentasikan temuan teknis terkait antarmuka, logika bisnis, integrasi pembayaran, maupun persistensi data sebagai jejak kemajuan tanpa menggantikan artefak kode. Kolom **Sprint** memuat nama iterasi. Kolom **Fokus pemantauan** memuat jenis pemeriksaan harian. Kolom **Rumusan Daily Scrum** memuat kalimat operasional untuk fokus tersebut pada iterasi bersangkutan. Rentang tanggal tiap *Sprint* mengacu pada dokumen *Sprint Planning*.

## Tabel Daily Scrum

| Sprint | Fokus pemantauan | Rumusan Daily Scrum |
| --- | --- | --- |
| Sprint 1 | Verifikasi kemajuan | Memverifikasi kemajuan implementasi halaman publik, formulir pendaftaran KPP, integrasi pembayaran nirtunai QRIS, serta otentikasi dan dasbor peserta terhadap rencana pada *Sprint Backlog* Sprint 1. |
| Sprint 1 | Penyelarasan rencana kerja harian | Menyelaraskan rencana kerja harian dengan sisa pekerjaan pada butir PB-01 hingga PB-04 dan dengan sasaran Sprint 1 pada dokumen *Sprint Planning*. |
| Sprint 1 | Pencatatan hambatan | Mencatat hambatan pada validasi isian formulir, penyimpanan data pendaftaran, konfirmasi transaksi pembayaran, pembaruan status lunas, maupun sesi pengguna dan peran akses. |
| Sprint 1 | Pemastian konsistensi | Memastikan konsistensi tampilan layanan publik tanpa otentikasi dan alur pendaftaran hingga pembayaran pendaftaran pada lingkungan pengembangan yang digunakan dalam penelitian. |
| Sprint 2 | Verifikasi kemajuan | Memverifikasi kemajuan modul unggah dokumen peserta, halaman jadwal materi, biaya, unduhan sertifikat pada sisi peserta, serta daftar dan verifikasi pendaftaran pada sisi pengelola terhadap *Sprint Backlog* Sprint 2. |
| Sprint 2 | Penyelarasan rencana kerja harian | Menyelaraskan rencana kerja harian dengan sisa pekerjaan pada butir PB-05 hingga PB-08 dan dengan sasaran Sprint 2 pada dokumen *Sprint Planning*. |
| Sprint 2 | Pencatatan hambatan | Mencatat hambatan pada penyimpanan berkas, alur perbaikan unggahan, pembaruan status dokumen, penugasan periode kursus, maupun konsistensi data antara tampilan peserta dan panel pengelola. |
| Sprint 2 | Pemastian konsistensi | Memastikan status pendaftaran dan dokumen pada layanan mandiri peserta selaras dengan keputusan verifikasi pengelola. |
| Sprint 3 | Verifikasi kemajuan | Memverifikasi kemajuan pengelolaan periode dan materi, pencatatan kehadiran, biaya dan tagihan, serta pengelolaan berkas kelulusan dan akses sertifikat pada peserta terhadap *Sprint Backlog* Sprint 3. |
| Sprint 3 | Penyelarasan rencana kerja harian | Menyelaraskan rencana kerja harian dengan sisa pekerjaan pada butir PB-09 hingga PB-14 dan dengan sasaran Sprint 3 pada dokumen *Sprint Planning*. |
| Sprint 3 | Pencatatan hambatan | Mencatat hambatan pada operasi pembukaan maupun penutupan periode, rekapitulasi kehadiran, transaksi tagihan, unggah berkas kelulusan, maupun ketersediaan unduhan sertifikat pada sisi peserta. |
| Sprint 3 | Pemastian konsistensi | Memastikan konsistensi data operasional kursus antar modul periode, materi, kehadiran, biaya, dan kelulusan. |
| Sprint 4 | Verifikasi kemajuan | Memverifikasi kemajuan pendaftaran akun pengelola pada kanal administrasi, verifikasi surel, serta pengelolaan daftar akun administrator oleh pengawas utama terhadap *Sprint Backlog* Sprint 4. |
| Sprint 4 | Penyelarasan rencana kerja harian | Menyelaraskan rencana kerja harian dengan sisa pekerjaan pada butir PB-15 dan PB-16 dan dengan sasaran Sprint 4 pada dokumen *Sprint Planning*. |
| Sprint 4 | Pencatatan hambatan | Mencatat hambatan pada alur verifikasi surel, aktivasi akses panel pengelola, pembatasan peran, maupun konsistensi daftar akun administrator. |
| Sprint 4 | Pemastian konsistensi | Memastikan akses administrasi memenuhi kebijakan keamanan yang direncanakan pada tahap perancangan sistem. |
