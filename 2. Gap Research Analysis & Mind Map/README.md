# BAB II

## TINJAUAN PUSTAKA DAN KERANGKA PEMIKIRAN

### 2.1 Landasan Teori

#### 2.1.1 Machine Learning

_Machine Learning (ML)_ merupakan cabang dari kecerdasan buatan (_Artificial Intelligence/AI_) yang memungkinkan komputer mempelajari pola dari data dan membuat prediksi tanpa harus diprogram secara eksplisit (Laila dkk., 2025).  
Dalam bidang pendidikan, _machine learning_ dimanfaatkan untuk menganalisis data akademik mahasiswa, menemukan pola, dan memprediksi kemungkinan yang akan terjadi guna mendukung pengambilan keputusan.

#### 2.1.2 Educational Data Mining (EDM)

_Educational Data Mining (EDM)_ merupakan proses penambangan data pendidikan untuk mendapatkan informasi penting dari data akademik yang berguna bagi pengembangan pembelajaran (Selly & Arman, 2022).  
Melalui EDM, perguruan tinggi dapat mengidentifikasi mahasiswa yang berpotensi mengalami kendala akademik dan memberikan bimbingan lebih awal.

#### 2.1.3 Logistic Regression

Regresi logistik biner merupakan metode statistika sekaligus algoritma klasifikasi yang digunakan untuk memodelkan hubungan antara variabel dependen (Y) yang bersifat biner, seperti lulus atau tidak lulus, dengan satu atau lebih variabel independen (X) (Azis dkk., 2022).  
Model ini menghitung probabilitas suatu kejadian berdasarkan fungsi logit. Kelebihan regresi logistik adalah mudah diinterpretasi serta mampu menunjukkan seberapa besar pengaruh masing-masing variabel terhadap hasil akhir.

#### 2.1.4 Random Forest

_Random Forest_ merupakan algoritma berbasis _ensemble learning_ yang menggabungkan sejumlah _Decision Tree_ untuk meningkatkan akurasi prediksi (Harkamsyah, 2025).  
Setiap pohon dalam _Random Forest_ dibangun dari sampel acak data dan fitur, kemudian hasil akhirnya diperoleh melalui mekanisme voting.  
Kelebihan _Random Forest_ antara lain mampu menangani data non-linear, tahan terhadap _overfitting_, serta memberikan informasi mengenai _feature importance_ yang menunjukkan variabel paling berpengaruh.

#### 2.1.5 Faktor yang Mempengaruhi Kelulusan Mahasiswa

Menurut beberapa penelitian, faktor yang memengaruhi kelulusan mahasiswa meliputi:

1. **Nilai Akademik:** mencerminkan kemampuan dan pencapaian belajar.
2. **Kehadiran:** semakin tinggi kehadiran, semakin besar peluang lulus tepat waktu.
3. **Aktivitas Akademik:** keterlibatan dalam organisasi, seminar, atau kegiatan ilmiah dapat meningkatkan motivasi dan kemampuan sosial.

Penelitian ini berfokus pada tiga faktor yang dapat diukur secara objektif melalui data akademik: nilai, kehadiran, dan aktivitas akademik mahasiswa.

### 2.2 Penelitian Terdahulu

Beberapa penelitian sebelumnya telah dilakukan untuk memprediksi kelulusan mahasiswa dengan berbagai algoritma _machine learning_.  
Penelitian-penelitian ini menjadi dasar dan pembanding dalam penelitian yang dilakukan.

**Reyto Yogastiana (2025)** – _Prediksi Kelulusan Mahasiswa Menggunakan Algoritma Decision Tree C4.5_  
Menggunakan data simulatif sebanyak 200 mahasiswa dengan variabel IPK, jumlah SKS, kehadiran, dan lama studi.  
Hasil menunjukkan akurasi **85%**, dengan IPK sebagai faktor paling berpengaruh.

**Reki Kurnia Permana dkk. (2025)** – _Prediksi Kelulusan Mahasiswa dengan Menggunakan Algoritma Decision Tree_  
Menggunakan data nyata dari 161 mahasiswa Universitas Teknologi Digital Bandung.  
Akurasi model mencapai **90%**, dengan IPS semester 2 dan 3 serta status pekerjaan sebagai faktor utama.

**Rafika Syahranita, Suhartono, dan Syahiduz Zaman (2023)** – _Prediksi Kategori Kelulusan Mahasiswa Menggunakan Metode Regresi Logistik Multinomial_  
Menggunakan data 300 mahasiswa UIN Maulana Malik Ibrahim Malang untuk mengklasifikasikan mahasiswa menjadi tiga kategori: cepat, tepat waktu, dan lambat.  
Akurasi model **85,5%**, _recall_ **93,9%**, dengan IP tiap semester menjadi faktor dominan.

**Harkamsyah Andrianof, Aggy Pramana Gusman, dan Okta Andrica Putra (2025)** – _Implementasi Algoritma Random Forest untuk Prediksi Kelulusan Mahasiswa Berdasarkan Data Akademik_  
Menggunakan data dari beberapa program studi di Universitas Putra Indonesia YPTK Padang.  
Akurasi **87,5%**, ROC-AUC **0,912**, dengan IPK dan kehadiran sebagai variabel paling berpengaruh.

Dari keempat penelitian tersebut dapat disimpulkan bahwa algoritma seperti _Decision Tree_, _Logistic Regression_, dan _Random Forest_ telah terbukti efektif dengan akurasi di atas **80%**.  
Namun, sebagian besar penelitian belum membandingkan secara langsung model linear (_Logistic Regression_) dengan model ensemble (_Random Forest_), serta belum mempertimbangkan aktivitas akademik sebagai variabel tambahan.  
Hal ini menjadi dasar (_research gap_) penelitian ini.

### 2.3 Kerangka Pemikiran (Model Penelitian)

Penelitian ini berasumsi bahwa nilai akademik (X1), tingkat kehadiran (X2), dan aktivitas akademik (X3) berpengaruh terhadap kelulusan mahasiswa (Y).  
Model prediksi dibuat menggunakan dua algoritma, yaitu _Logistic Regression_ dan _Random Forest_, untuk melihat perbandingan kinerjanya.

**Hubungan antar variabel:**  
Nilai Akademik (X1)  
│  
Kehadiran (X2) → Logistic Regression & Random Forest → Prediksi Kelulusan Mahasiswa (Y) (Tepat Waktu / Tidak Tepat Waktu)  
│  
Aktivitas Akademik (X3)

Model ini menunjukkan bahwa ketiga variabel (X1, X2, X3) diolah menggunakan dua model _machine learning_ berbeda untuk menghasilkan prediksi kelulusan mahasiswa (Y).

### 2.4 Hipotesis Penelitian

1. **H1:** Algoritma _Random Forest_ memiliki tingkat akurasi lebih tinggi dibandingkan _Logistic Regression_ dalam memprediksi kelulusan mahasiswa.
2. **H2:** Variabel IPK dan tingkat kehadiran berpengaruh signifikan terhadap hasil prediksi kelulusan mahasiswa.
3. **H3:** Penambahan variabel aktivitas akademik dapat meningkatkan akurasi model prediksi kelulusan.
