# Sprint Retrospective

Sprint Retrospective merupakan tahap refleksi tim pada akhir sprint untuk mengevaluasi proses kerja, mengidentifikasi hal yang sudah berjalan baik, serta menentukan perbaikan pada sprint berikutnya. Dalam penelitian ini, retrospektif dilakukan dengan mempertimbangkan kesesuaian proses pengembangan sistem informasi terhadap kebutuhan pengguna yang dirumuskan dalam `Kebutuhan user`.

## Tujuan Sprint Retrospective

1. Mengevaluasi efektivitas proses kerja tim selama sprint.
2. Mengidentifikasi hambatan yang memengaruhi pencapaian Sprint Goal.
3. Menetapkan tindakan perbaikan yang konkret untuk sprint berikutnya.
4. Meningkatkan kualitas kolaborasi dan hasil pengembangan sistem.

## Hasil Sprint Retrospective per Sprint


| Sprint   | Yang Berjalan Baik                                                                          | Yang Perlu Ditinggalkan                                                                           | Tindak Lanjutan Perbaikan                                                                               |
| -------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| Sprint 1 | Alur pendaftaran online dan unggah dokumen berhasil dibangun sesuai target awal.            | Praktik validasi input yang belum konsisten pada beberapa kondisi data.                           | Menstandarkan aturan validasi, menambah skenario uji form, dan merapikan pesan kesalahan input.         |
| Sprint 2 | Integrasi verifikasi dokumen dan pembayaran QRIS berjalan pada alur utama layanan.          | Pola sinkronisasi status pembayaran dan notifikasi yang belum stabil di beberapa kasus transaksi. | Memperjelas transisi status verifikasi-pembayaran dan memperketat pengujian integrasi transaksi.        |
| Sprint 3 | Modul periode, materi, dan kehadiran sudah dapat digunakan admin untuk operasional harian.  | Praktik pengelolaan jadwal yang belum sepenuhnya selaras dengan data peserta per periode.         | Memperbaiki relasi data, menambah validasi keterkaitan antar modul, dan uji ulang skenario operasional. |
| Sprint 4 | Modul pendukung (biaya, sertifikat, dashboard, profil, notifikasi) berhasil diintegrasikan. | Kebiasaan menunda perapian minor pada tampilan dan ringkasan informasi akhir.                     | Finalisasi antarmuka, retest end-to-end, serta penyempurnaan dokumentasi hasil pengembangan.            |


## Rencana Perbaikan Berkelanjutan

Tindak lanjut retrospektif difokuskan pada peningkatan kualitas validasi data, kestabilan integrasi antar modul, serta konsistensi tampilan antarmuka. Dengan pendekatan ini, proses pengembangan sistem informasi tetap adaptif, terkontrol, dan selaras dengan kebutuhan layanan yang diperoleh dari `Kebutuhan user`.