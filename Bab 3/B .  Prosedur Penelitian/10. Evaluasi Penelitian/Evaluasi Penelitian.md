# Evaluasi Penelitian

*Evaluasi penelitian* pada bagian ini merujuk pada kegiatan mengukur dan mendeskripsikan sejauh mana sistem memenuhi tujuan kebergunaan dari sudut pandang pengguna, melengkapi bukti fungsional dari pengujian perangkat lunak. *System Usability Scale* adalah instrumen baku berisi sepuluh pernyataan dengan skala respons untuk menghitung skor kebergunaan antara 0 hingga 100 per orang menurut rumus Brook, sehingga hasilnya dapat dibandingkan dengan penelitian sejenis dan ditafsirkan melalui rentang yang lazim dipakai pada rekayasa perangkat lunak berbasis pengalaman pemakaian.

Hubungan bagian ini dengan penelitian terletak pada jawaban terhadap rumusan masalah mengenai evaluasi kebergunaan sistem KPP berbasis web, tanpa menggantikan prosedur Scrum. Pengujian *black-box* pada *Increment Development & Testing* memverifikasi perilaku sesuai spesifikasi; *Sprint Review* mengumpulkan kesan kualitatif tiap iterasi; sedangkan SUS memberi ukuran terstandar terhadap kemudahan pemakaian setelah produk utuh dapat diuji. Evaluasi formatif dijadwalkan bersama kematangan *increment* per *sprint*, dan evaluasi sumatif dengan SUS diarahkan pada akhir Sprint 4 ketika modul prioritas telah terintegrasi.

Rincian berikut memuat **instrumen lengkap**, **skala jawaban**, dan **rumus skor** yang akan dipakai pada pelaksanaan; redaksi pernyataan mengacu versi Indonesia yang setara dengan kuesioner asli Brook dan konsisten dengan lembar jawaban responden pada lampiran hasil penelitian.

## Skala respons

Setiap pernyataan dijawab dengan memilih **satu** nilai pada skala Likert lima tingkat berikut.

**Tabel 1 Skala jawaban per pernyataan SUS**

| Nilai | Makna |
| --- | --- |
| 1 | Sangat tidak setuju |
| 2 | Tidak setuju |
| 3 | Netral |
| 4 | Setuju |
| 5 | Sangat setuju |

## Pernyataan kuesioner

Berikut sepuluh pernyataan yang akan tercetak pada lembar atau formulir elektronik. Nomor butir ganjil dan genap memengaruhi arah konversi pada perhitungan skor.

**Tabel 2 Pernyataan System Usability Scale versi Indonesia**

| No | Pernyataan |
| --- | --- |
| 1 | Saya berpikir akan sering menggunakan sistem ini. |
| 2 | Saya merasa sistem ini rumit secara tidak perlu. |
| 3 | Saya merasa sistem ini mudah digunakan. |
| 4 | Saya memerlukan bantuan teknis untuk dapat menggunakan sistem ini. |
| 5 | Saya menemukan berbagai fungsi dalam sistem ini terintegrasi dengan baik. |
| 6 | Saya merasa terlalu banyak inkonsistensi dalam sistem ini. |
| 7 | Saya membayangkan kebanyakan orang akan cepat belajar menggunakan sistem ini. |
| 8 | Saya merasa sistem ini sangat menyulitkan dalam penggunaan. |
| 9 | Saya merasa sangat percaya diri menggunakan sistem ini. |
| 10 | Saya perlu belajar banyak hal sebelum dapat mulai menggunakan sistem ini. |

## Rumus dan interpretasi skor

Untuk setiap butir ke-*i* dengan jawaban *R* pada skala 1 hingga 5, dihitung **kontribusi butir** *C* menurut aturan Brook:

- Butir **ganjil** nomor 1, 3, 5, 7, 9: kontribusi = *R* − 1, sehingga bernilai 0 hingga 4.
- Butir **genap** nomor 2, 4, 6, 8, 10: kontribusi = 5 − *R*, sehingga bernilai 0 hingga 4.

**Tabel 3 Ringkasan konversi butir**

| Nomor butir | Pola | Rumus kontribusi |
| --- | --- | --- |
| 1, 3, 5, 7, 9 | Ganjil | *C* = *R* − 1 |
| 2, 4, 6, 8, 10 | Genap | *C* = 5 − *R* |

Jumlah kontribusi keseluruhan:

**X** = jumlah kesepuluh kontribusi butir = *C*₁ + *C*₂ + … + *C*₁₀.

Nilai **X** berkisar antara 0 hingga 40. **Skor SUS** untuk satu responden:

**SUS** = 2,5 × **X**.

Skor akhir per orang berada pada rentang **0 hingga 100**. Interpretasi agregat mengacu rentang yang dipakai pada landasan metode, misalnya skor di bawah 51 sering dikategorikan tidak dapat diterima, rentang 51 hingga 73 marginal hingga baik, dan di atas 73 baik hingga sangat baik, dengan penyesuaian kutipan sumber pada bab landasan teori.

Pada tahap perencanaan, peneliti menyiapkan templat lembar yang memuat petunjuk pengisian, Tabel 1 dan Tabel 2 di atas, serta ruang jawaban per butir; setelah data terkumpul, perhitungan dilakukan sesuai rumus ini dan disajikan pada hasil penelitian.

## Tahap pelaksanaan evaluasi SUS

Pelaksanaan di lapangan mengikuti prasyarat baris Sprint 4 pada dokumen *Shippable Product*.

**Tabel 4 Tahap langkah-langkah evaluasi SUS**

| No | Tahap | Uraian |
| --- | --- | --- |
| 1 | Prasyarat *Shippable Product* | Memastikan keluaran Sprint 4 stabil; fitur pada baris tersebut dapat dioperasikan untuk skenario administrasi dan komunikasi internal layanan. |
| 2 | Lingkungan uji | URL atau akses aplikasi, akun per peran, data uji yang aman; mendukung alur end-to-end dari publik hingga administrasi akun. |
| 3 | Pengarahan responden | Menjelaskan tujuan penilaian tanpa mengarahkan jawaban butir; tugas ringkas mengikuti modul utama baris Sprint 4. |
| 4 | Sesi pemakaian | Responden menjalankan alur hingga cukup mengenal antarmuka untuk menilai pengalaman menyeluruh. |
| 5 | Pengisian SUS | Menggunakan lembar atau formulier yang memuat Tabel 1 skala, Tabel 2 pernyataan, dan kolom jawaban; diisi mandiri. |
| 6 | Pengolahan skor | Menerapkan Tabel 3 dan rumus SUS = 2,5 × X per responden; agregat deskriptif pada hasil penelitian. |
| 7 | Interpretasi | Mengacu rentang landasan metode; dapat dihubungkan dengan temuan kualitatif *Sprint Review* sprint sebelumnya. |
