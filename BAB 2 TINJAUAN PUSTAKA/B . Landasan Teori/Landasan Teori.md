# Landasan Teori

Bagian ini membahas konsep dan teknologi yang mendasari perancangan serta implementasi sistem pendaftaran Kursus Persiapan Pernikahan (KPP) berbasis web dengan pembayaran QRIS di Biara Loresa SCJ SP3. Transformasi digital pada layanan institusi menunjukkan bahwa sistem informasi dapat meningkatkan efisiensi dan kualitas tata kelola data jika disesuaikan dengan kebutuhan organisasi dan pemangku kepentingan. Hal ini sangat relevan bagi lembaga keagamaan yang membutuhkan layanan terdokumentasi dan akuntabel. Landasan teori berikut dikaitkan dengan literatur empiris dan kebutuhan operasional biara, sebagaimana diwujudkan dalam pengembangan perangkat lunak pada penelitian ini (Ilyas et al., 2025).

## 1. Sistem Informasi

Sistem informasi (SI) terdiri dari manusia, proses, data, perangkat lunak, dan perangkat keras yang memproses informasi untuk mendukung keputusan dan operasional organisasi. Di **Biara Loresa SCJ SP3**, SI dirancang untuk mendukung **Kursus Persiapan Pernikahan (KPP)** sebagai layanan gerejawi, bukan aplikasi komersial. Berdasarkan wawancara, biara membutuhkan penggantian pendaftaran yang tidak terkomputerisasi, berkas fisik, dan pembayaran tunai dengan layanan daring terpusat. SI diimplementasikan sebagai aplikasi web *client-server* untuk peserta dan pengelola *admin*, dengan pembayaran QRIS melalui Midtrans serta pengamanan akses dan data sesuai peran pengguna (Zhou et al., 2025).

## 2. Bahasa Pemrograman PHP

PHP digunakan sebagai bahasa pemrograman utama di sisi server untuk memproses logika bisnis, validasi data, autentikasi, dan integrasi layanan eksternal dalam aplikasi web. Pada proyek ini, PHP dipilih sesuai persyaratan Laravel versi 8.2 ke atas karena ekosistemnya yang matang, pengembangan yang cepat, dan kemudahan pemeliharaan. Lapisan server memisahkan logika bisnis dari antarmuka, sehingga perubahan fitur dapat dilakukan tanpa mengganggu konsistensi arsitektur. PHP menjadi fondasi stabil untuk fitur administrasi dan layanan transaksi digital pada sistem KPP ini (Nugroho et al., 2022).

## 3. Laravel Framework

Laravel digunakan sebagai *framework* utama yang menyediakan struktur untuk routing, middleware, ORM, keamanan, dan manajemen konfigurasi aplikasi. Penelitian ini menggunakan Laravel 12 untuk mempercepat siklus pengembangan melalui komponen yang dapat digunakan kembali dan konvensi arsitektur. Studi tentang pengembangan website dengan arsitektur MVC pada Laravel menunjukkan bahwa *framework* ini mendukung pengelolaan modul dan memudahkan pengembangan lanjutan pada sistem berbasis layanan. Laravel menjadi fondasi teknologi yang tepat untuk aplikasi layanan kursus pernikahan dengan banyak modul dan proses kompleks (Novia et al., 2022).

## 4. Arsitektur Model-View-Controller (MVC)

Laravel menerapkan pola Model-View-Controller (MVC) untuk memisahkan tanggung jawab antara logika data (Model), proses (Controller), dan tampilan (View). Pemisahan ini meningkatkan pemeliharaan, pengujian, dan skalabilitas aplikasi seiring bertambahnya fitur dan pengguna. Studi arsitektur perangkat lunak web menunjukkan bahwa pemisahan peran yang jelas dan pengurangan ketergantungan antar lapisan mendukung evolusi sistem tanpa mengorbankan kejelasan struktur. Penerapan MVC pada aplikasi ini memenuhi kebutuhan pengembangan jangka panjang dan menjaga konsistensi kode (More et al., 2025).

## 5. Blade Template Engine

Secara teoritis, Blade memisahkan kode tampilan dari logika bisnis sehingga antarmuka lebih mudah dirawat dan diuji. Blade menyediakan sintaks ringkas, pewarisan layout, komponen, dan direktif untuk halaman publik, dasbor peserta, dan panel admin. Dalam aplikasi ini, Blade digunakan untuk merender formulir pendaftaran multi-langkah, daftar dokumen, status pendaftaran, serta antarmuka pengelolaan periode dan materi. Studi empiris tentang antarmuka Laravel dengan Blade pada sistem informasi kampus menunjukkan bahwa lapisan tampilan yang terstruktur meningkatkan konsistensi antarmuka (Oktiriani et al., 2022).

## 6. Eloquent ORM

Laravel menggunakan Eloquent ORM untuk menghubungkan model objek aplikasi dengan tabel relasional pada basis data tanpa perlu menulis query SQL terpisah untuk setiap operasi. Penggunaan ORM meningkatkan produktivitas karena relasi data, validasi model, dan operasi CRUD dapat dilakukan secara konsisten melalui abstraksi objek. Literatur terbaru menunjukkan bahwa pendekatan ORM dalam operasi CRUD meningkatkan keterbacaan kode dan konsistensi model data pada aplikasi relasional. Eloquent sangat relevan untuk modul pendaftaran, dokumen, pembayaran, kehadiran, dan sertifikat yang memiliki relasi data kompleks (Bonteanu & Tudose, 2024).

## 7. Basis Data Relasional (MySQL)

Basis data relasional digunakan untuk menyimpan data terstruktur seperti akun, pendaftaran, periode, materi, pembayaran, dan histori notifikasi secara konsisten. Integritas data sangat penting karena kualitas layanan digital bergantung pada akurasi, keterlacakan, dan keandalan informasi bagi pengguna. Studi komparatif pada situs web pemerintah daerah menunjukkan bahwa layanan elektronik berkembang secara bertahap dan dipengaruhi oleh kualitas serta aksesibilitas kanal digital. Perancangan relasi kunci, *constraint*, dan migrasi skema basis data menjadi elemen fundamental dalam pengembangan aplikasi ini (Gavriluță et al., 2022).

## 8. JavaScript, Vite, dan Tailwind CSS

Pada *frontend*, JavaScript digunakan untuk menciptakan interaksi dinamis pada halaman aplikasi. Vite digunakan untuk bundling aset, meningkatkan kecepatan dan efisiensi pemuatan halaman. Tailwind CSS dipilih sebagai *framework* CSS berbasis utilitas untuk mempercepat pengembangan antarmuka responsif. Kajian empiris tentang arsitektur web hybrid di ekosistem Laravel menunjukkan bahwa antarmuka responsif yang terintegrasi dengan backend MVC dan basis data relasional meningkatkan efisiensi operasional dan keterbacaan tampilan dasbor, sesuai prinsip pemisahan *frontend* dari logika bisnis (Pfuño Alccahuamani et al., 2026).

## 9. Middleware dan RBAC

Middleware Laravel digunakan untuk memfilter permintaan berdasarkan autentikasi dan peran pengguna, yaitu peserta, administrator, dan super administrator. Teori kontrol akses menegaskan bahwa pemisahan hak akses berbasis peran menurunkan risiko penyalahgunaan fitur dan kebocoran data. Studi RBAC berskala besar menunjukkan bahwa model peran yang dirancang dengan baik meningkatkan efisiensi administrasi keamanan dan mengurangi kesalahan penetapan hak akses. Penerapan middleware peran pada aplikasi ini menerapkan prinsip *security by design* pada tingkat aplikasi (Sahani et al., 2022).

## 10. API Midtrans

Integrasi API pembayaran memungkinkan transaksi pendaftaran diproses otomatis, tervalidasi, dan status pembayaran dapat dipantau secara *real-time*. Implementasi menggunakan paket resmi Midtrans untuk PHP Midtrans guna menghasilkan transaksi Snap, termasuk saluran QRIS sesuai konfigurasi. Penelitian adopsi pembayaran berbasis kode QR menunjukkan bahwa kepercayaan, kesesuaian persepsi, dan kebergunaan memperkuat niat menggunakan sistem pembayaran tersebut. Callback dan umpan balik status pada *gateway* harus dirancang agar selaras dengan faktor penerimaan pengguna sehingga transaksi pendaftaran dapat dipantau secara andal (Turker et al., 2022).

## 11. Notifikasi Email

Laravel menyediakan mekanisme notifikasi dan mailer untuk mengirim pembaruan status dokumen, jadwal, pembayaran, dan kelulusan kepada peserta. Berdasarkan teori layanan digital, komunikasi sistem yang tepat waktu meningkatkan kualitas layanan dengan memberikan kepastian proses di setiap tahapan. Studi tentang adopsi pembayaran QRIS menunjukkan bahwa kepercayaan, kualitas layanan, dan kejelasan informasi memengaruhi sikap pengguna terhadap layanan pembayaran digital berbasis QR. Modul notifikasi merupakan komponen esensial dalam menjaga kualitas interaksi layanan aplikasi (Muchtar et al., 2024).

## 12. Autentikasi, Sesi, dan Perlindungan CSRF

Aplikasi berbasis sesi menyimpan identitas pengguna di sisi server setelah login, sehingga setiap permintaan berikutnya tetap berada dalam konteks keamanan yang sama. Perlindungan terhadap *Cross-Site Request Forgery (CSRF*) memerlukan token pada formulir yang divalidasi server. Autentikasi membedakan peserta, admin, dan super admin, sementara registrasi administrator pada subdomain menggunakan verifikasi email untuk memastikan keabsahan akun. Kombinasi autentikasi, sesi, dan CSRF membentuk lapisan kontrol akses yang konsisten dengan middleware RBAC. Validasi token acak (*nonce*) secara efektif mengurangi risiko CSRF pada aplikasi web (Ele, 2024).

## 13. Axios dan Permintaan HTTP pada Sisi Klien

Axios adalah klien HTTP berbasis Promise yang digunakan pada *frontend* untuk berkomunikasi dengan endpoint aplikasi secara asinkron, seperti memeriksa status pembayaran tanpa memuat ulang halaman. Permintaan asinkron mengurangi pemblokiran antarmuka dan meningkatkan responsivitas dibanding navigasi penuh. Studi perbandingan performa RESTful API antara Express.js dan Laravel menunjukkan bahwa pola permintaan HTTP penting dalam perancangan interaksi klien-server. Axios menyediakan abstraksi permintaan terstandarisasi untuk mendukung umpan balik cepat setelah pembayaran atau pembaruan status (Hadinata & Stianingsih, 2024).

## 14. Manajemen Penyimpanan Berkas dan Unggahan Dokumen

Unggahan dokumen pendaftaran, materi kursus, dan sertifikat memerlukan validasi tipe MIME dan ukuran serta pembatasan akses unduhan. Berkas disimpan terpisah dari kode aplikasi untuk mengurangi risiko eksekusi berkas berbahaya dan memudahkan pencadangan. Survei keamanan aplikasi web berbasis OWASP menegaskan bahwa jalur unggah dan validasi input harus diaudit secara sistematis. Aplikasi ini membatasi format dan ukuran pada formulir sesuai praktik keamanan (Shahid et al., 2022).

## 15. Chart.js

Chart.js adalah pustaka JavaScript sisi klien untuk menggambar grafik statistik pada elemen *canvas* HTML5 berdasarkan data dari server melalui Blade. Dalam dasbor administrasi, visualisasi tren pendaftaran, pembayaran, atau distribusi status peserta memudahkan pengambilan keputusan operasional. Teori presentasi informasi menyatakan bahwa *encoding* visual yang tepat mempercepat interpretasi pola dibanding hanya teks atau angka. Pustaka ini dimuat melalui CDN resmi dengan versi tetap sehingga pemeliharaan dependensi *frontend* terkendali tanpa memperbesar bundel Vite secara signifikan (Zhang et al., 2025).

## 16. Pustaka Dompdf

Dompdf mengubah dokumen HTML dan CSS menjadi berkas PDF di sisi server, sehingga sertifikat dapat dihasilkan dari templat Blade. Integrasi paket barryvdh/laravel-dompdf membungkus Dompdf sebagai layanan Laravel dengan injeksi dependensi yang konsisten. Penjanaan PDF mendukung distribusi resmi dokumen kelulusan tanpa bergantung pada pengolah kata di sisi klien. Literatur tentang sistem sertifikat digital yang mematuhi standar internasional menegaskan bahwa dokumen resmi dapat dibentuk dari templat terstruktur dan dibagikan secara terkendali. Hal ini sejalan dengan kebutuhan menghasilkan PDF dari templat HTML/CSS dan membatasi akses sesuai kebijakan penyimpanan agar templat tidak disalahgunakan (Yu et al., 2023).

## 17. Pendekatan Agile

*Agile* adalah pendekatan pengembangan perangkat lunak yang menekankan adaptasi terhadap perubahan, pengembangan iteratif, dan kolaborasi dengan pemangku kepentingan, bukan spesifikasi lengkap di awal proyek. Manifesto for Agile Software Development menekankan individu dan interaksi, perangkat lunak yang berfungsi, kolaborasi klien, serta respons terhadap perubahan. Pendekatan ini relevan untuk sistem KPP yang memiliki banyak modul dan dikembangkan secara bertahap serta diuji sebelum diperluas. Kajian data skala besar pada repositori perangkat lunak menunjukkan bahwa pola pengembangan Agile dapat dipetakan secara sistematis dalam ekosistem terbuka. Dalam penelitian ini, nilai-nilai Agile mengatur prioritas fitur pada program, sedangkan Scrum mengoperasionalkannya melalui peran, artefak, dan *sprint* (Moreno Martínez et al., 2024).

## 18. Metode Scrum

**Scrum** adalah kerangka kerja dalam pendekatan Agile yang menyediakan peran tetap, artefak, dan acara berulang untuk mengelola pengembangan produk kompleks. Scrum menggunakan Product Backlog, Sprint, serta peran Product Owner, Scrum Master, dan tim pengembang untuk menjaga transparansi dan akuntabilitas progres. Acara seperti perencanaan *sprint*, *daily scrum*, tinjauan *sprint*, dan retrospektif mendukung inspeksi dan adaptasi berkelanjutan. Di Biara Loresa SCJ SP3, Scrum digunakan untuk perencanaan kebutuhan, implementasi bertahap modul Laravel, dan pengujian fungsional sebelum integrasi penuh. Praktik ini sesuai dengan pengembangan perangkat lunak berbasis DevOps dan Scrum yang disintesis dari tinjauan literatur berskala besar (Pastrana et al., 2025).