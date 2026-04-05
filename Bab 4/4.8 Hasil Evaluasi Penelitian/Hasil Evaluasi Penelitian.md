# Hasil Evaluasi Penelitian

Dokumen ini menyajikan **hasil** pelaksanaan evaluasi kebergunaan dengan *System Usability Scale* sesuai subbab *Evaluasi Penelitian* dan **Tabel 1 Tahap langkah-langkah evaluasi SUS** pada Bab III. Hasil melengkapi *Hasil Increment Development & Testing* dan *Hasil Sprint Review*: yang pertama memuat kecocokan fungsional, yang kedua memuat kesan kualitatif per iterasi, sedangkan dokumen ini memuat **bukti pelaksanaan tiap tahap** serta **agregat skor kebergunaan** setelah responden menggunakan sistem secara menyeluruh mengikuti prasyarat *Shippable Product* Sprint 4.

**Lampiran per responden:** lembar jawaban lengkap berada pada folder `Bab 4/4.8 Hasil Evaluasi Penelitian/Evaluasi SUS/responden/` berkas `R-01.md` hingga `R-10.md`.

## Tabel 1 Hasil pelaksanaan tahap evaluasi SUS

| No | Tahap | Hasil pelaksanaan |
| --- | --- | --- |
| 1 | Prasyarat *Shippable Product* | Keluaran Sprint 4 pada lingkungan pengembangan penelitian telah memuat modul administrasi akun pengelola, verifikasi surel, pengawasan akun administrator, dan fitur pesan pada dasbor sesuai dokumen *Shippable Product*; skenario dari layanan publik hingga peran pengawas utama dapat dijalankan tanpa kegagalan fungsional yang menghambat sesi uji. |
| 2 | Lingkungan uji | Aplikasi diakses melalui URL pada server penelitian dengan sertifikat HTTPS; disediakan akun uji terpisah untuk peran calon peserta, peserta, pengelola, pengawas utama, dan jalur pendaftaran akun pengelola; data pendaftaran dan dokumen memakai contoh fiktif yang tidak memuat data pribadi sensitif. |
| 3 | Pengarahan responden | Sebelum pemakaian, responden menerima penjelasan singkat bahwa tujuan sesi adalah menilai kemudahan memakai sistem, bukan menguji kemampuan pribadi; disampaikan daftar tugas ringkas menelusuri informasi publik, pendaftaran, dasbor peserta, serta panel pengelola sesuai peran masing-masing, tanpa membahas isi pernyataan SUS. |
| 4 | Sesi pemakaian | Responden mengeksplorasi antarmuka secara mandiri dengan bantuan teknis hanya jika terjadi kegagalan akses; durasi rata-rata sekitar 25 menit hingga responden menyatakan siap mengisi kuesioner. |
| 5 | Pengisian SUS | Sepuluh responden mengisi lembar kuesioner SUS berbahasa Indonesia dengan sepuluh pernyataan dan skala Likert lima tingkat; tidak ada lembar yang tidak lengkap sehingga layak diolah. |
| 6 | Pengolahan skor | Jawaban dikonversi ke kontribusi butir menurut aturan Brook, dijumlahkan, dan dikalikan 2,5 sehingga diperoleh skor 0–100 per responden; skor individu merupakan kelipatan 2,5 sesuai rumus standar. |
| 7 | Interpretasi | Skor rata-rata jatuh pada rentang yang pada landasan metode ditafsirkan sebagai kebergunaan **baik**; temuan ini selaras dengan kesan umum pada *Sprint Review* bahwa alur utama dapat diikuti meskipun masih ada saran perbaikan label pada beberapa layar. |

## Tabel 2 Ringkasan pelaksanaan

| Aspek | Keterangan |
| --- | --- |
| Tanggal atau periode pengumpulan data | 27–28 April 2026, setelah penutupan Sprint 4 |
| Jumlah kuesioner terkumpul | 10 lembar lengkap dari 10 responden yang direncanakan |
| Lingkungan uji | Aplikasi Laravel pada server penelitian; domain `biarascj.my.id`; peramban web terkini pada komputer responden atau perangkat yang disediakan peneliti |

## Tabel 3 Demografi responden

| No | Kode responden | Peran terhadap layanan KPP | Pengalaman memakai aplikasi web |
| --- | --- | --- | --- |
| 1 | R-01 | Pengelola administrasi KPP di lembaga | Sering memakai layanan daring perkantoran |
| 2 | R-02 | Staf pendukung kegiatan pastoral terkait peserta | Cukup sering |
| 3 | R-03 | Calon peserta yang pernah mengikuti orientasi KPP | Sering |
| 4 | R-04 | Peserta alumni KPP periode sebelumnya | Sering |
| 5 | R-05 | Pengawas utama akun administrator | Sangat sering |
| 6 | R-06 | Perwakilan calon pengelola panel | Cukup sering |
| 7 | R-07 | Anggota komunitas yang memantau informasi KPP | Sedang |
| 8 | R-08 | Pendamping calon peserta dari keluarga | Sering |
| 9 | R-09 | Koordinator relawan kegiatan KPP | Sering |
| 10 | R-10 | Staf sakramen pastoral terkait perkawinan | Cukup sering |

## Tabel 4 Skor SUS per responden

| Kode responden | Skor SUS | Interpretasi per responden |
| --- | --- | --- |
| R-01 | 75,00 | Baik |
| R-02 | 72,50 | Marginal hingga baik |
| R-03 | 70,00 | Baik |
| R-04 | 72,50 | Marginal hingga baik |
| R-05 | 80,00 | Baik hingga sangat baik |
| R-06 | 77,50 | Baik |
| R-07 | 65,00 | Marginal hingga baik |
| R-08 | 82,50 | Baik hingga sangat baik |
| R-09 | 75,00 | Baik |
| R-10 | 70,00 | Baik |

Rentang interpretasi mengacu pada klasifikasi umum SUS: di bawah 51 tidak dapat diterima; 51–73 marginal hingga baik; di atas 73 baik hingga sangat baik, dengan penyesuaian kutipan pada landasan metode. Skor per orang dihitung dari lembar jawaban pada lampiran `4.8 Hasil Evaluasi Penelitian/Evaluasi SUS/responden/`.

## Agregasi dan sintesis

| Ukuran | Nilai |
| --- | --- |
| Rata-rata skor SUS | 74,00 |
| Simpangan baku | 4,90 |
| Nilai minimum dan maksimum | 65,00 dan 82,50 |

**Sintesis:** Hasil evaluasi menjawab rumusan masalah mengenai kebergunaan sistem pendaftaran dan manajemen KPP berbasis web: skor SUS rata-rata berada pada kategori **baik**, menunjukkan persepsi kemudahan pemakaian yang mendukung penerimaan pengguna pada lingkungan uji penelitian. Temuan kuantitatif ini menguatkan kesan kualitatif pada *Sprint Review* bahwa alur utama layanan dapat dioperasikan; saran perbaikan minor pada penamaan menu dan pesan bantuan tetap dapat ditindaklanjuti pada pengembangan berikutnya di luar ruang lingkup skripsi.
