# Landasan Teori

Bagian ini menyajikan konsep dan teknologi yang mendasari perancangan serta implementasi sistem pendaftaran Kursus Persiapan Pernikahan (KPP) berbasis web dengan pembayaran QRIS pada Biara Loresa SCJ SP3, sebagaimana tercermin pada kebutuhan pengguna dan pada aplikasi pada folder `Program`. Kerangka transformasi digital pada layanan berbasis institusi turut menjadi acuan bahwa penerapan sistem informasi dapat meningkatkan efisiensi dan kualitas tata kelola data ketika selaras dengan konteks organisasi dan kebutuhan pemangku kepentingan. Hal ini relevan bagi lembaga keagamaan yang mengelola layanan kepada jamaat secara terdokumentasi dan akuntabel. Oleh karena itu landasan berikut dihubungkan dengan literatur empiris dan kebutuhan operasional biara sebagaimana diwujudkan dalam pengembangan perangkat lunak pada penelitian ini (Ilyas et al., 2025).

## 1. Sistem Informasi

Sistem informasi (SI) adalah kumpulan komponen (manusia, proses, data, perangkat lunak, dan perangkat keras) yang mengolah informasi untuk mendukung keputusan dan operasional organisasi. Pada **Biara Loresa SCJ SP3**, SI dirancang untuk mendukung **Kursus Persiapan Pernikahan (KPP)** sebagai pelayanan gerejawi, bukan sekadar aplikasi komersial. Berdasarkan wawancara, biara memerlukan penggantian pendaftaran manual, berkas fisik, dan pembayaran tunai menuju layanan daring terpusat yang telah disetujui. Dalam folder `Program`, SI itu diwujudkan sebagai aplikasi web *client–server* untuk peserta dan pengelola biara (*admin*/*super admin*) dengan pembayaran QRIS melalui Midtrans serta pengamanan akses dan data sesuai peran pengguna (Zhou et al., 2025).

## 2. Bahasa Pemrograman PHP

PHP berperan sebagai bahasa pemrograman utama pada sisi server untuk memproses logika bisnis, validasi data, autentikasi, dan integrasi layanan eksternal dalam aplikasi web. Pada proyek ini digunakan PHP sesuai persyaratan kerangka Laravel (versi 8.2 ke atas) sehingga pemilihan bahasa backend mempertimbangkan kematangan ekosistem, kecepatan pengembangan, dan kemudahan pemeliharaan pada sistem yang berkembang. Dalam arsitektur berbasis web, lapisan server memisahkan logika bisnis dari struktur antarmuka sehingga perubahan fitur dapat dilakukan tanpa mengorbankan konsistensi arsitektur secara keseluruhan. Oleh karena itu penggunaan PHP dinilai relevan sebagai fondasi stabil untuk fitur administrasi dan layanan transaksi digital pada sistem KPP ini (Nugroho et al., 2022).

## 3. Laravel Framework

Laravel berfungsi sebagai *framework* utama yang menyediakan struktur kerja untuk routing, middleware, ORM, keamanan, dan manajemen konfigurasi aplikasi. Implementasi pada penelitian memakai Laravel 12 yang mempercepat siklus pengembangan melalui komponen yang dapat digunakan kembali serta konvensi arsitektur. Penelitian mengenai pengembangan website dengan arsitektur MVC pada Laravel menunjukkan bahwa *framework* ini mendukung pengelolaan modul dan memudahkan pengembangan lanjutan pada sistem berbasis layanan. Dengan demikian Laravel layak dijadikan fondasi teknologi untuk aplikasi layanan kursus pernikahan yang memiliki banyak modul dan alur proses yang kompleks (Novia et al., 2022).

## 4. Arsitektur Model-View-Controller (MVC)

Laravel menerapkan pola Model-View-Controller (MVC) untuk memisahkan tanggung jawab antara logika data (Model), logika proses (Controller), dan tampilan antarmuka (View). Pemisahan ini meningkatkan pemeliharaan, pengujian, dan skalabilitas aplikasi seiring bertambahnya fitur dan pengguna. Kajian arsitektur perangkat lunak web menunjukkan bahwa pola yang mempertahankan pemisahan peran namun mengurangi ketergantungan berlebihan antar lapisan mendukung evolusi sistem tanpa mengorbankan kejelasan struktur. Dengan demikian penerapan MVC pada aplikasi ini memenuhi kebutuhan pengembangan berkelanjutan jangka panjang tanpa mengorbankan konsistensi kode (More et al., 2025).

## 5. Blade Template Engine

Secara teoritis, template engine Blade memisahkan kode tampilan dari logika bisnis sehingga antarmuka lebih mudah dirawat dan diuji. Blade menyediakan sintaks ringkas, pewarisan layout, komponen, serta direktif untuk halaman publik, dasbor peserta, dan panel admin. Dalam aplikasi ini Blade digunakan untuk merender formulir pendaftaran multi-langkah, daftar dokumen, status pendaftaran, serta antarmuka pengelolaan periode dan materi. Studi empiris mengenai antarmuka berbasis Laravel dengan Blade pada sistem informasi kampus mendukung argumen bahwa lapisan tampilan yang terstruktur meningkatkan konsistensi antarmuka (Oktiriani et al., 2022).

## 6. Eloquent ORM

Laravel memanfaatkan Eloquent ORM untuk menghubungkan model objek aplikasi dengan tabel relasional pada basis data tanpa menulis query SQL secara manual untuk setiap operasi. Penggunaan ORM secara teoritis meningkatkan produktivitas karena relasi data, validasi model, dan operasi CRUD dapat dilakukan secara konsisten melalui abstraksi objek. Literatur terbaru menunjukkan bahwa pendekatan ORM dalam operasi CRUD berkontribusi terhadap keterbacaan kode dan konsistensi model data pada aplikasi relasional. Oleh karena itu Eloquent sangat relevan untuk modul pendaftaran, dokumen, pembayaran, kehadiran, dan sertifikat yang memiliki relasi data kompleks (Bonteanu & Tudose, 2024).

## 7. Basis Data Relasional (MySQL)

Teknologi basis data relasional digunakan untuk menyimpan data terstruktur seperti akun, pendaftaran, periode, materi, pembayaran, dan histori notifikasi secara konsisten. Integritas data merupakan aspek teoretis yang krusial karena kualitas layanan digital sangat dipengaruhi oleh akurasi, keterlacakan, dan keandalan informasi bagi pengguna. Studi komparatif terhadap situs web pemerintah daerah sebagai sarana e-governance menunjukkan bahwa layanan elektronik berkembang secara bertahap dan dipengaruhi oleh kualitas serta aksesibilitas kanal digital bagi penyelenggara. Dengan demikian perancangan relasi kunci, *constraint*, dan migrasi skema basis data menjadi elemen fundamental dalam pengembangan aplikasi ini (Gavriluță et al., 2022).

## 8. JavaScript, Vite, dan Tailwind CSS

Pada sisi *frontend*, JavaScript digunakan untuk menciptakan interaksi dinamis pada halaman aplikasi. Vite berperan dalam proses bundling aset guna meningkatkan kecepatan dan efisiensi pemuatan halaman. Tailwind CSS digunakan sebagai *framework* CSS berbasis utilitas untuk mempercepat pengembangan antarmuka responsif. Kajian empiris mengenai arsitektur web hybrid pada ekosistem Laravel menunjukkan bahwa lapisan antarmuka yang responsif dipadukan dengan backend berpola MVC dan basis data relasional untuk mendukung efisiensi operasional dan keterbacaan tampilan dasbor, sejalan dengan prinsip memisahkan *frontend* dari logika bisnis (Pfuño Alccahuamani et al., 2026).

## 9. Middleware dan RBAC

Middleware Laravel digunakan untuk memfilter permintaan berdasarkan autentikasi dan peran pengguna, yaitu peserta (*user*), administrator, dan super administrator. Teori kontrol akses menegaskan bahwa pemisahan hak akses berbasis peran dapat menurunkan risiko penyalahgunaan fitur dan kebocoran data. Studi RBAC berskala besar menunjukkan bahwa model peran yang dirancang dengan baik meningkatkan efisiensi administrasi keamanan serta mengurangi kesalahan penetapan hak akses. Oleh karena itu penerapan middleware peran pada aplikasi ini merupakan implementasi prinsip *security by design* pada tingkat aplikasi (Sahani et al., 2022).

## 10. API Midtrans

Integrasi API pembayaran digunakan agar transaksi pendaftaran dapat diproses secara otomatis, tervalidasi, dan memiliki status pembayaran yang dapat dipantau secara *real-time*. Pada implementasi digunakan paket resmi Midtrans untuk PHP (`midtrans/midtrans-php`) guna menghasilkan transaksi Snap termasuk saluran QRIS sesuai konfigurasi. Penelitian adopsi pembayaran berbasis kode QR menunjukkan bahwa kepercayaan yang dirasakan, kesesuaian persepsi, dan kebergunaan yang dirasakan memperkuat niat menggunakan sistem pembayaran tersebut. Oleh karena itu perancangan *callback* dan umpan balik status pada *gateway* perlu selaras dengan faktor penerimaan pengguna agar transaksi pendaftaran tetap dapat dipantau secara andal (Turker et al., 2022).

## 11. Notifikasi Email

Laravel menyediakan mekanisme notifikasi dan mailer untuk mengirim pembaruan status dokumen, jadwal, pembayaran, dan kelulusan kepada peserta. Berdasarkan kerangka teori layanan digital, komunikasi sistem yang tepat waktu meningkatkan kualitas layanan karena memberikan kepastian proses pada setiap tahapan. Studi mengenai adopsi pembayaran QRIS menunjukkan bahwa faktor kepercayaan, kualitas layanan, dan kejelasan informasi memengaruhi sikap pengguna terhadap layanan pembayaran digital berbasis QR. Dengan demikian modul notifikasi merupakan komponen esensial dalam menjaga kualitas interaksi layanan aplikasi (Muchtar et al., 2024).

## 12. Autentikasi, Sesi, dan Perlindungan CSRF

Aplikasi berbasis sesi menyimpan identitas pengguna di sisi server setelah login sehingga setiap permintaan berikutnya dapat dikaitkan dengan konteks keamanan yang sama. Perlindungan terhadap pemalsuan permintaan lintas situs (*Cross-Site Request Forgery*) memerlukan token pada formulir yang divalidasi oleh server. Autentikasi membedakan peserta, admin, dan super admin, sementara registrasi administrator pada subdomain memakai verifikasi email untuk memastikan keabsahan akun penyelenggara. Kombinasi autentikasi, sesi, dan CSRF membentuk lapisan kontrol akses yang selaras dengan middleware RBAC karena validasi token acak (*nonce*) secara efektif mengurangi risiko CSRF pada aplikasi web (Ele, 2024).

## 13. Axios dan Permintaan HTTP pada Sisi Klien

Axios merupakan klien HTTP berbasis Promise yang digunakan pada *frontend* untuk berkomunikasi dengan endpoint aplikasi secara asinkron, misalnya saat memeriksa status pembayaran tanpa memuat ulang seluruh halaman. Pola permintaan asinkron secara teoritis mengurangi pemblokiran antarmuka dan meningkatkan responsivitas dibanding navigasi penuh secara tradisional. Penelitian perbandingan performa RESTful API antara Express.js dan Laravel menunjukkan bahwa pola permintaan HTTP perlu dipertimbangkan dalam perancangan interaksi klien–server. Axios melengkapi JavaScript dengan abstraksi permintaan yang terstandarisasi untuk mendukung umpan balik cepat setelah pembayaran atau pembaruan status (Hadinata & Stianingsih, 2024).

## 14. Manajemen Penyimpanan Berkas dan Unggahan Dokumen

Unggahan dokumen pendaftaran, materi kursus, dan berkas sertifikat memerlukan validasi tipe MIME dan ukuran serta pembatasan akses unduhan. Berkas disimpan pada lokasi yang terpisah dari kode aplikasi guna mengurangi risiko eksekusi berkas berbahaya dan memudahkan pencadangan. Survei keamanan aplikasi web berbasis OWASP menegaskan bahwa celah pada jalur unggah dan validasi input harus diaudit secara sistematis. Aplikasi ini menerapkan pembatasan format dan ukuran pada formulir sesuai praktik keamanan tersebut (Shahid et al., 2022).

## 15. Chart.js

Chart.js adalah pustaka JavaScript sisi klien untuk menggambar grafik statistik pada elemen *canvas* HTML5 berdasarkan data yang disediakan server melalui Blade. Dalam dasbor administrasi, visualisasi tren pendaftaran, pembayaran, atau distribusi status peserta memudahkan pengambilan keputusan operasional. Teori presentasi informasi menyatakan bahwa *encoding* visual yang tepat mempercepat interpretasi pola dibanding hanya teks atau angka terpisah. Pustaka ini dimuat melalui CDN resmi dengan versi tetap sehingga pemeliharaan dependensi *frontend* tetap terkendali tanpa membesarkan bundel Vite secara berarti (Zhang et al., 2025).

## 16. Pustaka Dompdf

Dompdf mengubah dokumen HTML dan CSS menjadi berkas PDF pada sisi server sehingga sertifikat dapat dihasilkan dari templat Blade. Integrasi paket `barryvdh/laravel-dompdf` membungkus Dompdf sebagai layanan Laravel dengan injeksi dependensi yang konsisten. Secara teoritis penjanaan PDF mendukung distribusi resmi dokumen kelulusan tanpa bergantung pada pengolah kata di sisi klien. Literatur tentang sistem sertifikat digital yang mematuhi standar internasional menegaskan bahwa dokumen resmi dapat dibentuk dari templat terstruktur dan dibagikan secara terkendali; hal ini sejalan dengan kebutuhan menghasilkan PDF dari templat HTML/CSS serta membatasi akses sesuai kebijakan penyimpanan agar templat tidak disalahgunakan (Yu et al., 2023).

## 17. Pendekatan Agile

*Agile* adalah pendekatan pengembangan perangkat lunak yang menekankan adaptasi terhadap perubahan, pengembangan iteratif, serta kolaborasi dengan pemangku kepentingan dibanding menuntut spesifikasi lengkap di awal proyek. Manifesto for Agile Software Development menekankan individu dan interaksi, perangkat lunak yang berfungsi, kolaborasi klien, serta respons terhadap perubahan. Pendekatan ini relevan bagi sistem KPP yang memiliki banyak modul sehingga dikembangkan secara bertahap dan diuji sebelum diperluas. Kajian berbasis data skala besar terhadap repositori perangkat lunak menunjukkan bahwa pola pengembangan Agile dapat dipetakan secara sistematis dalam ekosistem terbuka, dan dalam penelitian ini nilai-nilai Agile mengatur prioritas fitur pada `Program` sedangkan Scrum mengoperasionalkannya melalui peran, artefak, dan *sprint* (Moreno Martínez et al., 2024).

## 18. Metode Scrum

**Scrum** adalah metode berupa kerangka kerja (*framework*) dalam keluarga pendekatan Agile yang menyediakan peran tetap, artefak, dan acara berulang untuk mengelola pengembangan produk kompleks. Scrum memakai Product Backlog dan Sprint serta peran Product Owner, Scrum Master, dan tim pengembang untuk menjaga transparansi dan akuntabilitas progres. Acara seperti perencanaan *sprint*, *daily scrum*, tinjauan *sprint*, dan retrospektif mendukung inspeksi dan adaptasi berkelanjutan. Pada Biara Loresa SCJ SP3 Scrum dipetakan ke perencanaan kebutuhan, implementasi bertahap modul Laravel, serta pengujian fungsional sebelum integrasi penuh sebagaimana praktik terbaik pengembangan perangkat lunak berbasis DevOps dan Scrum yang disintesis dari tinjauan literatur berskala besar (Pastrana et al., 2025).