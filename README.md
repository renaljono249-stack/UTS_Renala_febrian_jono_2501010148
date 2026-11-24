# UTS DATA ACQUISITION & MANAGEMENT
## Pariwisata Yogyakarta

### 1. Identitas Mahasiswa
- **Nama:** Renala Febrian Jono
- **NIM:** 2501010148
- **Program Studi:** Informatika
- **Perguruan Tinggi:** Institut Bisnis dan Teknologi Indonesia (INSTIKI)
- **Mata Kuliah:** Data Acquisition & Management
- **Kelas:** F
- **Tahun Akademik:** 2026/2027
- **Topik Proyek:** Pariwisata Yogyakarta

### 2. Deskripsi Proyek
Proyek ini bertujuan untuk melakukan pengumpulan, pemeriksaan, pembersihan, pengolahan, dan penggabungan data yang berkaitan dengan pariwisata di Yogyakarta.

Data diperoleh melalui tiga metode, yaitu:
1. Open Dataset dari Kaggle.
2. API Open-Meteo.
3. Web Scraping dari website Visiting Jogja.

### 3. Sumber Data

**A. Open Dataset – Kaggle**

Nama dataset: Dataset Pariwisata Yogyakarta.

URL: https://www.kaggle.com/datasets/saufan/dataset-pariwisata-yogyakarta

File:
- tour.csv
- tour_rating.csv
- user.csv

**B. API – Open-Meteo**

URL: https://api.open-meteo.com/v1/forecast

Lokasi: Yogyakarta.

Koordinat:
- Latitude: -7.8014
- Longitude: 110.3647

Variabel:
- Temperature
- Rain
- Wind Speed
- Weather Code

**C. Web Scraping – Visiting Jogja**

Website: https://visitingjogja.jogjaprov.go.id/

Halaman scraping: https://visitingjogja.jogjaprov.go.id/wisata-jogja/

Jumlah data hasil scraping: 107 data unik.

### 4. Proses Pengolahan Data

**A. Open Dataset**
- Membaca file CSV.
- Memeriksa jumlah baris dan kolom.
- Memeriksa tipe data dan nilai kosong.
- Memeriksa data duplikat.
- Melakukan pembersihan data.
- Menyimpan data hasil pembersihan.

**B. API**
- Mengakses API Open-Meteo.
- Memeriksa status HTTP.
- Menggunakan timeout dan mekanisme retry.
- Mengambil data cuaca Yogyakarta.
- Mengubah JSON menjadi tabel CSV.
- Menyimpan data mentah dan provenance.

**C. Web Scraping**
- Memeriksa robots.txt.
- Mengakses halaman Visiting Jogja.
- Menggunakan Requests dan BeautifulSoup.
- Mengambil judul dan URL artikel wisata.
- Mengumpulkan data dari beberapa halaman.
- Menghapus data duplikat.
- Menghasilkan 107 data unik.

**D. Penggabungan Data**
- Menggabungkan dataset Kaggle dan hasil scraping.
- Menggunakan metode Inner Join.
- Menggunakan nama tempat wisata sebagai kunci penghubung.
- Memeriksa duplikasi dan nilai kosong.
- Menyimpan hasil merge dan metadata.

### 5. Hasil Penggabungan Data
File hasil: `hasil_merge_pariwisata_yogyakarta.csv`

Hasil penggabungan:
- Jumlah baris: 1
- Jumlah kolom: 14
- Tempat wisata yang cocok: Gembira Loka Zoo
- Duplikasi baris: 0
- Duplikasi Place_Id: 0

Penggabungan hanya menghasilkan satu baris karena hanya satu pasangan nama tempat wisata yang cocok secara persis.

### 6. Etika dan Provenance Data
Proyek ini memperhatikan:
- Pencantuman sumber data.
- Pemeriksaan lisensi dan ketentuan penggunaan.
- Perlindungan data pribadi.
- Penyimpanan data mentah.
- Dokumentasi proses pembersihan.
- Pencatatan URL dan tanggal akses.
- Pemeriksaan checksum MD5.

Status lisensi dataset Kaggle masih perlu diverifikasi sebelum penggunaan ulang atau distribusi dataset.

### 7. Tools yang Digunakan
- Google Colab
- Python
- Pandas
- Requests
- BeautifulSoup
- Open-Meteo API
- GitHub

### 8. Kesimpulan
Proyek ini menerapkan tiga metode akuisisi data, yaitu open dataset, API, dan web scraping untuk memperoleh data pariwisata Yogyakarta.

Data kemudian diperiksa, dibersihkan, didokumentasikan, dan sebagian digabungkan untuk menghasilkan dataset yang dapat digunakan dalam analisis lebih lanjut.

---
