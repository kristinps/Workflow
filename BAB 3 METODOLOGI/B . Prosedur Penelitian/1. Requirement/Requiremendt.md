# Requirement

**Kebutuhan sistem** pada literatur rekayasa perangkat lunak sering disebut *requirement*. Istilah tersebut menyatakan apa yang harus dipenuhi oleh suatu sistem informasi agar layanan berjalan sesuai harapan pengguna dan pembimbing organisasi. Pengelompokan lazim membedakan kebutuhan fungsional yang meliputi perilaku layanan, data, dan alur kerja, serta kebutuhan non-fungsional yang meliputi kinerja, keamanan, dan lingkungan operasi. Keduanya menjadi dasar perancangan, prioritas pengembangan, dan pengujian.

Penelitian ini merancang sistem informasi pendaftaran untuk Kursus Persiapan Perkawinan, selanjutnya disebut KPP, di Biara Loresa SCJ SP3. Identifikasi kebutuhan mengacu pada **wawancara pada 15 Februari 2026** bersama **Pastor Markus Apriyono**, SCJ, selaku Direktur Biara, yang memetakan seluruh alur layanan dari pendaftaran hingga sertifikat. Temuan lapangan menunjukkan bahwa pendaftaran, berkas, dan administrasi biaya masih banyak bersifat tidak terkomputerisasi dan tidak terpadu, sehingga verifikasi memakan waktu dan ketertelusuran data peserta kurang konsisten. Atas dasar itu diperlukan sistem terintegrasi yang mendukung unggah dan verifikasi dokumen, pembayaran tercatat, serta layanan informasi bagi peserta dan pengelola.

Untuk menyajikan kebutuhan fungsional secara ringkas dan terarah sebelum dilanjutkan ke infrastruktur, diagram, dan perincian lainnya pada subbab berikut, ringkasan **fitur utama** beserta **keterangan** pelaksanaannya dalam empat tema besar layanan KPP disajikan pada **Tabel 1**.

**Tabel 1 Ringkasan fitur utama kebutuhan fungsional sistem KPP**

| No  | Fitur                                                       | Keterangan                                                                                                                                                                                    |
| --- | ----------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Pendaftaran berbasis web dan manajemen dokumen digital      | Menggantikan prosedur konvensional berbasis dokumen fisik. Mendukung unggah berkas, verifikasi oleh pengelola, peningkatan ketertelusuran, serta pengurangan ketergantungan pada arsip fisik. |
| 2   | Pembayaran elektronik melalui QRIS dengan layanan Midtrans               | Menyatukan administrasi biaya agar tercatat dan dapat diaudit. Mengurangi ketergantungan pada transaksi tunai sehingga akuntabilitas dan transparansi meningkat.                              |
| 3   | Modul terpadu periode, materi, jadwal, kehadiran, dan biaya | Mengintegrasikan data operasional KPP yang sebelumnya berjalan terpisah antar tahap layanan dalam satu alur terkelola.                                                                        |
| 4   | Alur kelulusan dan sertifikat digital                       | Menyediakan dokumentasi resmi sesuai tata kelola sistem informasi. Mendukung penerbitan dan unduhan sertifikat bagi peserta yang memenuhi persyaratan.                                        |


---

Agar sistem informasi berbasis web ini dapat dikembangkan, diuji, dan dioperasikan secara layak, diperlukan infrastruktur server dan nama domain dengan spesifikasi serta biaya yang selaras dengan beban aplikasi web, penyimpanan basis data, berkas unggahan peserta, serta layanan pembayaran. Ringkasan komponen, spesifikasi, dan biaya disajikan pada **Tabel 2**.

**Tabel 2 Komponen infrastruktur dan estimasi biaya operasional**

| Komponen | Spesifikasi                               | Biaya               |
| -------- | ----------------------------------------- | ------------------- |
| Server   | 2 core, 2 GB RAM, 40 GB, Ubuntu 20.04 LTS | Rp 60.000 per bulan |
| Domain   | biarascj.my.id                            | Rp 5.500 per tahun  |


---

Pengembangan sistem direncanakan memakai kerangka aplikasi web beserta perangkat kerja untuk pengkodean dan pengujian lokal. Kebutuhan fungsional berikut divisualisasikan dalam diagram perencanaan ringkas, sedangkan rincian struktur data, aturan akses, dan antarmuka dijabarkan pada tahap perancangan dan pembangunan.

**Diagram 1 — Hirarki pembagian akses halaman peserta dan pengelola.** Diagram berikut menyusun akses secara bertingkat dari layanan publik, panel peserta, panel pengelola yang mencakup wewenang pengawas utama, hingga jalur khusus pendaftaran akun pengelola, sebagai gambaran perencanaan tanpa menyebut rinci rute teknis.

```mermaid
flowchart TB
    AKSES["Perencanaan akses sistem KPP"]
    AKSES --> PUB["Layanan publik"]
    AKSES --> PST["Panel peserta"]
    AKSES --> ADM["Panel pengelola"]
    AKSES --> REG["Jalur pendaftaran akun pengelola"]

    PUB --> P1["Beranda, profil, berita, galeri, kontak"]
    PUB --> P2["Form KPP, konfirmasi, pembayaran pendaftaran"]

    PST --> S1["Status pendaftaran, dokumen, jadwal, biaya, sertifikat"]
    PST --> S2["Profil dan kata sandi"]

    ADM --> D1["Daftar pendaftaran dan verifikasi dokumen"]
    ADM --> D2["Periode, materi, kehadiran, biaya, sertifikat"]
    ADM --> D3["Pengawas utama mengelola akun pengelola"]

    REG --> R1["Registrasi dan verifikasi surel"]
```



**Diagram 2 — Diagram kelas UML perspektif peserta terhadap basis data.** Diagram ini menonjolkan kelompok data yang terutama dibaca maupun diisi peserta melalui akun dan data pendaftaran, meliputi hubungan antar pendaftaran, periode kursus, materi, kehadiran, tagihan biaya, surat kelulusan, dan pesan informasi.

```mermaid
classDiagram
    direction TB
    class User {
        +id UUID
        +email
        +role
    }
    class PendaftaranPernikahan {
        +id UUID
        +user_id
        +periode_id
        +status_pembayaran
        +status_dokumen
    }
    class PeriodePernikahan {
        +id UUID
        +nama
    }
    class MateriKursus {
        +id UUID
        +periode_id
        +judul
    }
    class KehadiranKursus {
        +id UUID
        +pendaftaran_id
        +materi_kursus_id
    }
    class Biaya {
        +id UUID
        +periode_id
    }
    class BiayaTagihan {
        +id UUID
        +biaya_id
        +pendaftaran_id
        +status
    }
    class SuratKelulusan {
        +id UUID
        +pendaftaran_id
        +file
    }
    class PesanDashboard {
        +id UUID
        +user_id
        +dari_user_id
    }
    User "1" --> "*" PendaftaranPernikahan
    PendaftaranPernikahan "*" --> "0..1" PeriodePernikahan
    PeriodePernikahan "1" --> "*" MateriKursus
    PendaftaranPernikahan "1" --> "*" KehadiranKursus
    MateriKursus "1" --> "*" KehadiranKursus
    PendaftaranPernikahan "1" --> "*" BiayaTagihan
    Biaya "1" --> "*" BiayaTagihan
    Biaya "*" --> "0..1" PeriodePernikahan
    PendaftaranPernikahan "1" --> "*" SuratKelulusan
    User "1" --> "*" PesanDashboard
```



**Diagram 3 — Diagram kelas UML perspektif pengelola terhadap basis data.** Diagram ini menekankan entitas yang menjadi pusat tata kelola operasional: periode sebagai induk materi dan kehadiran, biaya dan tagihan, serta pendaftaran yang diverifikasi dan ditautkan ke surat kelulusan.

```mermaid
classDiagram
    direction TB
    class PeriodePernikahan {
        +id UUID
        +nama
        +tanggal_mulai
        +tanggal_selesai
    }
    class MateriKursus {
        +id UUID
        +periode_id
        +judul
    }
    class KehadiranKursus {
        +id UUID
        +pendaftaran_id
        +materi_kursus_id
    }
    class Biaya {
        +id UUID
        +periode_id
        +nominal
    }
    class PendaftaranPernikahan {
        +id UUID
        +periode_id
        +status_dokumen
        +status_kursus
    }
    class BiayaTagihan {
        +id UUID
        +biaya_id
        +pendaftaran_id
    }
    class SuratKelulusan {
        +id UUID
        +pendaftaran_id
        +file
    }
    PeriodePernikahan "1" --> "*" MateriKursus
    PeriodePernikahan "1" --> "*" Biaya
    PeriodePernikahan "1" --> "*" PendaftaranPernikahan
    PendaftaranPernikahan "1" --> "*" KehadiranKursus
    MateriKursus "1" --> "*" KehadiranKursus
    PendaftaranPernikahan "1" --> "*" BiayaTagihan
    Biaya "1" --> "*" BiayaTagihan
    PendaftaranPernikahan "1" --> "*" SuratKelulusan
```



**Diagram 4 — Alur fitur pendaftaran dan manajemen dokumen.** Alur mengikuti pengiriman formulir KPP, pembentukan data pendaftaran, unggah dokumen oleh peserta, serta putusan verifikasi oleh pengelola berupa persetujuan, penolakan per berkas, maupun permintaan perbaikan.

```mermaid
flowchart TD
    A[Mulai] --> B[Isi dan kirim form KPP]
    B --> C[Data tersimpan pada PendaftaranPernikahan]
    C --> D[Peserta masuk ke area peserta]
    D --> E[Unggah dokumen persyaratan]
    E --> F[Pengelola tinjau dokumen]
    F --> G{Disetujui?}
    G -->|Ya| H[Status dokumen memadai dan lanjut alur]
    G -->|Perlu perbaikan| I[Peserta perbaiki unggahan]
    I --> E
    H --> J[Selesai tahap dokumen]
```



**Diagram 5 — Alur fitur pembayaran QRIS melalui Midtrans.** Diagram ini menggambarkan rencana alur mulai dari penayangan halaman pembayaran, penyiapan kode pembayaran nirtunai, pembayaran oleh peserta, hingga konfirmasi lunas melalui penyedia layanan pembayaran dan pemeriksaan status transaksi.

```mermaid
flowchart TD
    A[Buka halaman pembayaran beridentitas] --> B{QRIS ada dan belum kedaluwarsa?}
    B -->|Tidak| C[Menghasilkan token QRIS Midtrans]
    B -->|Ya| D[Tampilkan kode QR maupun Snap]
    C --> D
    D --> E[Pembayaran oleh peserta]
    E --> F[Panggilan balik Midtrans maupun pemeriksaan status]
    F --> G{Penyelesaian transaksi?}
    G -->|Ya| H[status_pembayaran = lunas]
    G -->|Belum| D
    H --> I[Selesai]
```



**Diagram 6 — Alur fitur modul terpadu periode, materi, jadwal, kehadiran, dan biaya.** Alur merangkum urutan operasi pengelola: menentukan periode, menambah materi dan menyebarkan jadwal, mencatat kehadiran per materi, serta mengelola biaya dan tagihan terkait periode.

```mermaid
flowchart TD
    A[Pengelola] --> B[Membuat maupun mengubah PeriodePernikahan]
    B --> C[Tambah MateriKursus per periode]
    C --> D[Kirim informasi jadwal ke peserta]
    D --> E[Catat KehadiranKursus per materi]
    E --> F[Tetapkan Biaya dan BiayaTagihan per periode]
    F --> G[Data operasional terpadu]
```



**Diagram 7 — Alur fitur kelulusan dan sertifikat digital.** Alur menghubungkan pencatatan kelulusan pada data pendaftaran dengan berkas sertifikat yang dapat diakses peserta pada bagian layanan kelulusan dan sertifikat.

```mermaid
flowchart TD
    A[Pengelola] --> B[Kelola SuratKelulusan untuk pendaftaran]
    B --> C[Berkas disimpan pada entitas surat]
    C --> D[Peserta buka halaman sertifikat]
    D --> E[Mengunduh maupun melihat status kelulusan]
    E --> F[Selesai]
```



Hak akses direncanakan dibedakan menurut peran. Halaman publik dapat diakses tanpa masuk sistem. Layanan peserta dan layanan pengelola memerlukan masuk sistem dan wewenang masing-masing. Pengelola tingkat utama direncanakan memiliki wewenang tambahan untuk mengatur akun pengelola lain dibanding pengelola biasa.
