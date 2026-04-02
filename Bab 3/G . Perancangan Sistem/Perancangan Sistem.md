# Perancangan Sistem

Perancangan sistem pada penelitian ini disusun sebagai acuan teknis untuk pengembangan aplikasi pendaftaran Kursus Persiapan Pernikahan (KPP) berbasis web di Biara Loresa SCJ SP3. Tahap perancangan bertujuan memastikan bahwa kebutuhan pengguna yang diperoleh dari proses pengumpulan data dapat diterjemahkan menjadi struktur sistem yang jelas, terukur, dan mudah diimplementasikan. Perancangan mencakup arsitektur sistem, desain data, alur proses layanan, serta rancangan antarmuka sesuai peran pengguna. Hasil perancangan ini menjadi pedoman utama pada tahap implementasi sistem informasi yang dikembangkan.

## 1. Perancangan Arsitektur Sistem

Arsitektur sistem menggunakan pola client-server berbasis web, di mana pengguna mengakses aplikasi melalui browser dan pemrosesan data dilakukan pada server aplikasi. Sistem dibangun menggunakan framework Laravel dengan pemisahan tanggung jawab antara lapisan antarmuka, logika bisnis, dan pengelolaan data. Pola ini mendukung pengembangan modular sehingga perubahan pada satu komponen tidak mengganggu keseluruhan sistem secara signifikan. Selain itu, arsitektur dirancang untuk mendukung integrasi layanan pembayaran digital QRIS melalui Midtrans pada alur transaksi pendaftaran.

## 2. Perancangan Basis Data

Perancangan basis data difokuskan pada penyimpanan data peserta, data pendaftaran, dokumen persyaratan, transaksi pembayaran, periode kursus, materi, kehadiran, biaya tambahan, dan sertifikat. Relasi antarentitas disusun untuk memastikan integritas data, khususnya pada keterkaitan antara pengguna, status pendaftaran, dan bukti pembayaran. Struktur data juga disesuaikan dengan kebutuhan akses berbasis peran agar admin, super admin, dan peserta memperoleh data sesuai otoritas masing-masing. Dengan rancangan ini, proses pencatatan dan pelacakan data layanan dapat berjalan lebih tertib dibandingkan sistem manual.

## 3. Perancangan Alur Proses

Alur proses sistem dirancang mulai dari registrasi peserta, pengisian formulir pendaftaran, unggah dokumen, verifikasi admin, pembayaran QRIS, hingga pemantauan status layanan oleh peserta. Pada sisi pengelola, sistem menyediakan alur manajemen periode, materi, kehadiran, biaya tambahan, serta pengelolaan sertifikat peserta. Setiap alur dilengkapi aturan validasi untuk menjaga konsistensi proses dan mencegah kesalahan input data. Perancangan alur ini memastikan layanan KPP dapat berjalan secara end-to-end dalam satu sistem terintegrasi.

## 4. Perancangan Antarmuka Pengguna

Antarmuka dirancang dengan prinsip kemudahan penggunaan agar dapat dioperasikan oleh pengguna dengan latar belakang teknis yang beragam. Tampilan pada sisi peserta difokuskan pada kemudahan pendaftaran, unggah dokumen, pembayaran, dan pemantauan status layanan secara jelas. Sementara itu, tampilan pada sisi admin dan super admin difokuskan pada efisiensi pengelolaan data serta pemantauan operasional layanan. Dengan rancangan antarmuka tersebut, sistem diharapkan mampu meningkatkan kualitas pengalaman pengguna sekaligus efektivitas administrasi layanan KPP.
