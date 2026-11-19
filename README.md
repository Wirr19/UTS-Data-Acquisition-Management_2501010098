# UTS Data Acquisition and Management – Indonesia Tourism

## Deskripsi
Proyek ini melakukan akuisisi, pemeriksaan, pengolahan, dan penggabungan data destinasi wisata Indonesia dengan data cuaca historis dan informasi wilayah pendukung.

## Sumber Data
- Kaggle – Indonesia Tourism Destination: https://www.kaggle.com/datasets/aprabowo/indonesia-tourism-destination
- Open-Meteo Historical API: https://open-meteo.com/
- Wikipedia – List of Indonesian cities by population: https://en.wikipedia.org/wiki/List_of_Indonesian_cities_by_population

## Cakupan
- Dataset destinasi: sekitar 400 destinasi di Jakarta, Yogyakarta, Semarang, Bandung, dan Surabaya.
- Cuaca historis: 1 Januari–31 Desember 2024 untuk lima kota tersebut.
- Data pendukung wilayah: tabel kota dari Wikipedia.

## Struktur Repository
- `UTSDAM_perbaikan_final.ipynb`: satu notebook utama untuk seluruh tahapan soal.
- `data/raw/`: sumber mentah CSV, JSON, HTML, dan bukti robots.txt.
- `data/processed/`: hasil olahan, dataset gabungan, metadata, dan checklist etika.
- `docs/`: provenance, bukti robots.txt, dan metadata scraping.

## Tahapan Pengerjaan
1. Akuisisi dataset destinasi wisata dari Kaggle menggunakan KaggleHub.
2. Identifikasi jenis, format, tipe kolom, cakupan, ukuran file, dan estimasi storage tahunan.
3. Akuisisi cuaca harian Open-Meteo untuk lima kota selama tahun 2024.
4. Pemeriksaan robots.txt dan ekstraksi tabel kota dari Wikipedia.
5. Pembersihan data dan penggabungan berdasarkan kolom `City`.
6. Validasi jumlah baris, keunikan `Place_Id`, dan kelengkapan hasil merge.
7. Pemeriksaan etika dan pencatatan provenance setiap sumber.

## Catatan Lisensi dan Etika
- Data Card Kaggle menampilkan `Data files © Original Authors`; pernyataan pada bagian Acknowledgements tidak dengan sendirinya membuktikan izin lisensi formal untuk penggunaan ulang.
- Status lisensi dan asal asli dataset Kaggle ditandai perlu verifikasi sampai tersedia bukti yang memadai.
- Data API Open-Meteo dilisensikan CC BY 4.0 dan memerlukan atribusi. Penggunaan layanan API publik gratis dibatasi untuk penggunaan nonkomersial; periksa ketentuan resmi sebelum penggunaan lain.
- User-Agent menggunakan email kontak yang diisi pada konfigurasi notebook. Pastikan alamat dan kebijakan penggunaannya sesuai arahan dosen.
- Tanggal unduh manual Kaggle tidak diisi tanpa bukti. Waktu unduh programatis melalui KaggleHub dicatat secara terpisah dari waktu pencatatan metadata.

## Cara Menjalankan
1. Buka notebook `UTSDAM_perbaikan_final.ipynb` di Google Colab.
2. Jalankan semua cell dari atas ke bawah tanpa melewati cell.
3. Pastikan dataset KaggleHub berhasil diunduh dan semua request sumber data berhasil.
4. Periksa keluaran setiap cell dan file yang terbentuk pada folder `data/` dan `docs/`.

## Hasil Utama
Hasil penggabungan disimpan pada `data/processed/merged_dataset.csv`, dengan informasi struktur dan validasi di `data/processed/merged_dataset.metadata.json`.
