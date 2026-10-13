# mahadata-spark-supplychain
# Replikasi Spark MLlib: Supply Chain Demand Forecasting

Repositori ini dibuat untuk memenuhi **Tugas Eksplorasi Mandiri Mahadata / Big Data (IF25-40402)** di Institut Teknologi Sumatera (ITERA).

Eksperimen ini melakukan **replikasi parsial** dari jurnal ilmiah bereputasi Scopus Q1 mengenai prediksi permintaan rantai pasok berbasis pemrosesan data terdistribusi menggunakan Apache Spark (PySpark MLlib).

---

## 📄 Artikel Acuan
* **Judul Artikel:** *Predictive big data analytics for supply chain demand forecasting: Methods, applications, and research opportunities*
* **Penulis:** M. Seyedan & F. Mafakheri
* **Jurnal:** *Journal of Big Data* (Springer Nature, 2020)
* **DOI:** [10.1186/s40537-020-00329-2](https://doi.org/10.1186/s40537-020-00329-2)

---

## 🛠️ Ringkasan Metodologi Eksperimen
1. **Data Ingestion & Generation:** Pembuatan dataset transaksi *supply chain* sintetik yang mencakup variabel harga unit, indikator promosi, waktu transaksi, dan kuantitas permintaan barang.
2. **Preprocessing & Feature Engineering:**
   * Ekstraksi fitur temporal (`Hour`, `DayOfWeek`) dari *timestamp*.
   * Transformasi variabel kategorikal (`ProductID`) menggunakan `StringIndexer`.
   * Pembentukan vektor fitur dengan `VectorAssembler` dan standardisasi skala data menggunakan `StandardScaler`.
3. **Model Training & Evaluation:** Pelatihan model **Random Forest Regressor** dan **Linear Regression** serta evaluasi metrik *Root Mean Squared Error* (RMSE) dan *Mean Absolute Error* (MAE).

---

## 📁 Struktur Berkas Repository
* `EksperimenMahadataPySpark.ipynb` : Notebook utama eksperimen PySpark.
* `requirements.txt` : Daftar pustaka/dependensi Python yang dibutuhkan.
* `hasil_supply_chain.csv` : Hasil evaluasi metrik RMSE, MAE, dan waktu komputasi.
* `grafik_supply_chain.png` : Grafik visualisasi perbandingan RMSE antar model.
* `README.md` : Dokumentasi lengkap repositori.

---

## 🚀 Cara Menjalankan Notebook
1. Buka file `EksperimenMahadataPySpark.ipynb` pada repositori ini.
2. Klik tombol **Open in Colab** di bagian atas notebook.
3. Jalankan seluruh sel kode secara berurutan (`Runtime` > `Run all`).
