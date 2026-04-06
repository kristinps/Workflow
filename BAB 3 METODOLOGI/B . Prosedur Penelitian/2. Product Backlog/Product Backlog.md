# Product Backlog

*Product backlog* adalah daftar tunggal dan terurut berisi semua pekerjaan yang diperlukan untuk mengembangkan serta menyempurnakan produk, mulai dari gambaran besar fitur hingga rincian teknis. Dalam kerangka Scrum, backlog disusun dan diprioritaskan oleh *Product Owner* bersama tim, dapat berubah seiring umpan balik, dan menjadi sumber utama perencanaan *Sprint*. Isinya bukan daftar tetap melainkan artefak hidup yang mencerminkan nilai bisnis dan kebutuhan pengguna terbaru.

Penelitian ini mengembangkan sistem informasi pendaftaran untuk Kursus Persiapan Perkawinan, selanjutnya disebut KPP, berbasis web di Biara Loresa SCJ SP3. *Product backlog* menghubungkan tahap analisis kebutuhan dengan pelaksanaan iteratif pengembangan perangkat lunak. Penyusunan epik, *user story*, dan butir backlog di bawah mengacu pada ruang lingkup fungsi yang direalisasikan pada implementasi aplikasi penelitian, sehingga menjadi landasan dokumentasi Scrum pada Bab Prosedur Penelitian dan jejak pelacakan pekerjaan antar *Sprint*.

## Tabel epik

Epik adalah kelompok fitur besar yang menyatukan beberapa kebutuhan pengguna ke dalam satu tema nilai bisnis maupun teknis. Tabel berikut merangkum epik yang mencakup modul utama aplikasi KPP sesuai struktur fitur pada implementasi penelitian.


| Kode | Nama epik                                         | Deskripsi ringkas                                                                                                                                            |
| ---- | ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| E01  | Portal publik dan informasi                       | Menyajikan halaman beranda, profil lembaga, berita, galeri, formulir kontak, serta kanal informasi umum bagi pengunjung.                                     |
| E02  | Pendaftaran KPP dan pembayaran pendaftaran        | Mendukung pendaftaran calon peserta secara daring, pembentukan akun peserta, dan pembayaran biaya pendaftaran melalui kode QRIS.                             |
| E03  | Dasbor dan layanan mandiri peserta                | Memberi peserta akses terpusat untuk memantau status pendaftaran, dokumen, jadwal materi, rincian biaya, sertifikat, serta pengaturan profil dan kata sandi. |
| E04  | Verifikasi pendaftaran dan dokumen oleh pengelola | Memungkinkan pengelola meninjau daftar pendaftaran, menyetujui maupun menolak pendaftaran, memverifikasi dokumen per berkas, dan menetapkan periode kursus.    |
| E05  | Operasional kursus                                | Mengelola periode KPP, materi dan penyebaran jadwal, pencatatan kehadiran per materi, serta biaya dan tagihan per periode.                                   |
| E06  | Kelulusan dan sertifikat digital                  | Mengelola penerbitan surat kelulusan maupun berkas sertifikat serta akses unduh bagi peserta yang memenuhi syarat.                                             |
| E07  | Administrasi akun pengelola                       | Mendukung pendaftaran dan verifikasi akun pengelola pada lingkup khusus serta pengelolaan akun administrator oleh pengawas utama.                            |


## Tabel user story

*User story* menyatakan kebutuhan pengguna dalam satu narasi ringkas yang dapat diprioritaskan dan diuji. Kolom **Kode US** memuat penanda cerita. **Epik** menunjuk tema besar. **User Story** menggabungkan peran, keinginan, dan manfaat dalam satu kalimat.


| Kode US | Epik | User Story |
| ------- | ---- | ---------- |
| US-01 | E01 | Sebagai pengunjung, saya ingin mengakses informasi umum biara dan KPP melalui halaman publik agar memperoleh gambaran layanan sebelum mendaftar. |
| US-02 | E02 | Sebagai calon peserta, saya ingin mengisi dan mengirim formulir pendaftaran KPP secara daring agar data pendaftaran tercatat tanpa proses kertas berulang. |
| US-03 | E02 | Sebagai calon peserta, saya ingin membayar biaya pendaftaran dengan pembayaran nirtunai berbasis QRIS agar pembayaran terverifikasi dan status administrasi jelas. |
| US-04 | E03 | Sebagai peserta, saya ingin masuk ke sistem dan melihat ringkasan status pendaftaran agar mengetahui tahapan proses secara transparan. |
| US-05 | E03 | Sebagai peserta, saya ingin mengunggah dan memperbarui dokumen persyaratan agar persyaratan administrasi terpenuhi sesuai arahan pengelola. |
| US-06 | E03 | Sebagai peserta, saya ingin melihat jadwal materi, rincian biaya, serta kelulusan maupun sertifikat agar dapat merencanakan kehadiran dan menyelesaikan administrasi kursus. |
| US-07 | E04 | Sebagai pengelola, saya ingin melihat daftar pendaftaran masuk serta menyetujui maupun menolak pendaftaran agar hanya peserta yang memenuhi syarat yang dilanjutkan. |
| US-08 | E04 | Sebagai pengelola, saya ingin memverifikasi setiap dokumen dan menetapkan periode kursus bagi peserta agar data peserta konsisten dengan jalur layanan KPP. |
| US-09 | E05 | Sebagai pengelola, saya ingin membuat dan mengubah periode kursus, materi, serta menyebarkan jadwal kepada peserta agar operasional kursus terjadwal dan terkomunikasikan. |
| US-10 | E05 | Sebagai pengelola, saya ingin mencatat kehadiran peserta per materi agar rekapitulasi kehadiran mendukung penilaian kelulusan. |
| US-11 | E05 | Sebagai pengelola, saya ingin menetapkan biaya dan tagihan terkait periode maupun peserta agar administrasi keuangan kursus tercatat terpusat. |
| US-12 | E06 | Sebagai pengelola, saya ingin mengunggah maupun memperbarui berkas kelulusan maupun sertifikat untuk pendaftaran tertentu agar peserta memperoleh bukti resmi secara digital. |
| US-13 | E06 | Sebagai peserta, saya ingin mengunduh maupun membuka sertifikat ketika telah tersedia agar memperoleh dokumen resmi secara daring tanpa pengurusan berkas di kantor yang tidak terkomputerisasi. |
| US-14 | E07 | Sebagai calon pengelola, saya ingin mendaftar sebagai akun pengelola melalui jalur khusus dan memverifikasi surel agar akses panel pengelola aman dan teridentifikasi. |
| US-15 | E07 | Sebagai pengawas utama, saya ingin mengelola daftar akun pengelola agar hak akses administrasi dapat diatur secara terpusat. |


## Tabel product backlog

Butir *product backlog* memecah pekerjaan menjadi unit yang dapat direncanakan dalam *Sprint*. Kolom **Kode PB** memuat penanda butir. **User Story** menunjuk kode cerita pengguna yang menjadi acuan. **Butir backlog** merangkum nama maupun judul ringkas pekerjaan menurut istilah Scrum. **Rumusan implementasi** memperjelas cara maupun ruang lingkup teknis pengerjaan. **Prioritas** mengatur urutan penanganan relatif. Kedua kolom terakhir disajikan berdampingan agar dapat dibandingkan untuk uji coba penyusunan naskah.


| Kode PB | User Story | Butir backlog | Rumusan implementasi | Prioritas |
| ------- | ---------- | ------------- | -------------------- | --------- |
| PB-01 | US-01 | Halaman publik meliputi beranda, profil lembaga, berita, galeri, dan kontak | Mengembangkan tampilan layanan publik meliputi beranda, profil lembaga, berita, galeri, dan kontak agar informasi umum KPP dapat diakses tanpa masuk sistem. | Tinggi |
| PB-02 | US-02 | Formulir pendaftaran KPP dan halaman konfirmasi sukses | Merealisasikan formulir pendaftaran KPP secara daring, validasi isian, penyimpanan data pendaftaran, serta halaman umpan balik sukses bagi calon peserta. | Tinggi |
| PB-03 | US-03 | Integrasi pembayaran QRIS dan pembaruan status lunas | Mengintegrasikan pembayaran nirtunai berbasis QRIS dengan pembaruan status lunas melalui konfirmasi transaksi dari penyedia layanan pembayaran. | Tinggi |
| PB-04 | US-04 | Otentikasi peserta, dasbor ringkas, dan status pendaftaran | Menerapkan otentikasi peserta, dasbor ringkas, dan tampilan status pendaftaran pada sesi pengguna yang telah terdaftar. | Tinggi |
| PB-05 | US-05 | Modul unggah dokumen dan perbaikan berkas untuk peserta | Membangun modul unggah dokumen persyaratan, penyimpanan berkas, serta alur perbaikan unggahan sesuai hasil verifikasi pengelola. | Tinggi |
| PB-06 | US-06 | Halaman jadwal materi, biaya, dan unduhan sertifikat pada sisi peserta | Menyediakan antarmuka jadwal materi, rincian biaya, dan akses unduh sertifikat pada area layanan mandiri peserta. | Sedang |
| PB-07 | US-07 | Daftar pendaftaran, penyaringan masuk, persetujuan maupun penolakan pendaftaran | Mengimplementasikan daftar pendaftaran dengan penyaringan entri masuk, beserta aksi persetujuan maupun penolakan pendaftaran oleh pengelola. | Tinggi |
| PB-08 | US-08 | Verifikasi dokumen per berkas dan penugasan periode kursus | Merealisasikan verifikasi dokumen per berkas dan penugasan peserta ke periode kursus tertentu dengan pembaruan status yang konsisten. | Tinggi |
| PB-09 | US-09 | Pengelolaan periode kursus meliputi pembukaan, penutupan, penghapusan sesuai kebijakan | Mendukung pengelolaan siklus periode kursus meliputi pembukaan, penutupan, dan penghapusan sesuai kebijakan melalui antarmuka pengelola. | Sedang |
| PB-10 | US-09 | Pengelolaan materi, penjadwalan, dan pengiriman informasi jadwal ke peserta | Mengembangkan fitur materi kursus, penjadwalan, dan penyampaian informasi jadwal maupun materi kepada peserta. | Sedang |
| PB-11 | US-10 | Pencatatan kehadiran massal per materi dalam satu periode | Mencatat kehadiran peserta per materi secara massal dalam satu periode melalui antarmuka rekapitulasi kehadiran. | Sedang |
| PB-12 | US-11 | Pengelolaan biaya dan tagihan per periode maupun peserta | Mengelola penetapan biaya dan tagihan per periode maupun per pendaftaran peserta dengan pencatatan status tagihan terpusat. | Sedang |
| PB-13 | US-12 | Pengelolaan berkas surat kelulusan maupun sertifikat pada sisi pengelola | Mengimplementasikan unggah, pembaruan, dan penyimpanan berkas surat kelulusan maupun sertifikat pada panel pengelola. | Sedang |
| PB-14 | US-13 | Tautan unduh sertifikat dan tampilan status kelulusan pada sisi peserta | Menyediakan tautan unduh sertifikat dan penayangan status kelulusan pada sisi peserta ketika berkas telah tersedia. | Sedang |
| PB-15 | US-14 | Pendaftaran akun pengelola pada domain administrasi dan verifikasi surel | Merealisasikan pendaftaran akun pengelola pada kanal administrasi serta verifikasi surel sebelum akses penuh ke panel pengelola. | Sedang |
| PB-16 | US-15 | Pengelolaan akun administrator oleh pengawas utama | Mengembangkan modul pengelolaan daftar akun administrator oleh pengawas utama dengan pembatasan akses sesuai peran. | Rendah |

