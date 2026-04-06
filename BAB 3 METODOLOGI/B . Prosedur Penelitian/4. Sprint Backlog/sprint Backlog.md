# Sprint Backlog

*Sprint Backlog* adalah kumpulan pekerjaan yang dipilih dari *product backlog* untuk satu iterasi *Sprint* dan dipecah menjadi tugas yang dapat dilaksanakan selama periode tersebut. Daftar ini menjadi acuan pelaksanaan pengembangan harian dalam batas sasaran *Sprint* dan dapat disesuaikan secara terkendali sepanjang iterasi berlangsung. Setiap butir mengacu pada modul fitur pada aplikasi sehingga kemajuan dapat dilacak hingga *increment* siap diuji. Peran *Sprint Backlog* melengkapi rantai *product backlog* dan *Sprint Planning* dalam dokumentasi penelitian berbasis Scrum.

Penelitian ini mengimplementasikan sistem informasi pendaftaran untuk Kursus Persiapan Perkawinan, selanjutnya disebut KPP, di Biara Loresa SCJ SP3 pada proyek aplikasi berbasis Laravel. Tabel berikut menyusun seluruh rincian tugas pelaksanaan yang bersesuaian dengan pemetaan butir PB pada dokumen *Sprint Planning* dan dengan rumusan implementasi pada dokumen *Product Backlog*, sehingga jejak kerja antar *Sprint* tetap terbaca pada naskah Bab Prosedur Penelitian. Kolom **Kode SB** memuat identifikasi butir *Sprint Backlog* dengan pola SB{nomor *Sprint*}-{nomor urut tugas dalam *Sprint* tersebut}. Kolom **Kode PB** memuat kode butir *product backlog*. Kolom **Uraian tugas** memuat deskripsi pekerjaan teknis yang dilaksanakan pada iterasi bersangkutan. Rentang tanggal tiap *Sprint* mengacu pada dokumen *Sprint Planning*.

## Tabel Sprint Backlog


| Kode SB | Kode PB | Uraian tugas                                                                                                                                                 |
| ------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| SB1-01  | PB-01   | Mengembangkan tampilan layanan publik meliputi beranda, profil lembaga, berita, galeri, dan kontak agar informasi umum KPP dapat diakses tanpa masuk sistem. |
| SB1-02  | PB-02   | Merealisasikan formulir pendaftaran KPP secara daring, validasi isian, penyimpanan data pendaftaran, serta halaman umpan balik sukses bagi calon peserta.    |
| SB1-03  | PB-03   | Mengintegrasikan pembayaran nirtunai berbasis QRIS dengan pembaruan status lunas melalui konfirmasi transaksi dari penyedia layanan pembayaran.              |
| SB1-04  | PB-04   | Menerapkan otentikasi peserta, dasbor ringkas, dan tampilan status pendaftaran pada sesi pengguna yang telah terdaftar.                                      |
| SB2-01  | PB-05   | Membangun modul unggah dokumen persyaratan, penyimpanan berkas, serta alur perbaikan unggahan sesuai hasil verifikasi pengelola.                             |
| SB2-02  | PB-06   | Menyediakan antarmuka jadwal materi, rincian biaya, dan akses unduh sertifikat pada area layanan mandiri peserta.                                            |
| SB2-03  | PB-07   | Mengimplementasikan daftar pendaftaran dengan penyaringan entri masuk, beserta aksi persetujuan maupun penolakan pendaftaran oleh pengelola.                 |
| SB2-04  | PB-08   | Merealisasikan verifikasi dokumen per berkas dan penugasan peserta ke periode kursus tertentu dengan pembaruan status yang konsisten.                        |
| SB3-01  | PB-09   | Mendukung pengelolaan siklus periode kursus meliputi pembukaan, penutupan, dan penghapusan sesuai kebijakan melalui antarmuka pengelola.                     |
| SB3-02  | PB-10   | Mengembangkan fitur materi kursus, penjadwalan, dan penyampaian informasi jadwal maupun materi kepada peserta.                                               |
| SB3-03  | PB-11   | Mencatat kehadiran peserta per materi secara massal dalam satu periode melalui antarmuka rekapitulasi kehadiran.                                             |
| SB3-04  | PB-12   | Mengelola penetapan biaya dan tagihan per periode maupun per pendaftaran peserta dengan pencatatan status tagihan terpusat.                                  |
| SB3-05  | PB-13   | Mengimplementasikan unggah, pembaruan, dan penyimpanan berkas surat kelulusan maupun sertifikat pada panel pengelola.                                        |
| SB3-06  | PB-14   | Menyediakan tautan unduh sertifikat dan penayangan status kelulusan pada sisi peserta ketika berkas telah tersedia.                                          |
| SB4-01  | PB-15   | Merealisasikan pendaftaran akun pengelola pada kanal administrasi serta verifikasi surel sebelum akses penuh ke panel pengelola.                             |
| SB4-02  | PB-16   | Mengembangkan modul pengelolaan daftar akun administrator oleh pengawas utama dengan pembatasan akses sesuai peran.                                          |


