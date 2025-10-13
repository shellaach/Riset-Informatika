BAB II
TINJAUAN PUSTAKA DAN KERANGKA PEMIKIRAN

2.1 Landasan Teori

2.1.1 Machine Learning

Machine Learning (ML) merupakan salah satu cabang dari kecerdasan buatan (Artificial Intelligence/AI) yang memungkinkan komputer mempelajari pola dari data dan membuat prediksi tanpa harus diprogram secara langsung. (Laila dkk., 2025).
Dalam bidang pendidikan, machine learning dapat dimanfaatkan untuk menganalisis data akademik mahasiswa, menemukan pola, dan memprediksi kemungkinan yang akan terjadi guna mendukung pengambilan keputusan.

2.1.2 Educational Data Mining (EDM)

Educational Data Mining (EDM) merupakan proses penambangan data pendidikan untuk mendapatkan informasi tersirat dan mengekstrak informasi penting pada data pendidikan yang berguna bagi pengembangan pembelajaran. (Selly & Arman, 2022).
Melalui penerapan EDM, perguruan tinggi dapat mengetahui lebih awal mahasiswa yang berpotensi mengalami kendala akademik, sehingga bisa segera diberikan pendampingan atau bimbingan lebih awal.

2.1.3 Logistic Regression

Regresi logistik biner merupakan metode statistika sekaligus algoritma klasifikasi yang digunakan untuk memodelkan hubungan antara variabel dependen (Y) yang bersifat biner atau dikotomus (seperti lulus atau tidak lulus), dengan satu atau lebih variabel independen (X) yang dapat berupa data kualitatif, kuantitatif, atau kombinasi keduanya (Azis dkk., 2022). Model ini menghitung probabilitas suatu kejadian berdasarkan fungsi logit. Kelebihan regresi logistik adalah mudah diinterpretasi serta mampu menunjukkan seberapa besar pengaruh masing-masing variabel terhadap hasil akhir

2.1.4 Random Forest

Random Forest merupakan algoritma berbasis ensemble learning yang menggabungkan sejumlah Decision Tree untuk meningkatkan akurasi prediksi (Harkamsyah, 2025). Setiap pohon dalam Random Forest dibangun dari sampel acak data dan fitur, kemudian hasil akhirnya diperoleh melalui mekanisme voting.
Kelebihan Random Forest antara lain mampu menangani data non-linear, tahan terhadap overfitting, serta dapat memberikan informasi mengenai feature importance yang menunjukkan variabel paling berpengaruh.

2.1.5 Faktor yang Mempengaruhi Kelulusan Mahasiswa

Menurut beberapa penelitian, faktor yang memengaruhi kelulusan mahasiswa meliputi:

1. Nilai Akademik: mencerminkan kemampuan dan pencapaian belajar.
2. Kehadiran: semakin tinggi kehadiran, semakin besar peluang lulus tepat waktu.
3. Aktivitas Akademik: keterlibatan dalam organisasi, seminar, atau kegiatan ilmiah dapat meningkatkan kemampuan sosial dan motivasi belajar.
   Meskipun terdapat berbagai faktor lain seperti motivasi, stres akademik, dukungan sosial, dan latar belakang ekonomi yang juga berpengaruh terhadap kelulusan mahasiswa, penelitian ini berfokus pada faktor-faktor yang dapat diukur secara objektif melalui data akademik, yaitu nilai, kehadiran, dan aktivitas akademik mahasiswa.

2.2 Penelitian Terdahulu

Beberapa penelitian sebelumnya telah dilakukan untuk memprediksi kelulusan mahasiswa dengan berbagai algoritma machine learning. Penelitian-penelitian tersebut menjadi dasar dan pembanding dalam penelitian ini, khususnya terkait penggunaan algoritma klasifikasi seperti Decision Tree, Random Forest, dan Logistic Regression.

Penelitian oleh Reyto Yogastiana (2025) berjudul “Prediksi Kelulusan Mahasiswa Menggunakan Algoritma Decision Tree C4.5” membangun model prediksi kelulusan menggunakan data simulatif sebanyak 200 mahasiswa dengan variabel IPK, jumlah SKS, kehadiran, dan lama studi. Hasil penelitian menunjukkan bahwa algoritma Decision Tree C4.5 mampu menghasilkan akurasi sebesar 85%, dengan IPK sebagai faktor yang paling berpengaruh terhadap kelulusan. Penelitian ini menunjukkan bahwa Decision Tree mudah dipahami dan efektif untuk data akademik, meskipun masih terbatas pada data buatan dan belum dibandingkan dengan algoritma lain.

Selanjutnya, penelitian oleh Reki Kurnia Permana dkk. (2025) berjudul “Prediksi Kelulusan Mahasiswa dengan Menggunakan Algoritma Decision Tree” menggunakan data nyata dari 161 mahasiswa Universitas Teknologi Digital Bandung dengan variabel IPS semester 1–6, status pekerjaan, dan jenis kelamin. Hasil penelitian menunjukkan akurasi model sebesar 90%, dengan faktor yang paling berpengaruh terhadap kelulusan yaitu IPS semester 2 dan 3, serta status mahasiswa bekerja atau tidak bekerja. Penelitian ini menegaskan bahwa performa akademik di awal masa studi berpengaruh besar terhadap ketepatan waktu kelulusan. Namun, penelitian ini belum melibatkan algoritma pembanding untuk mengukur tingkat keakuratan yang lebih luas.

Penelitian oleh Rafika Syahranita, Suhartono, dan Syahiduz Zaman (2023) berjudul “Prediksi Kategori Kelulusan Mahasiswa Menggunakan Metode Regresi Logistik Multinomial” dilakukan di UIN Maulana Malik Ibrahim Malang dengan menggunakan data sebanyak 300 mahasiswa angkatan 2012–2018. Variabel yang digunakan meliputi jenis kelamin, jalur masuk, serta IP semester 1–6. Model Regresi Logistik Multinomial digunakan untuk mengklasifikasikan mahasiswa ke dalam tiga kategori: lulus cepat, tepat waktu, dan lambat. Hasil penelitian menunjukkan tingkat akurasi sebesar 85,5% dan recall sebesar 93,9%, dengan IP tiap semester menjadi faktor yang paling berpengaruh. Kelebihan penelitian ini adalah kemampuannya dalam menangani lebih dari dua kategori klasifikasi dan hasil model yang mudah diinterpretasikan. Namun, metode ini kurang optimal untuk data non-linear dan belum dibandingkan dengan model
yang lebih kompleks seperti Random Forest.

Penelitian berikutnya dilakukan oleh Harkamsyah Andrianof, Aggy Pramana Gusman, dan Okta Andrica Putra (2025) dengan judul “Implementasi Algoritma Random Forest untuk Prediksi Kelulusan Mahasiswa Berdasarkan Data Akademik”. Penelitian ini menggunakan data mahasiswa dari beberapa program studi di Universitas Putra Indonesia YPTK Padang. Variabel yang digunakan mencakup IPK, tingkat kehadiran, nilai mata kuliah inti, serta tren nilai per semester. Hasil pengujian menunjukkan bahwa algoritma Random Forest menghasilkan akurasi sebesar 87,5% dengan nilai ROC-AUC 0,912, menunjukkan kemampuan model yang sangat baik dalam membedakan mahasiswa yang lulus tepat waktu dan tidak. Faktor yang paling berpengaruh terhadap kelulusan adalah IPK dan kehadiran mahasiswa. Kelebihan penelitian ini adalah stabilitas dan akurasi tinggi, tetapi hasil model lebih sulit diinterpretasikan secara sederhana karena berbasis pada banyak pohon keputusan.

Dari keempat penelitian terdahulu tersebut dapat disimpulkan bahwa algoritma machine learning seperti Decision Tree, Logistic Regression, dan Random Forest telah terbukti mampu digunakan untuk memprediksi kelulusan mahasiswa dengan tingkat akurasi di atas 80%. Faktor yang paling berpengaruh terhadap kelulusan mahasiswa secara umum adalah IPK, IPS, dan kehadiran. Namun, sebagian besar penelitian tersebut masih berfokus pada satu algoritma tertentu dan belum membandingkan secara langsung kinerja antara model linear seperti Logistic Regression dengan model ensemble seperti Random Forest.

Selain itu, beberapa penelitian sebelumnya juga belum melibatkan variabel aktivitas akademik mahasiswa (seperti keikutsertaan dalam organisasi, seminar, atau kegiatan ilmiah), padahal faktor-faktor tersebut dapat memengaruhi motivasi, kedisiplinan, dan hasil belajar mahasiswa. Di sisi lain, sebagian penelitian masih menggunakan data terbatas atau bersifat simulatif, sehingga hasilnya belum sepenuhnya mencerminkan kondisi nyata di lingkungan perguruan tinggi.

Hal ini menjadi dasar dan celah penelitian (research gap) yang akan dikaji dalam penelitian ini, yaitu dengan membandingkan secara langsung algoritma Logistic Regression dan Random Forest dalam memprediksi kelulusan mahasiswa berdasarkan nilai akademik, tingkat kehadiran, dan aktivitas akademik. Melalui perbandingan ini, diharapkan dapat diketahui model mana yang memiliki kinerja paling optimal dalam konteks data pendidikan, serta memberikan rekomendasi yang dapat membantu pihak kampus dalam pengambilan keputusan akademik dan pembimbingan mahasiswa secara lebih dini.

2.3 Kerangka Pemikiran (Model Penelitian)

Penelitian ini berangkat dari asumsi bahwa nilai akademik (X1), tingkat kehadiran (X2), dan aktivitas akademik (X3) memengaruhi kelulusan mahasiswa (Y). Model prediksi akan dibuat menggunakan dua algoritma, yaitu Logistic Regression dan Random Forest, untuk melihat perbandingan kinerjanya.

Hubungan antar variabel dapat digambarkan sebagai berikut:
Nilai Akademik (X1)
|
Kehadiran (X2) --> Logistic Regression & Random Forest --> Prediksi Kelulusan Mahasiswa (Y) (Tepat Waktu / Tidak Tepat Waktu)
|
Aktivitas Akademik (X3)

Model ini menggambarkan bahwa ketiga variabel (X1, X2, X3) diolah menggunakan dua model machine learning berbeda (LR dan RF) untuk menghasilkan variabel prediksi kelulusan mahasiswa (Y).

2.4 Hipotesis Penelitian

1. H1: Algoritma Random Forest memiliki tingkat akurasi lebih tinggi dibandingkan Logistic Regression dalam memprediksi kelulusan mahasiswa.
2. H2: Variabel IPK dan tingkat kehadiran berpengaruh signifikan terhadap hasil prediksi kelulusan mahasiswa.
3. H3: Penambahan variabel aktivitas akademik mahasiswa dapat meningkatkan akurasi model prediksi kelulusan.
