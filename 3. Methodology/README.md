# BAB III

## METODOLOGI PENELITIAN

### 3.1 Jenis dan Pendekatan Penelitian

Penelitian ini menggunakan pendekatan kuantitatif dengan metode eksperimen komparatif (_comparative experimental method_).  
Tujuan pendekatan ini adalah membandingkan hasil dua algoritma _machine learning_, yaitu _Logistic Regression_ dan _Random Forest_, dalam memprediksi kelulusan mahasiswa berdasarkan data yang dikumpulkan.  
Data yang digunakan berupa data numerik (nilai, kehadiran, dan aktivitas akademik), kemudian diolah dan dianalisis menggunakan Python untuk membangun serta mengevaluasi model prediksi.

### 3.2 Populasi dan Sampel Penelitian

#### 3.2.1 Populasi

Populasi penelitian ini adalah seluruh mahasiswa Program Studi Informatika di Universitas Pembangunan Nasional “Veteran” Jawa Timur.

#### 3.2.2 Sampel

Sampel penelitian diambil dari sebagian mahasiswa yang memiliki data lengkap mengenai nilai, kehadiran, dan aktivitas akademik.  
Jumlah sampel minimal **200 data mahasiswa** agar hasil model dapat digeneralisasi dengan baik.  
Teknik pengambilan sampel menggunakan **purposive sampling**, yaitu pemilihan data berdasarkan kelengkapan atribut dan kesesuaian dengan tujuan penelitian.

### 3.3 Variabel Penelitian dan Definisi Operasional

#### 3.3.1 Variabel Dependen (Y)

**Status Kelulusan Mahasiswa**  
Menunjukkan apakah mahasiswa lulus tepat waktu atau tidak, dengan kategori:

- 1 = Lulus
- 0 = Tidak Lulus

#### 3.3.2 Variabel Independen (X)

1. **Nilai Akademik (X1):** rata-rata gabungan dari nilai tugas, UTS, dan UAS mahasiswa.
2. **Kehadiran (X2):** persentase kehadiran mahasiswa selama perkuliahan.
3. **Aktivitas Akademik (X3):** skor partisipasi dalam kegiatan akademik seperti organisasi, seminar, atau lomba ilmiah.

Ketiga variabel tersebut digunakan sebagai input untuk model _Logistic Regression_ dan _Random Forest_.

### 3.4 Teknik Pengumpulan Data

Data penelitian terdiri dari:

1. **Data sekunder** – diperoleh dari sistem akademik kampus yang berisi nilai dan kehadiran mahasiswa.
2. **Data primer (opsional)** – diperoleh melalui kuesioner sederhana untuk mengukur tingkat aktivitas akademik (jumlah kegiatan, seminar, atau organisasi yang diikuti).

Format data berbentuk **CSV (Comma Separated Values)** agar mudah diolah menggunakan Python.

Contoh struktur data:

| ID  | Nilai_Tugas | Nilai_UTS | Nilai_UAS | Kehadiran | Aktivitas | Status_Kelulusan |
| --- | ----------- | --------- | --------- | --------- | --------- | ---------------- |
| 1   | 80          | 75        | 85        | 90        | 8         | 1                |
| 2   | 60          | 55        | 58        | 65        | 5         | 0                |
| 3   | 78          | 80        | 79        | 88        | 7         | 1                |

### 3.5 Teknik Analisis Data

Langkah-langkah analisis data yang dilakukan dalam penelitian ini:

#### 1. Pra-pemrosesan Data

- Membersihkan data dari nilai kosong (_missing value_) atau duplikat.
- Menormalisasi atau menstandarkan data numerik (khusus untuk _Logistic Regression_).
- Mengonversi data kategorikal ke numerik menggunakan _Label Encoding_.
- Membagi dataset menjadi data latih (**80%**) dan data uji (**20%**).

#### 2. Pembangunan Model

- **Model 1: Logistic Regression**

  - Menggunakan fungsi _logit_ untuk memprediksi probabilitas kelulusan.
  - Dilatih menggunakan _Scikit-learn_ dengan parameter regularisasi **C** yang dioptimasi.

- **Model 2: Random Forest**
  - Menggunakan beberapa _Decision Tree_ dengan metode _bagging_.
  - Parameter penting: **n_estimators**, **max_depth**, dan **min_samples_leaf**.
  - Optimasi parameter dilakukan dengan _GridSearchCV_.

#### 3. Evaluasi Model

Kinerja model diukur menggunakan beberapa metrik berikut:

- **Accuracy** – proporsi prediksi yang benar.
- **Precision** – ketepatan model dalam memprediksi mahasiswa yang lulus.
- **Recall** – kemampuan model mendeteksi mahasiswa yang benar-benar lulus.
- **F1-Score** – rata-rata harmonik dari Precision dan Recall.
- **ROC-AUC** – kemampuan model membedakan antara kelas 1 dan 0.

Model dengan nilai F1-Score dan AUC tertinggi dianggap memiliki kinerja terbaik.

#### 4. Analisis Hasil

Hasil dari kedua model dibandingkan untuk melihat:

- Perbedaan performa antara _Logistic Regression_ dan _Random Forest_.
- Fitur (variabel) yang paling berpengaruh terhadap kelulusan mahasiswa.

Interpretasi dilakukan berdasarkan **feature importance** pada _Random Forest_ dan **koefisien regresi** pada _Logistic Regression_.

### 3.6 Alat dan Bahan Penelitian

- **Perangkat Lunak:** Python 3.10, Google Colab / Jupyter Notebook
- **Library Python:** pandas, numpy, scikit-learn, matplotlib, seaborn
- **Perangkat Keras:** Laptop dengan RAM minimal 8 GB dan prosesor Intel i5 atau setara
