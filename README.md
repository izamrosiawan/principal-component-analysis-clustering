# Implementasi PCA dalam Pra-pemrosesan Data untuk Analisis Clustering

Proyek ini bertujuan untuk mengimplementasikan **Principal Component Analysis (PCA)** sebagai metode reduksi dimensi dalam tahap pra-pemrosesan data sebelum melakukan analisis pengelompokan menggunakan algoritma **K-Means Clustering** pada dataset estimasi tingkat obesitas.

---

## 📂 Struktur Proyek

Berikut adalah struktur direktori dari repositori ini:

*   📂 **`main/`**
    *   📄 `ObesityDataSet_raw_and_data_sinthetic.csv` - Dataset mentah tingkat obesitas berdasarkan kebiasaan makan dan kondisi fisik.
    *   📄 `obesity_data_cleaned.csv` - Dataset setelah pembersihan data (handling outliers dan pembersihan baris kosong).
    *   📄 `obesity_data_preprocessed.csv` - Dataset yang telah dinormalisasi menggunakan StandardScaler.
    *   📄 `pca_features.csv` & `pca_clustered.csv` - Hasil ekstraksi fitur dengan PCA serta data akhir hasil clustering.
    *   📓 `kode-implementasi-principal-component-analysis-pca-dalam-pra-pemrosesan-data-untuk-analisis-clustering.ipynb` - Jupyter Notebook berisi seluruh alur kode Python dari analisis data eksploratif (EDA), reduksi dimensi PCA, hingga evaluasi cluster K-Means.
*   📂 **`laporan/`**
    *   📕 `laporan-implementasi-principal-component-analysis-pca-dalam-pra-pemrosesan-data-untuk-analisis-clustering.pdf` - Laporan tertulis lengkap yang menjabarkan hasil analisis dan metodologi.

---

## 📈 Metodologi & Alur Kerja

1.  **Exploratory Data Analysis (EDA)**: Menilai distribusi data, memeriksa *outliers*, korelasi antar variabel, serta mengidentifikasi missing values.
2.  **Pra-pemrosesan Data**:
    *   Melakukan *Label Encoding* pada variabel kategori.
    *   Melakukan standardisasi data menggunakan *StandardScaler* agar seluruh fitur memiliki skala yang sama sebelum PCA.
3.  **Principal Component Analysis (PCA)**:
    *   Menguji *Explained Variance Ratio* kumulatif untuk menentukan jumlah komponen utama yang optimal.
    *   Memproyeksikan fitur berdimensi tinggi ke dalam komponen utama (PC) baru.
    *   Visualisasi data dalam ruang 2D dan 3D komponen utama.
4.  **K-Means Clustering**:
    *   Menggunakan *Elbow Method* dan *Silhouette Score* untuk menentukan jumlah klaster $K$ terbaik.
    *   Mengelompokkan data berdasarkan komponen utama hasil PCA.
5.  **Evaluasi & Interpretasi**: Menganalisis karakteristik profil kesehatan dari masing-masing klaster yang terbentuk.

---

## 🛠️ Cara Menjalankan

### Persyaratan Sistem
Instal pustaka Python yang diperlukan sebelum menjalankan kode:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### Langkah Penggunaan
1. Navigasikan ke dalam folder `main/`.
2. Buka dan jalankan Jupyter Notebook `kode-implementasi-principal-component-analysis-pca-dalam-pra-pemrosesan-data-untuk-analisis-clustering.ipynb` secara berurutan.
3. Anda dapat melihat visualisasi scree plot, sebaran data hasil PCA, penentuan nilai $K$ optimal, dan pengelompokan klaster akhir.
