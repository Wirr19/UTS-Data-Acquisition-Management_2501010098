# UTS Data Acquisition and Management (DAM)  
## Indonesia Tourism Dataset

Proyek ini merupakan tugas Ujian Tengah Semester (UTS) mata kuliah **Data Acquisition and Management (DAM)**. Proyek berfokus pada proses akuisisi, pengumpulan, pengolahan, penggabungan, dan pemeriksaan kualitas serta etika penggunaan data pariwisata di Indonesia.

## Tujuan Proyek

1. Mengumpulkan data destinasi wisata di Indonesia dari sumber data yang tersedia.
2. Melakukan akuisisi data menggunakan metode yang sesuai.
3. Mengumpulkan data pendukung cuaca dari Open-Meteo.
4. Melakukan pembersihan dan pengolahan data.
5. Menggabungkan data menjadi dataset yang siap dianalisis.
6. Mendokumentasikan sumber data dan memeriksa aspek etika dalam proses akuisisi.

## Sumber Data

Proyek ini menggunakan beberapa sumber data:

| Sumber | Kegunaan |
|---|---|
| Kaggle – Indonesia Tourism Destination | Data utama destinasi wisata |
| Wikipedia | Data pendukung terkait informasi pariwisata |
| Open-Meteo API | Data cuaca untuk beberapa kota di Indonesia |

**Dataset utama:**

[Indonesia Tourism Destination – Kaggle](https://www.kaggle.com/datasets/aprabowo/indonesia-tourism-destination)

**Dokumentasi Open-Meteo:**

https://open-meteo.com/

**Ketentuan penggunaan Kaggle:**

https://www.kaggle.com/terms

> Catatan: Status lisensi formal dan asal sebagian data Kaggle masih memerlukan verifikasi. Oleh karena itu, proyek tidak menganggap seluruh aspek lisensi telah terkonfirmasi.

## Wilayah Pengumpulan Data

Pengumpulan data cuaca dilakukan pada lima kota:

- Jakarta
- Bandung
- Yogyakarta
- Semarang
- Surabaya

## Struktur Repository

```text
UTS_DAM_Indonesia_Tourism/
│
├── UTS_DAM_Indonesia_Tourism.ipynb
│
├── data/
│   ├── raw/
│   │   ├── tourism_with_id.csv
│   │   ├── halaman_wikipedia.html
│   │   ├── openmeteo_Bandung.json
│   │   ├── openmeteo_Jakarta.json
│   │   ├── openmeteo_Semarang.json
│   │   ├── openmeteo_Surabaya.json
│   │   ├── openmeteo_Yogyakarta.json
│   │   └── robots_txt_evidence.txt
│   │
│   └── processed/
│       ├── data_ethics_checklist.csv
│       └── merged_dataset.metadata.json
│
├── docs/
│   ├── provenance.csv
│   ├── robots_check.json
│   └── scraping_meta.json
│
└── README.md
```

## Penjelasan Folder

### 1. Notebook

`UTS_DAM_Indonesia_Tourism.ipynb` merupakan notebook utama yang berisi kode program dan tahapan pengerjaan UTS, mulai dari akuisisi data hingga pengolahan dan pemeriksaan data.

### 2. data/raw/

Folder ini menyimpan data mentah yang diperoleh dari sumber data sebelum melalui proses pengolahan lebih lanjut.

Contohnya:
- File CSV dataset pariwisata.
- File HTML hasil pengambilan halaman Wikipedia.
- File JSON hasil pengambilan data cuaca Open-Meteo.
- Bukti pemeriksaan robots.txt.

### 3. data/processed/

Folder ini menyimpan hasil pengolahan dan dokumentasi pemeriksaan data, seperti:
- Checklist etika akuisisi data.
- Metadata dataset hasil penggabungan.

### 4. docs/

Folder ini berisi dokumentasi proses akuisisi data, seperti:
- `provenance.csv`: mencatat sumber dan asal data.
- `robots_check.json`: menyimpan hasil pemeriksaan robots.txt.
- `scraping_meta.json`: menyimpan metadata proses scraping.

## Tahapan Pengerjaan

Secara umum, proses pengerjaan proyek dilakukan melalui tahapan berikut:

1. **Data Acquisition**  
   Mengumpulkan data destinasi wisata dari dataset Kaggle serta data pendukung dari Wikipedia dan Open-Meteo.

2. **Data Collection**  
   Menyimpan data hasil akuisisi dalam format CSV, HTML, dan JSON.

3. **Data Cleaning**  
   Memeriksa dan menyiapkan data agar dapat digunakan pada proses berikutnya.

4. **Data Integration**  
   Menggabungkan data yang diperlukan menjadi dataset hasil pengolahan.

5. **Data Validation**  
   Melakukan pemeriksaan terhadap struktur, kelengkapan, dan kualitas data.

6. **Data Ethics Check**  
   Memeriksa aspek etika akuisisi data, termasuk sumber data, lisensi, robots.txt, identifikasi informasi pribadi, serta dokumentasi provenance.

## Pemeriksaan Etika Data

Proyek ini menerapkan pemeriksaan etika untuk memastikan proses akuisisi dilakukan secara bertanggung jawab.

Beberapa aspek yang diperiksa meliputi:

- Tujuan penggunaan data.
- Informasi lisensi dan ketentuan penggunaan sumber.
- Asal-usul data.
- Pemeriksaan potensi informasi pribadi.
- Pemeriksaan quasi-identifier.
- Pemeriksaan robots.txt.
- Penggunaan timeout, User-Agent, dan jeda permintaan.
- Pemeriksaan API key atau token.
- Dokumentasi provenance.

Beberapa aspek lisensi dan asal data masih berstatus **Perlu verifikasi**, sehingga tidak dianggap telah sepenuhnya terkonfirmasi.

## Teknologi yang Digunakan

- **Python** – bahasa pemrograman utama.
- **Jupyter Notebook / Google Colab** – lingkungan pengerjaan notebook.
- **Pandas** – pengolahan dan analisis data.
- **Requests** – pengambilan data dari sumber web/API.
- **JSON dan CSV** – format penyimpanan data.
- **Git dan GitHub** – version control dan penyimpanan repository.

## Cara Menjalankan Proyek

1. Clone repository:

   ```bash
   git clone URL_REPOSITORY
   ```

2. Masuk ke direktori proyek:

   ```bash
   cd UTS_DAM_Indonesia_Tourism
   ```

3. Install library yang dibutuhkan jika belum tersedia:

   ```bash
   pip install pandas requests beautifulsoup4
   ```

4. Buka notebook menggunakan Jupyter Notebook atau Google Colab.

5. Jalankan setiap cell secara berurutan sesuai tahapan pengerjaan.

Pastikan file dataset berada pada lokasi folder yang sesuai dengan path yang digunakan dalam notebook.

## Hasil Proyek

Hasil dari proyek ini berupa:

- Data mentah destinasi wisata dan data pendukung cuaca.
- Data hasil pengolahan dan penggabungan.
- Metadata dataset.
- Dokumentasi sumber data atau provenance.
- Bukti pemeriksaan robots.txt dan proses scraping.
- Checklist pemeriksaan etika akuisisi data.

## Penutup

Proyek ini menunjukkan penerapan proses Data Acquisition and Management melalui pengumpulan, penyimpanan, pengolahan, integrasi, dan dokumentasi data pariwisata Indonesia. Selain menghasilkan dataset yang dapat digunakan untuk analisis lebih lanjut, proyek ini juga memperhatikan aspek kualitas data, transparansi sumber, dan etika dalam proses akuisisi data.

---

**Mata Kuliah:** Data Acquisition and Management (DAM)  
**Jenis Tugas:** Ujian Tengah Semester (UTS)  
**Topik:** Indonesia Tourism Data Acquisition
