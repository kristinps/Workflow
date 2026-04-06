# Pembahasan Increment Development & Testing

Pembahasan pada subbab ini melengkapi urutan Scrum setelah pemantauan harian: setiap iterasi diakhiri dengan *increment* yang dapat diintegrasikan ke repositori dan diuji secara *black-box* sesuai rencana pada Bab III. Cara menuju penyajian bukti di sini adalah dengan merangkum, per iterasi, **apakah keluaran perangkat lunak yang terbangun** selaras dengan rencana cakupan *increment* pada metodologi, lalu **apakah pemeriksaan perilaku dari sisi pengguna** membenarkan skenario pengujian yang direncanakan—tanpa menggantikan daftar kasus uji rinci pada lampiran atau subbab khusus.

Penyajian dibatasi pada ringkasan agar fokus Bab IV tetap pada sintesis capaian, sementara butir tugas per entri rencana kerja telah diuraikan pada pembahasan *Sprint Backlog*. Tabel berikut menyusun capaian *increment* dan capaian pengujian *black-box* dalam satu bidang pandang sehingga pembaca dapat menelusuri dari rencana Bab III ke konfirmasi pasca-pelaksanaan untuk tiap iterasi.

## Tabel ringkasan capaian Increment Development & Testing

| Sprint | Capaian increment | Capaian pengujian black-box |
| --- | --- | --- |
| Sprint 1 | *Increment* Sprint 1 terbangun memuat layanan publik, alur pendaftaran KPP, pembayaran nirtunai QRIS dengan pembaruan status, serta sesi peserta dengan dasbor dan status pendaftaran awal pada repositori pengembangan penelitian. | Pengujian *black-box* pada tampilan publik, formulir pendaftaran, alur pembayaran, serta otentikasi dan pembatasan akses menurut peran menunjukkan perilaku sesuai keluaran yang diharapkan pada kasus masukan valid dan penanganan tidak valid. |
| Sprint 2 | *Increment* Sprint 2 terbangun memuat layanan mandiri peserta untuk dokumen, jadwal, biaya, dan unduhan sertifikat serta panel pengelola untuk daftar pendaftaran, verifikasi dokumen, dan penugasan periode. | Pengujian *black-box* pada tampilan peserta dan tindakan pengelola menunjukkan pembaruan status dan tampilan yang konsisten setelah verifikasi maupun penolakan. |
| Sprint 3 | *Increment* Sprint 3 terbangun memuat pengelolaan periode dan materi, rekapitulasi kehadiran, biaya dan tagihan, serta berkas kelulusan dan akses sertifikat pada peserta. | Pengujian *black-box* pada siklus periode, kehadiran, tagihan, unggah kelulusan, serta unduh sertifikat dan status kelulusan pada peserta menunjukkan perilaku sesuai alur operasional KPP. |
| Sprint 4 | *Increment* Sprint 4 terbangun memuat pendaftaran akun pengelola dengan verifikasi surel serta modul pengelolaan akun administrator oleh pengawas utama. | Pengujian *black-box* pada alur verifikasi surel, aktivasi akses panel pengelola, serta operasi daftar akun administrator menunjukkan pembatasan akses menurut peran sesuai perancangan. |
