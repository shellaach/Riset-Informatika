BAB III
METODOLOGI PENELITIAN

3.1 Jenis dan Pendekatan Penelitian

Penelitian ini menggunakan pendekatan kuantitatif dengan metode eksperimen komparatif (comparative experimental method).
Tujuan pendekatan ini adalah untuk membandingkan hasil dua algoritma machine learning, Logistic Regression dan Random Forest dalam melakukan prediksi kelulusan mahasiswa berdasarkan data yang telah dikumpulkan.
Data yang digunakan berupa data numerik (nilai, kehadiran, dan aktivitas akademik), yang kemudian diolah dan dianalisis menggunakan perangkat lunak berbasis Python untuk membangun serta mengevaluasi model prediksi.


3.2 Populasi dan Sampel Penelitian

3.2.1 Populasi
Populasi dalam penelitian ini adalah seluruh mahasiswa pada program studi Informatika di Universitas Pembangunan Nasional “Veteran” Jawa Timur.

3.2.2 Sampel
Sampel penelitian diambil dari sebagian data mahasiswa yang memiliki informasi lengkap mengenai nilai, kehadiran, serta aktivitas akademik. Jumlah sampel minimal 200 data mahasiswa agar hasil model dapat digeneralisasi dengan baik.
Teknik pengambilan sampel yang digunakan adalah purposive sampling, yaitu pemilihan data berdasarkan kelengkapan atribut dan kesesuaian dengan tujuan penelitian.


3.3 Variabel Penelitian dan Definisi Operasional

3.3.1 Variabel Dependen (Y)
• Status Kelulusan Mahasiswa
Variabel ini menunjukkan apakah mahasiswa lulus tepat waktu atau tidak.
Kategorinya dibagi menjadi:
o 1 = Lulus
o 0 = Tidak Lulus

3.3.2 Variabel Independen (X)

1. Nilai Akademik (X1): rata-rata gabungan dari nilai tugas, UTS, dan UAS mahasiswa.
2. Kehadiran (X2): persentase kehadiran mahasiswa selama mengikuti perkuliahan.
3. Aktivitas Akademik (X3): skor partisipasi mahasiswa dalam kegiatan akademik seperti organisasi, seminar, atau lomba ilmiah.
   Semua variabel ini akan digunakan sebagai input untuk model prediksi Logistic Regression dan Random Forest.

3.4 Teknik Pengumpulan Data

Data yang digunakan terdiri dari:

1. Data sekunder — diperoleh dari sistem akademik kampus yang berisi nilai dan kehadiran mahasiswa.
2. Data primer (opsional) — dikumpulkan melalui kuesioner sederhana untuk mengukur tingkat aktivitas akademik mahasiswa (misalnya: jumlah kegiatan, seminar, atau organisasi yang diikuti).
   Format data yang digunakan berbentuk CSV (Comma Separated Values) agar dapat diolah menggunakan Python.
   Contoh struktur data yang digunakan:
   ID Nilai_Tugas Nilai_UTS Nilai_UAS Kehadiran Aktivitas Status_Kelulusan
   1 80 75 85 90 8 1
   2 60 55 58 65 5 0
   3 78 80 79 88 7 1


3.5 Teknik Analisis Data
Langkah-langkah analisis data dalam penelitian ini dijelaskan sebagai berikut:

1. Pra-pemrosesan Data
   • Membersihkan data dari nilai kosong (missing value) atau data ganda.
   • Menormalisasi atau menstandarkan data numerik (khusus untuk Logistic Regression).
   • Mengonversi data kategorikal ke bentuk numerik menggunakan label encoding.
   • Membagi dataset menjadi data latih (80%) dan data uji (20%).

2. Pembangunan Model
   • Model 1: Logistic Regression
   o Menggunakan fungsi logit untuk memprediksi probabilitas kelulusan.
   o Dilatih menggunakan Scikit-learn dengan parameter regularisasi C yang dioptimasi.
   • Model 2: Random Forest
   o Menggunakan beberapa Decision Tree dengan metode bagging.
   o Parameter penting: n_estimators, max_depth, dan min_samples_leaf.
   o Optimasi parameter dilakukan dengan GridSearchCV.

3. Evaluasi Model
   Kinerja model diukur menggunakan beberapa metrik berikut:
   • Accuracy – proporsi prediksi yang benar.
   • Precision – ketepatan model dalam memprediksi mahasiswa lulus.
   • Recall – kemampuan model mendeteksi semua mahasiswa yang benar-benar lulus.
   • F1-Score – rata-rata harmonik dari Precision dan Recall.
   • ROC-AUC – menunjukkan kemampuan model membedakan kelas 1 dan 0.
   Model dengan nilai F1-Score dan AUC paling tinggi dianggap memiliki kinerja terbaik.

4. Analisis Hasil
   Hasil dari kedua model dibandingkan untuk melihat:
   • Perbedaan performa antara Logistic Regression dan Random Forest.
   • Fitur (variabel) yang paling berpengaruh terhadap kelulusan mahasiswa.
   Interpretasi dilakukan berdasarkan feature importance pada Random Forest dan nilai koefisien pada Logistic Regression.


3.6 Alat dan Bahan Penelitian

Alat yang digunakan dalam penelitian ini meliputi:
• Perangkat Lunak: Python 3.10, Google Colab / Jupyter Notebook
• Library Python: pandas, numpy, scikit-learn, matplotlib, seaborn
• Perangkat Keras: Laptop dengan spesifikasi minimal RAM 8 GB dan prosesor Intel i5 atau setara.
