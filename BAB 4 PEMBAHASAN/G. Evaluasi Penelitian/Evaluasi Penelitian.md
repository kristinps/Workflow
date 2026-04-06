# Pembahasan Evaluasi Penelitian

Pembahasan pada subbab ini mengarah pada jawaban rumusan masalah mengenai evaluasi kebergunaan sistem KPP berbasis web melalui *System Usability Scale* (SUS), mengacu pada subbab *Evaluasi Penelitian* dan urutan tahapan evaluasi SUS pada Bab III. Cara menuju penyajian agregat di bawah adalah dengan mendokumentasikan **pelaksanaan tiap tahap** secara berurutan—mulai dari prasyarat produk yang siap diuji setelah iterasi pengembangan terakhir, persiapan lingkungan uji, pengarahan responden, sesi pemakaian, pengisian kuesioner, pengolahan skor, hingga interpretasi—sehingga jejak metodologis tetap dapat diaudit tanpa menggantikan lampiran lembar jawaban per orang.

Evaluasi ini melengkapi pembahasan pengujian *increment* (kecocokan fungsional teruji) dan pembahasan tinjauan per iterasi dengan **ukuran terstandar kemudahan pemakaian** setelah responden menjalankan sistem secara menyeluruh. Tabel-tabel berikut merangkum tahapan pelaksanaan, konteks pengumpulan data, demografi, skor per responden, serta agregat; lampiran per responden mendukung bukti butir demi butir.

**Hasil yang diharapkan dari subbab ini** dijelaskan secara bertingkat: pertama, apakah prosedur evaluasi dilaksanakan utuh dan dapat diaudit; kedua, apakah sampel responden memberi konteks yang relevan terhadap layanan; ketiga, bagaimana sebaran dan agregat skor SUS menunjukkan persepsi kebergunaan secara kuantitatif; keempat, bagaimana temuan itu menjawab rumusan masalah dan sejajar dengan kesan kualitatif selama pengembangan.

**Lampiran per responden:** lembar jawaban lengkap disertakan dalam bundel lampiran evaluasi SUS (satu berkas per orang; penamaan berkas mengikuti penanda responden yang tercantum pada tabel demografi di bawah).

## Tabel 1 Ringkasan capaian pelaksanaan tahap evaluasi SUS

| No | Tahap | Capaian pelaksanaan |
| --- | --- | --- |
| 1 | Prasyarat *Shippable Product* | Keluaran Sprint 4 pada lingkungan pengembangan penelitian telah memuat modul administrasi akun pengelola, verifikasi surel, pengawasan akun administrator, dan fitur pesan pada dasbor sesuai dokumen *Shippable Product*; skenario dari layanan publik hingga peran pengawas utama dapat dijalankan tanpa kegagalan fungsional yang menghambat sesi uji. |
| 2 | Lingkungan uji | Aplikasi diakses melalui URL pada server penelitian dengan sertifikat HTTPS; disediakan akun uji terpisah untuk peran calon peserta, peserta, pengelola, pengawas utama, dan jalur pendaftaran akun pengelola; data pendaftaran dan dokumen memakai contoh fiktif yang tidak memuat data pribadi sensitif. |
| 3 | Pengarahan responden | Sebelum pemakaian, responden menerima penjelasan singkat bahwa tujuan sesi adalah menilai kemudahan memakai sistem, bukan menguji kemampuan pribadi; disampaikan daftar tugas ringkas menelusuri informasi publik, pendaftaran, dasbor peserta, serta panel pengelola sesuai peran masing-masing, tanpa membahas isi pernyataan SUS. |
| 4 | Sesi pemakaian | Responden mengeksplorasi antarmuka secara mandiri dengan bantuan teknis hanya jika terjadi kegagalan akses; durasi rata-rata sekitar 25 menit hingga responden menyatakan siap mengisi kuesioner. |
| 5 | Pengisian SUS | Sepuluh responden mengisi lembar kuesioner SUS berbahasa Indonesia dengan sepuluh pernyataan dan skala Likert lima tingkat; tidak ada lembar yang tidak lengkap sehingga layak diolah. |
| 6 | Pengolahan skor | Jawaban dikonversi ke kontribusi butir menurut aturan Brook, dijumlahkan, dan dikalikan 2,5 sehingga diperoleh skor 0–100 per responden; skor individu merupakan kelipatan 2,5 sesuai rumus standar. |
| 7 | Interpretasi | Skor rata-rata jatuh pada rentang yang pada landasan metode ditafsirkan sebagai kebergunaan **baik**; temuan ini selaras dengan kesan umum pada tinjauan iteratif pengembangan bahwa alur utama dapat diikuti meskipun masih ada saran perbaikan label pada beberapa layar. |

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

## Uraian hasil evaluasi

Pelaksanaan evaluasi berjalan lengkap sesuai rangkaian tahap pada Tabel 1. Prasyarat produk siap uji terpenuhi sehingga responden dapat menelusuri alur mulai dari informasi publik hingga tugas administratif tanpa kegagalan fungsional yang menghentikan sesi. Lingkungan uji memakai akses aman ke server penelitian, akun contoh per peran, serta data fiktif sehingga etika dan kendali skenario tetap terjaga. Pengarahan memisahkan penilaian kemudahan dari tes kemampuan pribadi; sesi pemakaian mandiri berjalan rata-rata sekitar dua puluh lima menit hingga responden siap mengisi kuesioner. Seluruh lembar SUS terisi lengkap oleh sepuluh orang, lalu diolah dengan konversi butir dan skor 0–100 menurut rumus standar sehingga hasil agregat dapat dibandingkan dengan literatur kebergunaan.

Dari sisi sampel, sepuluh responden mencakup peran yang berbeda—mulai dari pengelola administrasi, staf pastoral, calon peserta dan alumni, pengawas akun, hingga perwakilan komunitas dan relawan—sehingga sudut pandang tidak terpaku pada satu jenis pengguna saja. Sebagian besar melaporkan pengalaman memakai aplikasi web sedang hingga sangat sering; hal ini membantu mengurangi risiko skor ekstrem hanya karena ketidakterbiasan terhadap antarmuka web, sekaligus tetap mempertahankan keragaman konteks pemakaian terhadap layanan KPP.

Distribusi skor per responden menunjukkan rentang 65,00 hingga 82,50. Nilai terendah masih berada pada wilayah interpretasi marginal hingga baik, sementara nilai tertinggi masuk kategori baik hingga sangat baik; sebagian besar skor individu berkisar sekitar 70–77,5 dengan beberapa jawaban di sekitar batas atas rentang marginal–baik. Pola tersebut mengindikasikan bahwa persepsi kemudahan relatif homogen: tidak ada responden yang memberi indikasi kebergunaan “tidak dapat diterima” menurut ambang umum SUS, dan hanya sebagian kecil yang berada dekat ambang bawah rentang “baik”. Dengan simpangan baku agregat yang moderat, dapat dibaca bahwa variasi antar individu lebih mencerminkan nuansa peran atau preferensi antarmuka daripada ketidakstabilan sistem pada skenario uji.

Pada tingkat agregat, skor rata-rata 74,00 berada di atas ambang umum yang sering dipakai untuk menafsirkan kebergunaan sebagai “baik”, dengan simpangan baku 4,90 yang menunjukkan konsensus moderate antar responden. Nilai minimum dan maksimum (65,00 dan 82,50) menggambarkan bahwa meskipun ada variasi, seluruh titik data tetap dalam spektrum yang dapat diterima hingga kuat untuk konteks produk informasi pelayanan. Temuan kuantitatif ini selaras dengan ringkasan tahap interpretasi pada Tabel 1 serta dengan kesan umum selama tinjauan iteratif bahwa alur utama dapat dijalankan, dengan ruang perbaikan pada label dan pesan bantuan yang tidak mengubah kesimpulan utama kebergunaan.

Rentang interpretasi mengacu pada klasifikasi umum SUS: di bawah 51 tidak dapat diterima; 51–73 marginal hingga baik; di atas 73 baik hingga sangat baik, dengan penyesuaian kutipan pada landasan metode. Skor per orang dihitung dari lembar jawaban pada lampiran per responden.

## Agregasi dan sintesis

| Ukuran | Nilai |
| --- | --- |
| Rata-rata skor SUS | 74,00 |
| Simpangan baku | 4,90 |
| Nilai minimum dan maksimum | 65,00 dan 82,50 |

**Sintesis:** Secara menyeluruh, temuan evaluasi menjawab rumusan masalah mengenai kebergunaan sistem pendaftaran dan manajemen KPP berbasis web dalam konteks sampel dan periode pengujian yang dilaporkan. Skor SUS rata-rata **74,00** menempatkan sistem pada interpretasi **baik** menurut kerangka umum SUS; disertai simpangan baku **4,90**, hasil ini tidak menunjukkan perbedaan persepsi yang ekstrem antar responden, melainkan konsolidasi opini bahwa antarmuka dan alur utama relatif mudah dipahami setelah pemakaian menyeluruh. Rentang skor individu tetap dalam batas yang layak untuk layanan administratif: tidak ada indikasi kegagalan kebergunaan menyeluruh, sementara nilai puncak mendukung adanya bagian alur yang dianggap sangat mulus oleh sebagian pengguna.

Temuan kuantitatif tersebut **menguatkan** kesan kualitatif selama pengembangan—khususnya bahwa alur layanan utama dapat dioperasikan end-to-end—tanpa meniadakan saran perbaikan pada aspek presentasi, seperti penamaan menu, kejelasan label, dan pesan bantuan pada beberapa layar. Saran tersebut bersifat penyempurnaan pengalaman pengguna dan dapat ditindaklanjuti pada pengembangan berikutnya di luar ruang lingkup skripsi. Dengan demikian, evaluasi SUS berfungsi sebagai **bukti pelengkap** bahwa di samping kebenaran fungsional melalui pengujian *black-box*, sistem juga menerima penilaian kemudahan pemakaian yang mendukung penerimaan pengguna pada lingkungan uji penelitian, dengan catatan bahwa generalisasi di luar sampel sepuluh responden dan setting uji tetap memerlukan kehati-hatian metodologis.
