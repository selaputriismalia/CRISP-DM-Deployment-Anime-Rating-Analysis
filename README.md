# Analisis Rating dan Pengelompokan Anime

Aplikasi dashboard interaktif berbasis Python dan Streamlit untuk mengeksplorasi karakteristik anime berdasarkan rating, genre, dan tipe media penayangan. Proyek ini menggunakan pendekatan CRISP-DM dan menerapkan Agglomerative Clustering untuk mengeksplorasi kelompok data anime.


## Daftar Isi
- [Latar Belakang](#latar-belakang)
- [Tujuan](#tujuan)
- [Fitur Dashboard](#fitur-dashboard)
- [Teknologi](#teknologi)
- [Dataset](#dataset)
- [Metodologi CRISP-DM](#metodologi-crisp-dm)
- [Struktur Repository](#struktur-repository)
- [Instalasi dan Menjalankan Aplikasi](#instalasi-dan-menjalankan-aplikasi)
- [Catatan Analisis](#catatan-analisis)

## Latar Belakang
Dataset anime memuat informasi yang dapat dieksplorasi untuk memahami persebaran rating dan karakteristik konten. Dashboard ini mengemas proses eksplorasi dan visualisasi agar hasilnya lebih mudah dipahami tanpa harus membaca seluruh data mentah secara manual.

## Tujuan
- Mengeksplorasi distribusi rating anime.
- Menampilkan genre yang paling sering muncul pada dataset.
- Membandingkan jumlah data berdasarkan tipe media.
- Menerapkan clustering untuk melihat pola kelompok data.
- Menyajikan hasil eksplorasi melalui dashboard interaktif.

## Fitur Dashboard
1. **Pratinjau dataset** — menampilkan sampel data yang dianalisis.
2. **Distribusi rating** — memvisualisasikan persebaran nilai rating.
3. **Top 10 genre** — menampilkan genre dengan jumlah kemunculan tertinggi.
4. **Distribusi tipe media** — membandingkan kategori seperti Movie, Music, ONA, OVA, Special, dan TV.
5. **Agglomerative Clustering** — menyediakan kontrol jumlah cluster pada rentang 2–10.
6. **Rating tertinggi dan terendah** — menampilkan daftar anime berdasarkan rating, dengan pilihan jumlah data yang ditampilkan.

## Teknologi
| Teknologi | Kegunaan |
|---|---|
| Python | Bahasa pemrograman utama |
| Streamlit | Dashboard interaktif |
| Pandas | Membaca dan mengolah data |
| NumPy | Operasi numerik |
| Matplotlib | Visualisasi |
| Seaborn | Visualisasi statistik |
| Scikit-learn | Standardisasi, PCA, dan clustering |

## Dataset
Aplikasi menggunakan file `Data_Cleaned.csv`, yaitu dataset yang telah dibersihkan sebelum digunakan pada dashboard.

Kolom dan atribut yang relevan mencakup identitas anime, indikator genre, tipe media, serta rating. Hasil analisis bergantung pada isi dan kualitas dataset tersebut.

## Metodologi CRISP-DM
### 1. Business Understanding — Pemahaman Bisnis
Menentukan fokus analisis: memahami pola rating dan karakteristik anime berdasarkan genre serta tipe media.

### 2. Data Understanding — Pemahaman Data
Memeriksa struktur, sampel, kolom, dan distribusi data untuk memahami atribut yang tersedia.

### 3. Data Preparation — Persiapan Data
Menggunakan dataset hasil pembersihan `Data_Cleaned.csv`. Fitur numerik yang digunakan pada proses clustering distandardisasi dengan `StandardScaler`.

### 4. Modeling — Pemodelan
Menggunakan Principal Component Analysis (PCA) untuk memproyeksikan data ke dua dimensi dan Agglomerative Clustering untuk membentuk kelompok data.

### 5. Evaluation — Evaluasi
Mengeksplorasi hasil pengelompokan melalui visualisasi dan membandingkan pola yang terbentuk. Evaluasi lanjutan menggunakan metrik clustering masih dapat ditambahkan untuk mengukur kualitas kelompok secara lebih terstruktur.

### 6. Deployment — Penerapan
Menyajikan hasil analisis melalui aplikasi Streamlit yang dapat dijalankan secara lokal atau dipublikasikan pada layanan hosting yang mendukung Streamlit.

## Struktur Repository
```text
2209116085_CRISP-DM_DEPLOYMENT/
├── Data_Cleaned.csv
├── main.py
├── requirements.txt
└── README.md
```

| File | Fungsi |
|---|---|
| `Data_Cleaned.csv` | Dataset untuk analisis |
| `main.py` | Kode utama dashboard dan proses analisis |
| `requirements.txt` | Daftar dependensi Python |
| `README.md` | Dokumentasi proyek |

## Instalasi dan Menjalankan Aplikasi
**Prasyarat:** Python terpasang pada komputer.

### 1. Clone repository
```bash
git clone https://github.com/selaputriismalia/2209116085_CRISP-DM_DEPLOYMENT.git
cd 2209116085_CRISP-DM_DEPLOYMENT
```

### 2. Buat virtual environment (disarankan)
Windows:
```bash
python -m venv .venv
.venv\\Scripts\\activate
```

macOS/Linux:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Instal dependensi
```bash
pip install -r requirements.txt
```

### 4. Jalankan dashboard
```bash
streamlit run main.py
```

Buka alamat lokal yang ditampilkan di terminal untuk mengakses dashboard.

## Catatan Analisis
Hasil analisis dipengaruhi oleh kualitas dan cakupan dataset. PCA memproyeksikan data ke dua dimensi untuk membantu visualisasi, sedangkan jumlah cluster yang dipilih memengaruhi hasil pengelompokan. Aplikasi ini berfokus pada analisis rating, visualisasi data, dan clustering.

---
**Topik:** Analisis Data · Visualisasi Data · Machine Learning · CRISP-DM
