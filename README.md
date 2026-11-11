# Akuisisi Data Akomodasi Kecamatan Kintamani

## Deskripsi Proyek

Proyek ini merupakan praktik akuisisi dan manajemen data yang bertujuan untuk mengumpulkan, mengolah, dan menganalisis data akomodasi di Kecamatan Kintamani, Kabupaten Bangli, Bali.

Pengambilan data dilakukan menggunakan **OpenStreetMap (OSM) melalui Overpass API** dengan bantuan Python. Data yang diperoleh mencakup berbagai jenis akomodasi, seperti hotel, guest house, hostel, chalet, dan motel.

Data hasil akuisisi kemudian melalui proses pengolahan dan pemeriksaan kualitas untuk mengetahui kelengkapan informasi, persebaran lokasi, serta kesesuaian data dengan sumber pembanding BPS.

## Tujuan Proyek

- Mengumpulkan data akomodasi di Kecamatan Kintamani menggunakan Overpass API.
- Mengolah data mentah JSON menjadi dataset berbentuk CSV.
- Melakukan pemeriksaan kualitas dan kelengkapan atribut data.
- Memvisualisasikan persebaran akomodasi berdasarkan koordinat geografis.
- Membandingkan jumlah data OpenStreetMap dengan data BPS.
- Melakukan verifikasi terhadap 10 sampel akomodasi secara manual.

## Teknologi dan Tools

- Python
- Google Colab / Jupyter Notebook
- OpenStreetMap (OSM)
- Overpass API
- Pandas
- Matplotlib
- GeoPandas

## Hasil Akuisisi Data

Berdasarkan proses pengambilan data pada 11 November 2026, diperoleh sebanyak **32 entitas akomodasi** di Kecamatan Kintamani.

| Jenis Akomodasi | Jumlah |
|---|---:|
| Hotel | 16 |
| Guest House | 9 |
| Hostel | 4 |
| Chalet | 2 |
| Motel | 1 |
| **Total** | **32** |

Hasil pemeriksaan spasial menunjukkan bahwa 31 objek berupa node dan 1 objek berupa way berhasil dipetakan di dalam wilayah Kecamatan Kintamani.

## Pengujian dan Validasi

Beberapa tahapan pemeriksaan yang dilakukan:

1. Pemeriksaan duplikasi berdasarkan identitas objek OpenStreetMap.
2. Pemeriksaan kelengkapan atribut, seperti nama, alamat desa, kelas bintang, jumlah kamar, dan website.
3. Pemeriksaan koordinat geografis.
4. Perbandingan jumlah data OSM dengan publikasi BPS Kecamatan Kintamani Dalam Angka 2025.
5. Verifikasi manual terhadap 10 sampel akomodasi.

Berdasarkan laporan, jumlah data OSM sebanyak 32 objek dibandingkan dengan 32 objek pada data pembanding BPS, sehingga menghasilkan rasio perbandingan sebesar **100%**.

## Temuan Kualitas Data

Beberapa permasalahan yang ditemukan selama proses pengolahan:

- Seluruh 32 objek tidak memiliki informasi alamat desa.
- Sebanyak 31 objek tidak mencantumkan kelas bintang.
- Sebanyak 30 objek tidak mencantumkan jumlah kamar dan website.
- Terdapat 1 objek tanpa nama akomodasi.

Data dengan atribut kosong tetap dipertahankan tanpa mengisi nilai dummy agar keaslian data dari sumber OpenStreetMap tetap terjaga.

## Hasil Akhir

Proyek ini menghasilkan dataset akomodasi Kecamatan Kintamani yang dapat digunakan sebagai data awal untuk analisis spasial dan penelitian terkait sektor pariwisata.

Selain dataset, proyek ini juga menghasilkan visualisasi peta persebaran, hasil pemeriksaan kualitas data, perbandingan dengan data BPS, serta dokumentasi hasil verifikasi sampel.

## Sumber Data

- OpenStreetMap: https://www.openstreetmap.org/
- Overpass API: https://overpass-api.de/
- BPS Kabupaten Bangli: https://banglikab.bps.go.id/

Data OpenStreetMap digunakan berdasarkan Open Database License (ODbL).

**Attribution:** © OpenStreetMap contributors.
