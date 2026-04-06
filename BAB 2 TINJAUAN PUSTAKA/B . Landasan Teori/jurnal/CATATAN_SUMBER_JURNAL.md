# Catatan folder jurnal — selaras `Landasan Teori.md`

## Aturan utama: jumlah harus sama

| Yang dihitung | Jumlah |
|---------------|--------|
| Kutipan (paragraf pengantar + subbab `## 1.` … `## 18.`) di `Landasan Teori.md` | **19** |
| Berkas `*.pdf` di folder `jurnal/` ini | **19** |
| Awalan nomor pada nama PDF (`0_` … `18_`) | **tepat satu berkas per nomor** |

Jika Anda menambah atau mengurangi subbab di naskah, **sesuaikan juga** jumlah PDF dan nama berkas agar ketiga baris di atas tetap benar.

## Jumlah kutipan di naskah

Terdapat **19 kutipan** (satu paragraf pengantar + **18 subbab** `## 1.` … `## 18.`), masing-masing **satu sumber** di akhir paragraf.

| No. | Subbab di `Landasan Teori.md` | Kutipan | PDF di folder ini |
|-----|------------------------------|---------|-------------------|
| 0 | Paragraf pengantar (sebelum `## 1.`) | Ilyas et al., 2025 | Ya (`0_2025_...`) |
| 1 | `## 1.` | Zhou et al., 2025 | Ya |
| 2 | `## 2.` | Nugroho et al., 2022 | Ya |
| 3 | `## 3.` | Novia et al., 2022 | Ya |
| 4 | `## 4.` | More et al., 2025 | Ya |
| 5 | `## 5.` | Oktiriani et al., 2022 | Ya |
| 6 | `## 6.` | Bonteanu & Tudose, 2024 | Ya |
| 7 | `## 7.` | Gavriluță et al., 2022 | Ya (`7_2022_...`) |
| 8 | `## 8.` | Pfuño Alccahuamani et al., 2026 | Ya (`8_2026_...`) |
| 9 | `## 9.` | Sahani et al., 2022 | Ya |
| 10 | `## 10.` | Turker et al., 2022 | Ya (`10_2022_...`) |
| 11 | `## 11.` | Muchtar et al., 2024 | Ya (`11_2024_...`) |
| 12 | `## 12.` | Ele, 2024 | Ya |
| 13 | `## 13.` | Hadinata & Stianingsih, 2024 | Ya |
| 14 | `## 14.` | Shahid et al., 2022 | Ya |
| 15 | `## 15.` | Zhang et al., 2025 | Ya |
| 16 | `## 16.` | Yu et al., 2023 | Ya (`16_2023_...`) |
| 17 | `## 17.` | Moreno Martínez et al., 2024 | Ya (`17_2024_...`) |
| 18 | `## 18.` | Pastrana et al., 2025 | Ya (`18_2025_...`) |

**Saat ini:** **19 berkas PDF** untuk **19 kutipan** — lengkap. **Tidak ada pengulangan sumber:** setiap paragraf pengantar dan subbab `## 1.`–`## 18.` memakai **satu artikel berbeda** (penulis/tahun unik).

### Verifikasi cepat (PowerShell)

Setelah mengubah isi folder `jurnal`, jalankan di folder tersebut untuk memastikan ada **19** PDF dan **tidak ada duplikat/ nomor hilang** pada awalan `0_`…`18_`:

```powershell
$j = "c:\Users\agung\Documents\SKRIPSI\Bab 2\B . Landasan Teori\jurnal"
(Get-ChildItem -LiteralPath $j -Filter *.pdf).Count   # harus 19
$nums = (Get-ChildItem -LiteralPath $j -Filter *.pdf) | ForEach-Object { if ($_.Name -match '^(\d+)_') { [int]$Matches[1] } }
0..18 | ForEach-Object { if ($_ -notin $nums) { "Hilang: $_" } }
$nums | Group-Object | Where-Object Count -gt 1 | ForEach-Object { "Duplikat nomor: $($_.Name)" }
```

## Aturan penamaan berkas

```
{nomor_subbab}_{tahun}_{nama_singkat_penulis}_{judul_singkat}.pdf
```

- **nomor_subbab** = angka pada judul `## N.` di `Landasan Teori.md` (**0** hanya untuk paragraf pengantar).
- **§10** hanya satu jurnal (Turker et al., 2022); awalan **`10_`** (bukan `10_1_` / `10_2_`).

## Penggantian sumber (sumber lama tidak diunduh)

| Subbab | Kutipan lama | Kutipan pengganti | Catatan singkat |
|--------|----------------|-------------------|-------------------|
| 7 | Ha, 2022 | Gavriluță et al., 2022 | MDPI *Sustainability* — situs web pemerintah daerah / e-governance |
| 11 | Eren, 2022 | Muchtar et al., 2024 | *Cogent Business & Management* — adopsi QRIS (salinan dari folder Penelitian Terdahulu) |
| 16 | Wibowo et al., 2022 | Yu et al., 2023 | MDPI *Standards* — sistem sertifikat digital berstandar internasional |
| 17 | Alami & Krancher, 2022 | Moreno Martínez et al., 2024 | MDPI *Software* — karakteristik Agile dari repositori berskala besar |
| 18 | Rahutomo et al., 2022 | Pastrana et al., 2025 | MDPI *Applied Sciences* — tinjauan literatur DevOps dan Scrum |
| 8 | Yamin & Abdalatif, 2024 | Pfuño Alccahuamani et al., 2026 | MDPI *Computers* — Laravel MVC & antarmuka web responsif (mengganti kutipan QR agar tidak bentrok tema dengan §10–§11) |

Pastikan **identik** dengan entri daftar pustaka skripsi.
