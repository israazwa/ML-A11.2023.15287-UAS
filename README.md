# Deteksi Berita Bohong dengan Machine Learning

Proyek ini bertujuan untuk membangun sistem klasifikasi otomatis yang dapat membedakan antara berita benar dan berita bohong menggunakan teknik machine learning. Dengan memanfaatkan dataset teks dan pendekatan NLP (Natural Language Processing), model-model dikembangkan untuk memberikan prediksi yang akurat terhadap konten berita online.

## 📊 Model dan Evaluasi

Tiga model machine learning digunakan dan dibandingkan berdasarkan metrik evaluasi:

### 1. Complement Naive Bayes (ComplementNB)
- **Accuracy** : 0.8017  
- **Precision**: 0.8603  
- **Recall**   : 0.9049  
- **F1-score** : 0.8820  

### 2. Logistic Regression
- **Accuracy** : 0.8312  
- **Precision**: 0.8339  
- **Recall**   : 0.9914  
- **F1-score** : 0.9059  

### 3. Random Forest
- **Accuracy** : 0.8465  
- **Precision**: 0.8552  
- **Recall**   : 0.9784  
- **F1-score** : 0.9126  

🔍 Dari hasil tersebut, Random Forest menghasilkan performa terbaik secara konsisten dengan F1-score tertinggi, yang menunjukkan keseimbangan optimal antara precision dan recall.

## ⚙️ Alur Sistem
1. Preprocessing teks berita (tokenisasi, stopword removal, stemming)
2. Transformasi ke fitur numerik menggunakan TF-IDF
3. Pelatihan model ComplementNB, Logistic Regression, dan Random Forest
4. Evaluasi performa menggunakan metrik klasik (Accuracy, Precision, Recall, F1-score)
5. Deployment model terbaik untuk prediksi realtime

## 🏁 Penutup

Deteksi berita bohong secara otomatis adalah langkah penting dalam menjaga kualitas informasi publik dan mengurangi dampak hoaks digital. Proyek ini menunjukkan bagaimana pendekatan machine learning dapat memberikan solusi nyata dalam memverifikasi kebenaran konten berita. Pengembangan ke depan dapat melibatkan data real-time, integrasi API berita, atau sistem pelaporan komunitas.
