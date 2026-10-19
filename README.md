# Anime Rating Analysis & Recommender System

Aplikasi analisis data anime berbasis **Python** dan **Streamlit** untuk mengeksplorasi karakteristik anime berdasarkan rating, genre, dan tipe media penayangan. Proyek ini juga menerapkan **Agglomerative Clustering** untuk mengelompokkan data anime dan menampilkan hasilnya secara visual.

> Proyek ini disusun sebagai implementasi analisis data dengan pendekatan **CRISP-DM (Cross-Industry Standard Process for Data Mining)**, dari pemahaman data hingga penyajian hasil melalui dashboard.

## Daftar Isi

- [Tentang Proyek](#tentang-proyek)
- [Tujuan](#tujuan)
- [Fitur Utama](#fitur-utama)
- [Teknologi yang Digunakan](#teknologi-yang-digunakan)
- [Dataset](#dataset)
- [Metodologi CRISP-DM](#metodologi-crisp-dm)
- [Struktur Repository](#struktur-repository)
- [Instalasi dan Menjalankan Aplikasi](#instalasi-dan-menjalankan-aplikasi)
- [Catatan Analisis](#catatan-analisis)
- [Pengembangan Selanjutnya](#pengembangan-selanjutnya)

## Tentang Proyek

Anime Rating Analysis & Recommender System merupakan proyek analisis data yang berfokus pada eksplorasi rating dan karakteristik anime. Data yang telah dibersihkan digunakan untuk menyajikan ringkasan dan visualisasi, serta sebagai masukan untuk proses pengelompokan menggunakan teknik machine learning.

Dashboard dibuat dengan Streamlit agar hasil analisis dapat dijelajahi secara interaktif tanpa perlu menjalankan setiap proses analisis secara manual.

## Tujuan

- Memahami distribusi rating anime berdasarkan dataset yang tersedia.
- Mengidentifikasi genre anime yang paling banyak muncul dalam data.
- Membandingkan jumlah anime berdasarkan tipe media penayangan.
- Menerapkan Agglomerative Clustering untuk mengeksplorasi kelompok data anime.
- Menyajikan hasil analisis dalam dashboard yang mudah digunakan dan dipahami.

## Fitur Utama

### 1. Pratinjau Dataset
Menampilkan beberapa baris awal dataset untuk membantu pengguna memahami struktur data yang dianalisis.

### 2. Distribusi Rating Anime
Menyajikan histogram distribusi rating sehingga pola persebaran nilai rating dapat diamati.

### 3. Sepuluh Genre Anime Terpopuler
Menghitung dan menampilkan sepuluh genre dengan jumlah kemunculan tertinggi berdasarkan kolom genre pada dataset.

### 4. Distribusi Tipe Media
Membandingkan tipe media anime, seperti Movie, Music, ONA, OVA, Special, dan TV.

### 5. Pengelompokan dengan Agglomerative Clustering
Melakukan standardisasi data menggunakan `StandardScaler`, mereduksi dimensi menjadi dua komponen menggunakan Principal Component Analysis (PCA), kemudian membentuk kelompok dengan Agglomerative Clustering. Jumlah cluster dapat diatur melalui sidebar aplikasi, dari 2 hingga 10 cluster.

### 6. Rating Tertinggi dan Terendah
Menampilkan daftar rating tertinggi dan terendah. Pengguna dapat memilih jumlah data yang ditampilkan, yaitu 5, 10, atau 15.

## Teknologi yang Digunakan

| Teknologi | Penggunaan |
|---|---|
| Python | Bahasa pemrograman utama |
| Streamlit | Membangun dashboard interaktif |
| Pandas | Membaca dan mengolah dataset |
| Matplotlib | Membuat visualisasi data |
| Seaborn | Visualisasi distribusi rating |
| Scikit-learn | Standardisasi, PCA, dan Agglomerative Clustering |
| NumPy | Mendukung operasi numerik |

## Dataset

Aplikasi menggunakan file `Data_Cleaned.csv`, yaitu dataset yang telah melalui proses pembersihan data.

Kolom-kolom utama yang digunakan meliputi:

- **anime_id**: identitas anime.
- **Kolom genre**: indikator genre, seperti Action, Adventure, Comedy, Drama, Fantasy, Romance, dan genre lainnya.
- **Kolom tipe media**: indikator media penayangan, seperti Movie, Music, ONA, OVA, Special, dan TV.
- **rating**: nilai rating anime.

Kolom genre dan tipe media disajikan dalam bentuk indikator pada dataset, sedangkan rating digunakan untuk analisis distribusi serta pemilihan rating tertinggi dan terendah.

## Metodologi CRISP-DM

Proyek ini dapat dijelaskan melalui enam tahapan CRISP-DM berikut.

### 1. Business Understanding — Pemahaman Bisnis
Menentukan tujuan analisis, yaitu memahami pola rating, karakteristik genre, dan tipe media anime agar informasi dalam dataset lebih mudah dipahami.

### 2. Data Understanding — Pemahaman Data
Memeriksa struktur dataset, melihat sampel data, memahami kolom yang tersedia, serta mengamati distribusi rating dan karakteristik anime.

### 3. Data Preparation — Persiapan Data
Menggunakan dataset hasil pembersihan `Data_Cleaned.csv`. Sebelum clustering, data yang digunakan dalam proses tersebut distandardisasi dengan `StandardScaler`.

### 4. Modeling — Pemodelan
Menerapkan PCA untuk mereduksi data menjadi dua dimensi, kemudian menggunakan Agglomerative Clustering untuk membentuk kelompok. Pengguna dapat menentukan jumlah cluster melalui kontrol pada dashboard.

### 5. Evaluation — Evaluasi
Mengamati visualisasi hasil clustering dan membandingkan karakteristik kelompok yang terbentuk. Visualisasi membantu eksplorasi pola, tetapi belum menjadi bukti bahwa cluster yang terbentuk merupakan model terbaik; evaluasi lanjutan dengan metrik clustering dapat dilakukan.

### 6. Deployment — Penerapan
Menyajikan hasil eksplorasi dan visualisasi melalui aplikasi Streamlit. Aplikasi dapat dijalankan secara lokal atau dipublikasikan melalui layanan hosting yang mendukung Streamlit.

## Struktur Repository

```text
2209116085_CRISP-DM_DEPLOYMENT/
├── Data_Cleaned.csv
├── main.py
├── requirements.txt
└── README.md
```

| File | Keterangan |
|---|---|
| `Data_Cleaned.csv` | Dataset yang digunakan aplikasi |
| `main.py` | Kode utama dashboard, visualisasi, dan clustering |
| `requirements.txt` | Daftar library Python yang dibutuhkan |
| `README.md` | Dokumentasi proyek |

## Instalasi dan Menjalankan Aplikasi

### Prasyarat
- Python telah terpasang di komputer.
- Git digunakan untuk mengunduh repository (opsional jika mengunduh ZIP).
- Koneksi internet diperlukan untuk instalasi library.

### 1. Clone repository

```bash
git clone https://github.com/selaputriismalia/2209116085_CRISP-DM_DEPLOYMENT.git
cd 2209116085_CRISP-DM_DEPLOYMENT
```

### 2. Buat virtual environment (opsional, tetapi disarankan)

Windows:

```bash
python -m venv .venv
.venv\Scripts\activate
```

macOS atau Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Instal dependensi

```bash
pip install -r requirements.txt
```

### 4. Jalankan aplikasi

Pastikan file `Data_Cleaned.csv` berada di direktori yang sama dengan `main.py`, lalu jalankan:

```bash
streamlit run main.py
```

Streamlit akan menampilkan alamat lokal di terminal. Buka alamat tersebut melalui browser untuk menggunakan dashboard.

## Catatan Analisis

- Hasil analisis bergantung pada isi dan kualitas dataset yang digunakan.
- PCA digunakan untuk memproyeksikan data ke dua dimensi sebelum proses clustering; visualisasi dua dimensi dapat menyederhanakan informasi dari data asli.
- Jumlah cluster yang dipilih pengguna memengaruhi hasil pengelompokan.
- Repository saat ini menyediakan analisis rating dan clustering. Fitur rekomendasi personal berdasarkan preferensi pengguna belum dijelaskan sebagai fitur terpisah dalam implementasi kode yang tersedia.

## Pengembangan Selanjutnya

Beberapa pengembangan yang dapat dipertimbangkan:

- Menambahkan metrik evaluasi clustering, misalnya Silhouette Score.
- Menampilkan identitas anime pada hasil cluster agar hasil lebih mudah diinterpretasikan.
- Menambahkan filter genre, rentang rating, dan tipe media.
- Mengembangkan rekomendasi anime berdasarkan genre atau preferensi pengguna.
- Mempublikasikan dashboard melalui layanan deployment yang sesuai dan mendokumentasikan tautan aplikasinya.

---

**Repository:** [2209116085_CRISP-DM_DEPLOYMENT](https://github.com/selaputriismalia/2209116085_CRISP-DM_DEPLOYMENT)

**Topik:** Data Analysis · Data Visualization · Machine Learning · CRISP-DM
