# Performance-Analysis-of-Machine-Learning-Algorithms-in-Phishing-URL-Detection-on-PhiUSIIL-Dataset

Repositori ini berisi hasil studi komparatif mendalam mengenai kinerja berbagai algoritma machine learning dalam mendeteksi URL phishing, menggunakan **dataset PhiUSIIL (Phishing URL Structured and Interpretable Information Learning)**.

##  Tujuan Proyek

Proyek ini bertujuan untuk:
- Membangun model klasifikasi URL phishing menggunakan 5 algoritma supervised learning:
  - XGBoost  
  - Random Forest  
  - Decision Tree  
  - K-Nearest Neighbors (KNN)  
  - Naive Bayes  
- Menganalisis dampak dari berbagai strategi preprocessing.
- Menentukan algoritma terbaik berdasarkan akurasi dan stabilitas performa.

---

##  Dataset

**PhiUSIIL Dataset** memiliki karakteristik berikut:
- Total: 99.935 data URL
- Jumlah fitur: 56 fitur termasuk struktur domain, HTML, dan karakteristik teks URL
- Label: 
  - `1` → URL Aman (Legitimate)  
  - `0` → URL Phishing
- Tipe data campuran: numerik dan kategorikal
- Tantangan:
  - Data imbalance  
  - Nilai hilang (missing values)  
  - Skala fitur yang tidak seragam

---

##  Metodologi

Penelitian dilakukan melalui empat skenario eksperimen:

1. **Baseline**: Preprocessing dasar (encoding, imputasi, seleksi fitur).
2. **SMOTE**: Penanganan imbalance menggunakan Synthetic Minority Oversampling Technique.
3. **SMOTE + Scaling**: Penambahan normalisasi fitur menggunakan StandardScaler.
4. **SMOTE + Scaling + Hyperparameter Tuning**: Tuning parameter model menggunakan Grid Search.

Langkah utama:
- Exploratory Data Analysis (EDA)
- Preprocessing data
- Pelatihan dan evaluasi model menggunakan 4 skenario
- Evaluasi dengan metrik **akurasi** dan **confusion matrix**

---

##  Hasil dan Temuan

- **XGBoost** memberikan hasil terbaik dengan akurasi hingga **99,94%**, dan jumlah kesalahan klasifikasi yang sangat rendah.
- **Random Forest** juga menunjukkan performa tinggi dan stabil.
- **Decision Tree** dan **KNN** memiliki performa cukup baik, namun sensitif terhadap distribusi data.
- **Naive Bayes** memiliki performa terendah, terutama setelah dilakukan scaling dan SMOTE, karena asumsinya sulit dipenuhi.

---

##  Algoritma Terbaik

 **XGBoost** dinyatakan sebagai algoritma terbaik dalam deteksi phishing URL pada dataset PhiUSIIL berdasarkan:
- Akurasi tinggi
- Error klasifikasi minimal
- Kemampuan menangani data kompleks dan tidak seimbang

---

## 💻 Teknologi yang Digunakan

- Python 3.10+
- Google Colaboratory
- Scikit-learn
- XGBoost
- Pandas, NumPy, Matplotlib, Seaborn
- SMOTE (Imbalanced-learn)

---


