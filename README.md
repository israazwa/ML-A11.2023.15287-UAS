# 📰 Model Deteksi Terbaik untuk Filtrasi Berita Bohong (Fake News)

**Nama Lengkap**: ISRA SHAHZADA AZWA SAQIBA
**NIM / ID**: A11.2023.15287  

---

## 1. Ringkasan dan Permasalahan Proyek

Dalam era digital saat ini, penyebaran informasi secara cepat mempermudah munculnya berita bohong (fake news) yang dapat menimbulkan disinformasi publik. Penyebaran informasi palsu, terutama melalui media sosial, menjadi tantangan besar bagi masyarakat, pemerintah, dan media.

Proyek ini bertujuan untuk membangun sistem klasifikasi yang dapat membedakan antara berita asli dan berita palsu dengan memanfaatkan algoritma machine learning. Model yang dibangun diharapkan mampu secara otomatis memfilter berita bohong sehingga membantu menjaga kualitas informasi yang beredar.

### 🎯 Tujuan

- Mengembangkan model klasifikasi berita bohong berbasis machine learning
- Mengevaluasi dan membandingkan performa beberapa model: Complement Naive Bayes, Logistic Regression, dan Random Forest
- Menentukan model terbaik berdasarkan metrik evaluasi

---

## 2. Alur Penyelesaian

Alur proses penyelesaian proyek ini:

1. Pengumpulan Dataset Berita
2. EDA (Exploratory Data Analysis)
3. Preprocessing & Feature Engineering
4. Modeling: ComplementNB, Logistic Regression, Random Forest
5. Evaluasi: Accuracy, Precision, Recall, F1-score
6. Analisis Hasil dan Penentuan Model Terbaik

---

## 3. Dataset, EDA, dan Proses Features

### 📁 Dataset

- **Sumber**: [Kaggle / Open Source Fake News Dataset]
- **Jumlah Data**: ±20.000 artikel berita
- **Fitur Penting**:
  - `title`: Judul berita
  - `text`: Isi konten berita
  - `label`: 0 = berita asli, 1 = berita palsu

### 📊 EDA (Exploratory Data Analysis)

Beberapa langkah EDA yang dilakukan:
- Analisis distribusi label berita
- Analisis panjang teks
- Word frequency dan visualisasi wordcloud
- Korelasi antara panjang berita dengan label

### ⚙️ Preprocessing & Feature Engineering

Langkah-langkah:
- Text cleaning: lowercase, hapus tanda baca, hapus stopwords
- Stemming / Lemmatization
- Tokenization & Vectorization (TF-IDF)
- Pembagian data: 80% training, 20% testing

---

## 4. Proses Learning / Modeling

Tiga algoritma yang digunakan dalam modeling:

### 🔹 Complement Naive Bayes
- Cocok untuk data teks dengan distribusi tidak seimbang
- Sederhana dan cepat

### 🔹 Logistic Regression
- Model linier untuk klasifikasi biner
- Memberikan interpretasi probabilitas

### 🔹 Random Forest
- Model ensemble berbasis decision tree
- Performa tinggi dan tahan overfitting

Proses training dan evaluasi dilakukan menggunakan pipeline dan cross-validation untuk hasil yang lebih stabil.

---

## 5. Performa Model

Hasil evaluasi ketiga model berdasarkan metrik klasifikasi:

| Model                   | Accuracy | Precision | Recall  | F1-score |
|-------------------------|----------|-----------|---------|----------|
| Complement Naive Bayes  | 0.8017   | 0.8603    | 0.9049  | 0.8820   |
| Logistic Regression     | 0.8312   | 0.8339    | 0.9914  | 0.9059   |
| Random Forest           | 0.8465   | 0.8552    | 0.9784  | 0.9126   |

**Catatan:**
- ComplementNB unggul dalam recall
- Logistic Regression sangat tinggi recall namun precision menurun
- Random Forest paling seimbang, menghasilkan **F1-score tertinggi**

---

## 6. Diskusi Hasil dan Kesimpulan

### 💬 Diskusi

- Semua model memiliki performa F1-score > 0.88
- ComplementNB cocok jika prioritasnya adalah mendeteksi sebanyak mungkin berita bohong (recall tinggi)
- Logistic Regression memiliki performa sangat baik namun tidak setinggi Random Forest
- Random Forest adalah model terbaik dari hasil evaluasi semua metrik

### ✅ Kesimpulan

- Model **Random Forest** dipilih sebagai model deteksi berita bohong terbaik pada dataset ini
- Model ini dapat digunakan dalam sistem penyaringan berita atau integrasi ke aplikasi pemeriksa fakta
- Pengembangan lanjutan:
  - Coba model deep learning seperti LSTM atau BERT
  - Lakukan analisis clickbait
  - Tambahkan fitur meta-data (waktu terbit, sumber, dll)

---

## 📚 Referensi

1. [Fake News Dataset - Kaggle](https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset)
2. Dokumentasi Scikit-learn: https://scikit-learn.org
3. Artikel: "The rise of fake news and how to detect it" – Journal of Information Ethics

---

## 📌 Catatan Tambahan

> Proyek ini merupakan bagian dari pembelajaran klasifikasi teks menggunakan machine learning.  
> Semua kode, hasil, dan eksperimen tersedia dalam repositori ini.
