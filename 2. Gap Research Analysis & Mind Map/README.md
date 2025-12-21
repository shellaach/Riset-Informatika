# BAB II

## TINJAUAN PUSTAKA DAN KERANGKA PEMIKIRAN

### 2.1 Karakter Katakana

Katakana merupakan salah satu sistem penulisan dalam bahasa Jepang yang digunakan untuk menuliskan kata serapan dari bahasa asing, nama ilmiah, nama produk, dan penekanan kata tertentu. Katakana dasar terdiri dari 46 karakter utama, yang masing-masing memiliki pola guratan khas. Namun, banyak karakter katakana memiliki bentuk visual yang mirip sehingga sulit dibedakan, terutama pada tulisan tangan.


#### 2.2 Handwritten Character Recognition

Handwritten Character Recognition (HCR) merupakan bidang dalam pengolahan citra dan kecerdasan buatan yang bertujuan untuk mengenali dan mengklasifikasikan karakter tulisan tangan dari citra digital. Tantangan utama HCR adalah adanya variasi gaya tulisan, perbedaan ketebalan garis, serta kemiripan bentuk antar karakter. 

Pada aksara Jepang, khususnya katakana, banyak karakter memiliki bentuk visual yang hampir serupa sehingga mempersulit proses pengenalan. Oleh karena itu, diperlukan metode yang mampu mengekstraksi fitur secara efektif dan diskriminatif. Pendekatan deep learning berbasis Convolutional Neural Network (CNN) banyak digunakan dalam HCR karena kemampuannya dalam mengekstraksi fitur secara otomatis, sehingga menjadi dasar dalam penelitian ini.


#### 2.3 Convolutional Neural Network (CNN)

Convolutional Neural Network (CNN) adalah salah satu jenis jaringan saraf tiruan yang dirancang khusus untuk memproses data berbentuk citra. CNN terdiri dari beberapa lapisan utama, yaitu convolution layer, pooling layer, dan fully connected layer. CNN mampu mengekstraksi fitur secara otomatis dari citra tanpa memerlukan proses ekstraksi fitur manual.


#### 2.4 ResNet-18

ResNet-18 merupakan salah satu varian Residual Network yang terdiri dari 18 layer. Keunggulan utama ResNet terletak pada penggunaan residual connection atau skip connection yang memungkinkan aliran informasi langsung dari layer sebelumnya ke layer berikutnya. Mekanisme ini membantu mengatasi masalah vanishing gradient dan memungkinkan pelatihan jaringan yang lebih dalam dengan performa yang stabil.

#### 2.5 Dataset ETL-5

Dataset ETL-5 merupakan bagian dari ETL Character Database yang dikembangkan oleh AIST Jepang. Dataset ini berisi citra tulisan tangan karakter Jepang dalam format grayscale dengan ukuran 72 × 76 piksel. Dataset ETL-5 banyak digunakan dalam penelitian pengenalan karakter Jepang karena kualitas dan konsistensi datanya.

### 2.6 Penelitian Terdahulu

Beberapa penelitian terdahulu yang menjadi acuan dalam penelitian ini berasal dari jurnal-jurnal yang relevan dengan pengenalan karakter Jepang dan penerapan Convolutional Neural Network (CNN).
Penelitian yang dilakukan oleh Rusyn et al. (2005) menggunakan arsitektur Preact ResNet-18 untuk pengenalan karakter kanji tulisan tangan dengan jumlah kelas yang besar. Hasil penelitian menunjukkan bahwa penggunaan ResNet-18 mampu meningkatkan akurasi pengenalan secara signifikan dibandingkan metode konvensional, serta mampu mengatasi permasalahan degradasi performa pada jaringan yang lebih dalam.

Nugroho dan Harjoko (2021) mengembangkan sistem transliterasi karakter hiragana dan katakana tulisan tangan menggunakan pendekatan CNN-SVM. Penelitian ini menunjukkan bahwa CNN efektif sebagai ekstraktor fitur, namun penggunaan arsitektur yang relatif sederhana masih memiliki keterbatasan dalam membedakan karakter yang memiliki kemiripan bentuk.
Winardi dan Hartati (2022) melakukan penelitian pengenalan aksara katakana menggunakan CNN dengan arsitektur LeNet. Hasil penelitian menunjukkan bahwa metode CNN mampu mengenali karakter katakana dengan cukup baik, namun performa masih terbatas pada kemampuan ekstraksi fitur arsitektur CNN yang dangkal.

Fernandi et al. (2024) menerapkan CNN untuk mendeteksi huruf hiragana tulisan tangan menggunakan dataset standar karakter Jepang. Penelitian ini membuktikan bahwa CNN mampu menangkap pola guratan karakter secara efektif, sehingga mendukung penggunaan CNN yang lebih dalam seperti ResNet-18 untuk meningkatkan performa.

Penelitian oleh Solis et al. (2023) mengusulkan penggunaan ensemble CNN untuk pengenalan karakter Jepang tulisan tangan. Hasil penelitian menunjukkan peningkatan performa dibandingkan model tunggal, yang mengindikasikan bahwa kemampuan ekstraksi fitur CNN sangat berpengaruh terhadap akurasi pengenalan karakter.

Berdasarkan penelitian-penelitian tersebut, dapat disimpulkan bahwa CNN merupakan metode yang efektif untuk pengenalan karakter Jepang. Namun, penelitian yang secara khusus menerapkan arsitektur ResNet-18 pada pengenalan tulisan tangan karakter katakana masih relatif terbatas. Oleh karena itu, penelitian ini berfokus pada penerapan ResNet-18 untuk mengisi celah penelitian tersebut dan meningkatkan performa pengenalan karakter katakana
