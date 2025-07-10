# Deteksi Berita Bohong Menggunakan Machine Learning

## 1. Identitas Lengkap

**Nama**       : [Nama Lengkap Anda]  
**NIM/NPM**    : [Nomor Induk Mahasiswa/Peserta]  
**Instansi**   : [Nama Universitas/Instansi]  
**Email**      : [Alamat Email]

---

## 2. Ringkasan, Permasalahan, Tujuan, dan Alur Penyelesaian

### Ringkasan
Dalam era digital, penyebaran informasi melalui media online sangat cepat, termasuk berita bohong (fake news). Hal ini dapat menimbulkan dampak negatif dalam berbagai sektor seperti politik, ekonomi, dan sosial. Oleh karena itu, penting untuk mengembangkan sistem yang dapat mendeteksi berita palsu secara otomatis.

### Permasalahan
Bagaimana cara mengidentifikasi berita bohong secara akurat menggunakan metode machine learning?

### Tujuan
Menentukan model machine learning terbaik di antara Complement Naive Bayes, Logistic Regression, dan Random Forest untuk mendeteksi berita bohong berdasarkan performa metrik seperti akurasi, presisi, recall, dan f1-score.

### Alur Penyelesaian

graph TD;
    A[Data Berita (Dataset)] --> B[Preprocessing & EDA];
    B --> C[Ekstraksi Fitur (TF-IDF)];
    C --> D[Modeling: ComplementNB, Logistic Regression, Random Forest];
    D --> E[Evaluasi Model];
    E --> F[Analisis Performa];
    F --> G[Kesimpulan Model Terbaik];
    
3. Penjelasan Dataset, EDA, dan Proses Features Dataset
Dataset
Dataset yang digunakan berisi kumpulan berita yang sudah dilabeli sebagai real atau fake. Dataset mencakup informasi seperti judul berita, isi konten, sumber, dan label.

Exploratory Data Analysis (EDA)
Jumlah total data: XXXX data

Distribusi label: Real: XX%, Fake: XX%

Wordcloud untuk kata-kata yang sering muncul di berita palsu vs berita nyata

Analisis panjang teks dan korelasinya dengan label

Proses Ekstraksi Fitur
Stopword removal

Tokenisasi

Lowercasing

Ekstraksi fitur menggunakan TF-IDF Vectorizer

4. Proses Learning / Modeling
Model yang digunakan:

Complement Naive Bayes (CNB): Cocok untuk teks dengan distribusi tidak seimbang

Logistic Regression (LR): Model linear yang sering digunakan dalam klasifikasi biner

Random Forest (RF): Model ansambel berbasis pohon keputusan

Data dibagi menggunakan skema pelatihan 80:20 (train:test split) dan fitur teks diekstraksi menggunakan TF-IDF.

5. Performa Model
Model	Accuracy	Precision	Recall	F1-score
ComplementNB	0.8017	0.8603	0.9049	0.8820
Logistic Regression	0.8312	0.8339	0.9914	0.9059
Random Forest	0.8465	0.8552	0.9784	0.9126

6. Diskusi Hasil dan Kesimpulan
Diskusi
ComplementNB memiliki nilai recall tinggi, namun sedikit kalah dari Logistic Regression dan Random Forest dari segi akurasi dan F1-score.

Logistic Regression menunjukkan recall hampir sempurna (0.9914), menandakan sangat baik dalam mengidentifikasi berita palsu, namun presisinya sedikit lebih rendah dibanding Random Forest.

Random Forest memberikan performa terbaik secara keseluruhan, dengan akurasi dan F1-score tertinggi, menunjukkan keseimbangan terbaik antara mengidentifikasi dan menghindari false positives.

Kesimpulan
Berdasarkan hasil evaluasi, model Random Forest merupakan model paling optimal untuk digunakan dalam sistem deteksi berita bohong karena memberikan kombinasi terbaik antara akurasi, presisi, recall, dan F1-score.
