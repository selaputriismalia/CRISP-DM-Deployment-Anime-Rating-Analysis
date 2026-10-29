# Analisis Rating dan Pengelompokan Anime — CRISP-DM

Repository ini mendokumentasikan proyek **data mining anime** yang dikerjakan dengan pendekatan CRISP-DM. Fokusnya adalah memahami data, melakukan persiapan data, mengeksplorasi rating dan genre, serta mencoba pengelompokan (clustering).

> **Catatan ruang lingkup:** repository ini berfokus pada proses analisis dan pemodelan data. Aplikasi web interaktif yang ditujukan untuk pengguna akhir akan didokumentasikan secara terpisah di repository **Anime Rating Dashboard** setelah kode sumber dashboard lama berhasil ditemukan dan dipulihkan.

## Tujuan Proyek

- Memahami struktur dan karakteristik dataset anime.
- Menyiapkan data untuk proses analisis.
- Mengeksplorasi distribusi rating, genre, dan tipe media.
- Menerapkan PCA untuk reduksi dimensi dan Agglomerative Clustering untuk eksplorasi kelompok data.
- Mendokumentasikan tahapan analisis menggunakan CRISP-DM.

## Alur CRISP-DM

1. **Business Understanding** — menentukan fokus analisis karakteristik dan rating anime.
2. **Data Understanding** — memeriksa struktur, atribut, distribusi, dan kualitas data.
3. **Data Preparation** — membersihkan serta menyiapkan data untuk pemodelan.
4. **Modeling** — menerapkan teknik reduksi dimensi dan clustering.
5. **Evaluation** — meninjau pola hasil pengelompokan dan mengevaluasi hasil analisis.
6. **Deployment** — mendokumentasikan penerapan hasil analisis. Dashboard pengguna akhir bukan fokus utama repository ini.

## Isi Repository

| File | Keterangan |
|---|---|
| `Sela_Datmin.ipynb` | Notebook eksplorasi, persiapan data, dan pemodelan |
| `Data_Cleaned.csv` | Dataset hasil preprocessing yang digunakan oleh dashboard analisis saat ini |
| `main.py` | Aplikasi Streamlit untuk visualisasi analisis dan clustering |
| `requirements.txt` | Dependensi Python |
| `README.md` | Dokumentasi proyek |

## Teknologi

- Python
- Pandas dan NumPy
- Matplotlib dan Seaborn
- Scikit-learn
- Jupyter Notebook
- Streamlit

## Menjalankan Aplikasi Analisis

Pastikan Python telah terpasang, kemudian jalankan:

```bash
git clone https://github.com/selaputriismalia/CRISP-DM-Deployment-Anime-Rating-Analysis.git
cd CRISP-DM-Deployment-Anime-Rating-Analysis
python -m venv .venv
```

Aktifkan virtual environment.

**Windows**
```bash
.venv\\Scripts\\activate
```

**macOS/Linux**
```bash
source .venv/bin/activate
```

Instal dependensi dan jalankan Streamlit:

```bash
pip install -r requirements.txt
streamlit run main.py
```

## Batasan Saat Ini

- `Data_Cleaned.csv` merupakan data hasil preprocessing dan tidak memuat semua informasi deskriptif dari dataset mentah, seperti nama anime.
- Dashboard analisis saat ini menampilkan eksplorasi data dan clustering; fitur rekomendasi anime interaktif belum dikonfirmasi tersedia pada aplikasi ini.
- Hasil clustering bergantung pada fitur yang digunakan, preprocessing, dan parameter model.

## Proyek Terkait

**Anime Rating Dashboard** akan menjadi proyek terpisah yang berfokus pada pengalaman pengguna, eksplorasi rating, dan fitur dashboard yang relevan. Repository dashboard akan dibuat setelah kode sumber aplikasi lama ditemukan agar dokumentasinya sesuai dengan implementasi sebenarnya.

---

**Topik:** Data Mining · Data Analysis · Data Visualization · Machine Learning · CRISP-DM
