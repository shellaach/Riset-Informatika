# BAB I

## PENDAHULUAN

### 1.1 Latar Belakang

Pendidikan tinggi merupakan salah satu faktor penting dalam membentuk sumber daya manusia yang berkualitas. Salah satu indikator keberhasilan institusi pendidikan adalah tingkat kelulusan mahasiswa tepat waktu. Namun, banyak faktor yang memengaruhi kelulusan mahasiswa, seperti nilai akademik, tingkat kehadiran, dan aktivitas akademik di luar perkuliahan.

Perkembangan teknologi informasi memungkinkan proses analisis data dilakukan secara lebih cepat dan akurat menggunakan pendekatan _machine learning_. Dengan memanfaatkan data historis mahasiswa, model prediksi dapat dibangun untuk memperkirakan kemungkinan seorang mahasiswa lulus tepat waktu. Hal ini membantu pihak kampus dalam mendeteksi mahasiswa yang berisiko tidak lulus dan memberikan bimbingan lebih dini.

Dalam penelitian ini, penulis membandingkan dua algoritma klasifikasi populer yaitu _Logistic Regression_ dan _Random Forest_. _Logistic Regression_ memiliki kelebihan dalam hal interpretasi hasil dan kemudahan analisis statistik, sedangkan _Random Forest_ dikenal lebih unggul dalam akurasi pada data yang kompleks. Melalui perbandingan ini, diharapkan dapat diketahui model mana yang memberikan hasil terbaik dalam memprediksi kelulusan mahasiswa berdasarkan nilai akademik, kehadiran, dan aktivitas akademik.

### 1.2 Rumusan Masalah

1. Bagaimana penerapan algoritma _Logistic Regression_ dan _Random Forest_ dalam memprediksi kelulusan mahasiswa?
2. Bagaimana kinerja kedua algoritma tersebut berdasarkan metrik evaluasi seperti akurasi, presisi, _recall_, dan _F1-score_?
3. Algoritma mana yang memiliki kinerja lebih baik untuk kasus prediksi kelulusan mahasiswa?

### 1.3 Tujuan Penelitian

Tujuan dari penelitian ini adalah:

1. Menerapkan algoritma _Logistic Regression_ dan _Random Forest_ dalam memprediksi kelulusan mahasiswa.
2. Membandingkan kinerja kedua algoritma berdasarkan hasil evaluasi model.
3. Mengidentifikasi faktor yang paling berpengaruh terhadap kelulusan mahasiswa berdasarkan hasil analisis fitur.

### 1.4 Manfaat Penelitian

**a. Manfaat Teoritis**  
Penelitian ini diharapkan dapat menjadi referensi akademik dalam penerapan algoritma _machine learning_ untuk prediksi kelulusan mahasiswa, serta memberikan kontribusi terhadap penelitian di bidang _Educational Data Mining (EDM)_.

**b. Manfaat Praktis**  
Hasil penelitian ini dapat membantu pihak fakultas atau program studi dalam melakukan pemantauan akademik serta memberikan intervensi dini kepada mahasiswa yang berisiko tidak lulus tepat waktu.

### 1.5 Batasan Masalah

Agar penelitian ini lebih terarah dan mudah dilakukan, penulis memberikan beberapa batasan sebagai berikut:

1. Penelitian ini hanya membahas tiga faktor utama yang dianggap berpengaruh terhadap kelulusan mahasiswa, yaitu nilai akademik, tingkat kehadiran, dan aktivitas akademik.
2. Data yang digunakan berasal dari data akademik mahasiswa Program Studi Informatika UPN “Veteran” Jawa Timur, atau menggunakan data simulasi yang dibuat menyerupai kondisi sebenarnya.
3. Algoritma yang dibandingkan dalam penelitian ini hanya dua, yaitu _Logistic Regression_ dan _Random Forest_.
4. Penelitian ini tidak membahas faktor non-akademik seperti motivasi, kondisi ekonomi, atau lingkungan sosial mahasiswa.
5. Proses pengujian model dilakukan dengan pembagian data latih dan data uji sebesar 80:20, sehingga hasil akurasi hanya menggambarkan performa model pada data yang digunakan.
