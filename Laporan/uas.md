# AI Resume Analyzer
## Klasifikasi Kategori Pekerjaan Berdasarkan Resume Menggunakan TF-IDF dan Support Vector Machine

---

# Identitas Kelompok

| Nama | NIM |
|--------|--------|
| Jakir Apriyan | 2406004 |
| Nama Anggota 2 | XXXXXXX |

---

# 1. Business Understanding

## 1.1 Latar Belakang

Perkembangan teknologi Artificial Intelligence (AI) telah membawa perubahan signifikan dalam berbagai bidang, termasuk proses rekrutmen tenaga kerja. Saat ini perusahaan sering menerima ratusan hingga ribuan resume untuk setiap lowongan pekerjaan yang dibuka. Kondisi tersebut menyebabkan proses screening kandidat secara manual menjadi tidak efisien dan membutuhkan waktu yang cukup lama.

Menurut Baral (2026), proses seleksi resume tradisional masih mengandalkan pencocokan kata kunci sederhana dan penilaian manusia sehingga berpotensi menyebabkan kandidat yang memenuhi kualifikasi terlewatkan ataupun kandidat yang kurang sesuai lolos ke tahap berikutnya. Oleh karena itu, dibutuhkan sistem cerdas yang mampu melakukan analisis dan klasifikasi resume secara otomatis.

Kemajuan Natural Language Processing (NLP) memungkinkan komputer memahami, menganalisis, dan mengolah dokumen teks secara otomatis. Dengan memanfaatkan teknik NLP dan Machine Learning, sistem dapat mempelajari pola dari data resume dan mengelompokkannya ke dalam kategori pekerjaan yang sesuai.

Proyek ini mengembangkan sistem **AI Resume Analyzer** yang mampu melakukan klasifikasi resume menggunakan metode TF-IDF sebagai ekstraksi fitur dan algoritma Support Vector Machine (SVM) serta Naive Bayes sebagai model klasifikasi.

---

## 1.2 Identifikasi Masalah

Berdasarkan latar belakang yang telah dijelaskan, permasalahan yang dapat diidentifikasi adalah:

1. Proses screening resume masih dilakukan secara manual.
2. Jumlah resume yang besar menyebabkan proses seleksi menjadi lambat.
3. Sulit menentukan kategori pekerjaan yang paling sesuai berdasarkan isi resume.
4. Diperlukan sistem otomatis yang mampu membantu proses klasifikasi resume secara cepat dan akurat.

---

## 1.3 Rumusan Masalah

1. Bagaimana membangun sistem klasifikasi resume menggunakan teknik NLP?
2. Bagaimana performa algoritma Support Vector Machine dan Naive Bayes dalam mengklasifikasikan resume?
3. Algoritma manakah yang menghasilkan performa terbaik?

---

## 1.4 Tujuan Penelitian

Tujuan penelitian ini adalah:

- Mengembangkan sistem klasifikasi resume berbasis NLP.
- Mengimplementasikan metode TF-IDF untuk ekstraksi fitur teks.
- Membandingkan performa algoritma SVM dan Naive Bayes.
- Menentukan model terbaik untuk klasifikasi resume.
- Membantu proses screening kandidat secara otomatis.

---

## 1.5 Manfaat Penelitian

### Bagi Perusahaan

- Mempercepat proses screening kandidat.
- Mengurangi beban kerja HRD.
- Membantu menentukan kandidat yang sesuai dengan posisi pekerjaan.

### Bagi Peneliti

- Menambah wawasan mengenai NLP dan Machine Learning.
- Menerapkan metode klasifikasi teks pada kasus nyata.

---

# 2. Literature Review

## 2.1 Penelitian Terdahulu

### Penelitian 1

Baral (2026) mengembangkan sistem AI Resume Analyzer berbasis Large Language Models (LLM) yang mampu melakukan ekstraksi informasi resume, semantic matching, dan pemberian rekomendasi terhadap kandidat. Sistem tersebut menunjukkan bahwa AI mampu membantu proses rekrutmen secara otomatis dengan tingkat akurasi yang tinggi.

### Penelitian 2

Santoso dan Widodo (2026) mengembangkan sistem deteksi teks berbasis Artificial Intelligence menggunakan pendekatan Multi-Layer Pattern Recognition. Sistem tersebut mampu mencapai akurasi sebesar 87,3% melalui analisis fitur linguistik, struktural, dan statistik pada dokumen teks.

### Penelitian 3

Pujiastuti dkk. (2025) menjelaskan bahwa teknologi AI memiliki kemampuan dalam memahami, menganalisis, dan memproses dokumen teks secara otomatis sehingga dapat meningkatkan efisiensi pekerjaan yang sebelumnya dilakukan secara manual.

---

## 2.2 Research Gap

| Penelitian | Metode | Keterbatasan |
|------------|---------|--------------|
| Baral (2026) | LLM + Semantic Matching | Fokus pada evaluasi resume menggunakan LLM dan belum membandingkan algoritma klasifikasi tradisional |
| Santoso & Widodo (2026) | Multi-Layer Pattern Recognition | Fokus pada deteksi teks AI, bukan klasifikasi resume |
| Pujiastuti dkk. (2025) | Analisis penggunaan AI | Tidak membahas klasifikasi resume |

Berdasarkan penelitian terdahulu, belum ditemukan penelitian yang secara spesifik membandingkan algoritma Support Vector Machine (SVM) dan Naive Bayes pada dataset Resume Dataset untuk klasifikasi kategori pekerjaan.

---

## 2.3 Novelty Penelitian

Pembaruan yang ditawarkan pada penelitian ini adalah:

1. Menggunakan dataset Resume Dataset dari Kaggle.
2. Mengimplementasikan metode TF-IDF untuk ekstraksi fitur.
3. Membandingkan algoritma Support Vector Machine (SVM) dan Naive Bayes.
4. Menyediakan fitur Confidence Score.
5. Menampilkan Top Matching Roles.
6. Mengimplementasikan sistem berbasis web menggunakan Streamlit.

---

# 3. Data Understanding

## Dataset

Dataset yang digunakan berasal dari Kaggle:

**Link Dataset:**

https://www.kaggle.com/datasets/gauravduttakiit/resume-dataset

### Informasi Dataset

| Informasi | Nilai |
|------------|--------|
| Jumlah Data | 10.000 Resume |
| Jumlah Kategori | 42 |
| Bentuk Data | Teks |
| Target | Kategori Pekerjaan |

---

## Contoh Kategori

- Data Science
- HR
- Java Developer
- Python Developer
- Testing
- Business Analyst
- Sales
- Network Security Engineer
- DevOps Engineer
- Web Designer

---

# 4. Exploratory Data Analysis (EDA)

EDA dilakukan untuk memahami karakteristik data sebelum proses pelatihan model.

Analisis yang dilakukan meliputi:

## Distribusi Kategori

Menampilkan jumlah resume pada setiap kategori pekerjaan.

## Distribusi Panjang Resume

Mengukur jumlah kata pada setiap resume untuk mengetahui variasi panjang dokumen.

## Resume Terpanjang dan Terpendek

Mengetahui distribusi panjang teks pada dataset.

## Word Frequency Analysis

Menganalisis kata-kata yang paling sering muncul dalam resume.

## Boxplot Panjang Resume

Digunakan untuk mendeteksi outlier pada panjang resume.

---

# 5. Data Preparation

Tahap preprocessing dilakukan untuk membersihkan dan menyiapkan data sebelum proses pelatihan model.

## Text Cleaning

Tahapan yang dilakukan:

- Convert to Lowercase
- Remove URL
- Remove Number
- Remove Punctuation
- Remove Extra Spaces

---

## Feature Engineering

Membuat fitur tambahan:

- Resume Length
- Word Count
- Character Count

---

## Feature Extraction

Metode yang digunakan:

### TF-IDF Vectorizer

TF-IDF digunakan untuk mengubah dokumen teks menjadi representasi numerik sehingga dapat diproses oleh algoritma Machine Learning.

---

## Encoding Target

Menggunakan:

```python
LabelEncoder()
```

untuk mengubah label kategori menjadi bentuk numerik.

---

## Split Dataset

Perbandingan data:

- Training Data : 80%
- Testing Data : 20%

---

# 6. Modeling

Penelitian ini menggunakan dua algoritma klasifikasi.

## Support Vector Machine (SVM)

Kelebihan:

- Cocok untuk data teks berdimensi tinggi.
- Memiliki kemampuan generalisasi yang baik.
- Sering digunakan pada kasus klasifikasi dokumen.

---

## Naive Bayes

Kelebihan:

- Cepat dalam proses pelatihan.
- Sederhana dan efisien.
- Cocok digunakan pada klasifikasi teks.

---

# 7. Evaluation

Evaluasi model dilakukan untuk mengukur performa algoritma dalam mengklasifikasikan resume ke dalam kategori pekerjaan yang sesuai.

## Metrik Evaluasi

Metrik yang digunakan dalam penelitian ini adalah:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

## Hasil Evaluasi Model

### Support Vector Machine (SVM)

| Metrik | Nilai |
|---------|---------|
| Accuracy | 100% |
| Precision | 100% |
| Recall | 100% |
| F1-Score | 100% |

### Naive Bayes

| Metrik | Nilai |
|---------|---------|
| Accuracy | 100% |
| Precision | 100% |
| Recall | 100% |
| F1-Score | 100% |

---

## Perbandingan Model

| Algoritma | Accuracy | Precision | Recall | F1-Score |
|------------|------------|------------|------------|------------|
| Support Vector Machine | 100% | 100% | 100% | 100% |
| Naive Bayes | 100% | 100% | 100% | 100% |

---

## Confusion Matrix

Berdasarkan hasil pengujian, seluruh data pada testing set berhasil diklasifikasikan dengan benar oleh kedua model.

Nilai False Positive (FP) dan False Negative (FN) tidak ditemukan sehingga tingkat kesalahan klasifikasi (Error Rate) sebesar:

**Error Rate = 0%**

Hal ini menunjukkan bahwa model mampu mengenali seluruh kategori resume yang terdapat pada data pengujian tanpa menghasilkan prediksi yang salah.

---

## Analisis Hasil

Hasil pengujian menunjukkan bahwa algoritma Support Vector Machine (SVM) dan Naive Bayes memperoleh performa yang sangat baik dengan nilai Accuracy, Precision, Recall, dan F1-Score masing-masing sebesar 100%.

Tingginya performa model menunjukkan bahwa metode TF-IDF berhasil mengekstraksi informasi penting dari dokumen resume sehingga pola antar kategori pekerjaan dapat dipelajari dengan baik oleh model klasifikasi.

Selain itu, karakteristik dataset Resume Dataset yang memiliki perbedaan kata kunci yang cukup jelas antar kategori pekerjaan turut berkontribusi terhadap tingginya performa model.

Meskipun hasil evaluasi menunjukkan performa sempurna pada data pengujian, pengujian menggunakan dataset eksternal atau data dunia nyata tetap diperlukan untuk memastikan kemampuan generalisasi model terhadap data yang belum pernah dilihat sebelumnya.

---

# 8. Implementasi Sistem

Sistem AI Resume Analyzer dikembangkan menggunakan framework Streamlit sehingga dapat digunakan secara interaktif melalui web browser.

## Fitur Sistem

### Upload Resume

Pengguna dapat mengunggah file resume dalam format PDF.

### Resume Preview

Sistem menampilkan isi resume yang telah diunggah sehingga pengguna dapat melakukan pengecekan sebelum proses analisis.

### Resume Classification

Model Machine Learning melakukan prediksi kategori pekerjaan berdasarkan isi resume.

### Confidence Score

Menampilkan tingkat keyakinan model terhadap hasil prediksi yang diberikan.

### Top Matching Roles

Menampilkan beberapa kategori pekerjaan yang paling sesuai dengan resume beserta skor kecocokannya.

### Dashboard Interaktif

Menyajikan hasil analisis secara visual dan mudah dipahami oleh pengguna.

---

# 9. Kesimpulan

Berdasarkan hasil penelitian yang telah dilakukan, dapat disimpulkan bahwa metode Natural Language Processing (NLP) dengan TF-IDF berhasil digunakan untuk mengubah dokumen resume menjadi representasi numerik yang dapat diproses oleh algoritma Machine Learning.

Algoritma Support Vector Machine (SVM) dan Naive Bayes berhasil mengklasifikasikan resume ke dalam kategori pekerjaan dengan performa yang sangat baik. Hasil evaluasi menunjukkan bahwa kedua model memperoleh nilai Accuracy, Precision, Recall, dan F1-Score sebesar 100%.

Tidak ditemukan kesalahan klasifikasi pada data pengujian sehingga Error Rate yang diperoleh adalah 0%.

Hasil tersebut menunjukkan bahwa kombinasi teknik preprocessing teks, ekstraksi fitur menggunakan TF-IDF, dan algoritma klasifikasi yang digunakan mampu mempelajari pola pada dataset Resume Dataset secara optimal.

Sistem AI Resume Analyzer yang dikembangkan juga berhasil diimplementasikan dalam bentuk aplikasi web berbasis Streamlit yang mampu memberikan prediksi kategori pekerjaan, confidence score, dan rekomendasi pekerjaan yang sesuai dengan isi resume.

---

# 10. Saran

Beberapa pengembangan yang dapat dilakukan pada penelitian selanjutnya antara lain:

1. Menggunakan dataset resume yang lebih beragam dan berasal dari dunia industri.
2. Menambahkan algoritma klasifikasi lain seperti Random Forest, XGBoost, atau BERT.
3. Melakukan pengujian menggunakan data resume baru yang belum terdapat pada dataset pelatihan.
4. Menambahkan fitur analisis keterampilan (skill analysis) dan rekomendasi pengembangan karier.
5. Mengintegrasikan sistem dengan platform rekrutmen berbasis web secara langsung.
