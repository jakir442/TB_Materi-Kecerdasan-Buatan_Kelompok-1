<div align="center">

# 🤖 AI Resume Analyzer

### Klasifikasi Kategori Pekerjaan Menggunakan NLP, TF-IDF, dan Machine Learning

![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-green?style=for-the-badge)
![NLP](https://img.shields.io/badge/NLP-TF--IDF-orange?style=for-the-badge)
![SVM](https://img.shields.io/badge/SVM-100%25-red?style=for-the-badge)
![Naive Bayes](https://img.shields.io/badge/Naive%20Bayes-100%25-yellow?style=for-the-badge)

## 🎥 Video Demo

**▶️ Tonton Demo AI Resume Analyzer di YouTube**
https://youtu.be/QFQ7avq9by4

---

### 📚 UAS Kecerdasan Buatan
### Program Studi Teknik Informatika

---

</div>

# 📌 Tentang Proyek

AI Resume Analyzer adalah sistem berbasis **Artificial Intelligence (AI)** yang mampu melakukan analisis dan klasifikasi resume secara otomatis berdasarkan isi dokumen yang diberikan.

Sistem memanfaatkan teknik **Natural Language Processing (NLP)** untuk memahami isi resume dan menggunakan algoritma **Machine Learning** untuk menentukan kategori pekerjaan yang paling sesuai.

Selain melakukan klasifikasi, sistem juga dapat memberikan:

✅ Prediksi kategori pekerjaan

✅ Confidence Score

✅ Top Matching Roles

✅ Persentase kecocokan pekerjaan

✅ Dashboard interaktif berbasis web

---

# 🎯 Latar Belakang

Dalam proses rekrutmen, perusahaan sering menerima ratusan hingga ribuan resume untuk setiap lowongan pekerjaan.

Proses screening secara manual membutuhkan waktu yang lama dan berpotensi menyebabkan kandidat yang berkualitas terlewatkan.

Melalui pemanfaatan AI dan NLP, proses klasifikasi resume dapat dilakukan secara otomatis sehingga membantu proses seleksi menjadi lebih cepat, efisien, dan akurat.

---

# 🧠 Tujuan Penelitian

- Mengembangkan sistem klasifikasi resume otomatis.
- Mengimplementasikan NLP untuk analisis dokumen resume.
- Membandingkan performa algoritma SVM dan Naive Bayes.
- Menentukan kategori pekerjaan yang sesuai berdasarkan isi resume.
- Membantu proses screening kandidat secara otomatis.

---

# 👨‍💻 Tim Pengembang

| Nama | NIM |
|--------|--------|
| Jakir Apriyan | 2406004 |
| Naila Azzahra | 2406013 |

---

# 📂 Dataset

Dataset yang digunakan berasal dari Kaggle.

### 🔗 Link Dataset

https://www.kaggle.com/datasets/trendcart/resume-dataset?resource=download

### Informasi Dataset

| Keterangan | Nilai |
|------------|------------|
| Jumlah Resume | 10.000 |
| Jumlah Kategori | 42 |
| Format Data | csv |
| Target | Kategori Pekerjaan |

---

# 🔄 Alur Pengerjaan Proyek

```text
Resume Dataset
      │
      ▼
Data Understanding
      │
      ▼
Exploratory Data Analysis (EDA)
      │
      ▼
Text Preprocessing
      │
      ▼
Feature Engineering
      │
      ▼
TF-IDF Vectorization
      │
      ▼
Train-Test Split
      │
      ▼
Model Training
 (SVM & Naive Bayes)
      │
      ▼
Evaluation
      │
      ▼
Deployment Streamlit
```

---

# 🔍 Tahapan Penelitian

## 1️⃣ Business Understanding

Tahap awal dilakukan dengan mengidentifikasi permasalahan pada proses screening resume yang masih dilakukan secara manual.

Masalah utama:

- Proses seleksi memakan waktu lama.
- Jumlah resume sangat banyak.
- Sulit menentukan kategori pekerjaan yang sesuai.

---

## 2️⃣ Data Understanding

Tahap memahami karakteristik dataset.

Aktivitas yang dilakukan:

- Mengecek jumlah data.
- Mengecek jumlah kategori.
- Analisis struktur dataset.
- Analisis distribusi kategori.

---

## 3️⃣ Exploratory Data Analysis (EDA)

EDA dilakukan untuk memperoleh insight terhadap data.

Analisis yang dilakukan:

- Distribusi kategori pekerjaan.
- Distribusi panjang resume.
- Resume terpendek dan terpanjang.
- Analisis frekuensi kata.
- Visualisasi data.

---

## 4️⃣ Data Preparation

### Text Cleaning

Proses pembersihan data:

- Lowercase
- Remove URL
- Remove Number
- Remove Punctuation
- Remove Extra Spaces

### Feature Engineering

Fitur tambahan yang dibuat:

- Resume Length
- Word Count
- Character Count

### Feature Extraction

Menggunakan:

**TF-IDF Vectorizer**

untuk mengubah teks menjadi representasi numerik.

### Label Encoding

Mengubah label kategori menjadi bentuk numerik menggunakan Label Encoder.

---

## 5️⃣ Modeling

Dua algoritma yang digunakan:

### Support Vector Machine (SVM)

Kelebihan:

- Cocok untuk data teks.
- Akurasi tinggi.
- Generalisasi baik.

### Naive Bayes

Kelebihan:

- Cepat.
- Ringan.
- Efektif untuk klasifikasi teks.

---

## 6️⃣ Evaluation

Evaluasi dilakukan menggunakan:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

# 📊 Hasil Penelitian

## Performa Model

| Algoritma | Accuracy | Precision | Recall | F1-Score |
|------------|------------|------------|------------|------------|
| SVM | 100% | 100% | 100% | 100% |
| Naive Bayes | 100% | 100% | 100% | 100% |

---

## Kesimpulan Evaluasi

- Kedua algoritma berhasil mengklasifikasikan seluruh data testing dengan benar.
- Error Rate yang diperoleh sebesar **0%**.
- TF-IDF mampu merepresentasikan informasi penting dalam resume dengan sangat baik.
- Model berhasil mempelajari pola antar kategori pekerjaan secara optimal.

---

# 🌐 Implementasi Web

Aplikasi dikembangkan menggunakan **Streamlit**.

### Fitur Utama

📄 Upload Resume PDF

📊 Resume Analysis

🎯 Job Category Prediction

📈 Confidence Score

🏆 Top Matching Roles

⚡ Fast Prediction

---

# 🛠️ Teknologi yang Digunakan

## Bahasa Pemrograman

- Python

## Library

- Pandas
- NumPy
- Scikit-Learn
- NLTK
- Matplotlib
- Seaborn
- Joblib
- Streamlit

---

# 📁 Struktur Repository

```bash
AI-Resume-Analyzer/
│
├── README.md
├── Laporan_uas.md
├── AI_Resume_Analyzer.ipynb
├── requirements.txt
│
├── dataset/
│   └── Resume.csv
│
├── models/
│   ├── svm_model.pkl
│   ├── nb_model.pkl
│   ├── tfidf.pkl
│   └── label_encoder.pkl
│
├── app/
│   └── streamlit_app.py
│
└── assets/
    ├── dashboard.png
    ├── eda.png
    ├── confusion_matrix.png
    └── architecture.png
```

---

# 🚀 Cara Menjalankan

### Clone Repository

```bash
git clone https://github.com/username/AI-Resume-Analyzer.git
```

### Masuk Folder Project

```bash
cd AI-Resume-Analyzer
```

### Install Dependency

```bash
pip install -r requirements.txt
```

### Jalankan Streamlit

```bash
streamlit run app.py
```

---

# 📸 Screenshot

## Dashboard

> Tambahkan screenshot dashboard Streamlit di sini

## EDA

> Tambahkan visualisasi EDA di sini

## Hasil Prediksi

> Tambahkan screenshot hasil prediksi di sini

---

# 📚 Referensi

1. Resume Dataset Kaggle
2. Scikit-Learn Documentation
3. Streamlit Documentation
4. Baral (2026) - AI Resume Analyzer
5. Santoso & Widodo (2026) - Multi-Layer Pattern Recognition
6. Pujiastuti dkk. (2025) - Pemanfaatan AI dalam Pengolahan Teks

---

<div align="center">

### ⭐ AI Resume Analyzer ⭐

Proyek UAS Mata Kuliah Kecerdasan Buatan  
Program Studi Teknik Informatika

</div>
