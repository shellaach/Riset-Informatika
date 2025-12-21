# BAB I

## PENDAHULUAN

### 1.1 Latar Belakang

Sistem penulisan bahasa Jepang merupakan salah satu sistem tulisan yang kompleks karena terdiri dari tiga jenis karakter utama, yaitu hiragana, katakana, dan kanji. Katakana memiliki peran penting dalam bahasa Jepang modern karena digunakan untuk menuliskan kata serapan, istilah asing, nama produk, serta istilah ilmiah. Meskipun jumlah karakter katakana relatif lebih sedikit dibandingkan kanji, banyak karakter katakana memiliki kemiripan bentuk visual, seperti ク dengan ケ atau ソ dengan ン, sehingga menyulitkan proses pengenalan, khususnya pada tulisan tangan.

Permasalahan pengenalan tulisan tangan semakin kompleks karena adanya variasi gaya penulisan antar individu. Setiap penulis dapat memiliki perbedaan ketebalan garis, kemiringan tulisan, serta penyederhanaan bentuk karakter. Variasi ini menjadi tantangan utama dalam pengembangan sistem pengenalan karakter otomatis, karena sistem harus mampu mengenali pola karakter yang tidak selalu konsisten secara visual.

Penelitian terkait pengenalan karakter Jepang dengan pendekatan kecerdasan buatan telah banyak dilakukan, terutama untuk karakter hiragana dan kanji. Beberapa penelitian menunjukkan bahwa metode Convolutional Neural Network (CNN) mampu memberikan performa yang baik dalam pengenalan tulisan tangan. Namun, penelitian yang secara khusus membahas pengenalan tulisan tangan katakana masih relatif terbatas dan sebagian besar masih menggunakan arsitektur CNN sederhana seperti LeNet.
Dalam beberapa tahun terakhir, arsitektur CNN yang lebih dalam seperti Residual Network (ResNet) menunjukkan kinerja yang unggul dalam berbagai tugas pengenalan citra. ResNet memperkenalkan konsep residual connection yang memungkinkan pelatihan jaringan yang lebih dalam tanpa mengalami degradasi performa. ResNet-18 sebagai salah satu varian ResNet yang ringan dan efisien telah terbukti efektif dalam berbagai tugas pengenalan citra dan tulisan tangan. Oleh karena itu, penelitian ini mengusulkan penggunaan arsitektur ResNet-18 untuk pengenalan tulisan tangan karakter katakana guna memperoleh performa pengenalan yang lebih baik dan stabil.


### 1.2 Rumusan Masalah

1. Bagaimana penerapan arsitektur Convolutional Neural Network (CNN) ResNet-18 dalam melakukan klasifikasi aksara Jepang jenis katakana berbasis citra tulisan tangan?
2. Seberapa efektif model ResNet-18 dalam mengenali karakter katakana berdasarkan hasil evaluasi performa menggunakan metrik akurasi, presisi, recall, dan F1-score?
3. Bagaimana pengaruh pembagian data (data splitting) terhadap tingkat akurasi pengenalan aksara katakana menggunakan model ResNet-18?


### 1.3 Tujuan Penelitian

Tujuan dari penelitian ini adalah:

1. Mengimplementasikan arsitektur CNN ResNet-18 untuk klasifikasi aksara Jepang jenis katakana berbasis citra tulisan tangan.
2. Mengevaluasi dan menganalisis performa model ResNet-18 dalam mengenali karakter katakana menggunakan matrik evaluasi klasifikasi.
3. Menganalisis pengaruh pembagian data terhadap akurasi pengenalan aksara katakana pada model ResNet-18.


### 1.4 Manfaat Penelitian

1. Memberikan kontribusi akademik dalam pengembangan penelitian pengenalan tulisan tangan karakter katakana berbasis deep learning.
2. Menjadi referensi bagi penelitian selanjutnya yang berkaitan dengan pengenalan karakter bahasa Jepang.
3. Menjadi dasar pengembangan sistem pengenalan tulisan tangan bahasa Jepang yang lebih akurat dan efisien.


### 1.5 Batasan Masalah

Agar penelitian ini lebih terarah dan mudah dilakukan, penulis memberikan beberapa  batasan sebagai berikut: 

1. Penelitian ini hanya membahas pengenalan dan klasifikasi aksara Jepang jenis katakana, tidak mencakup hiragana, kanji, maupun kombinasi aksara Jepang lainnya.
2. Dataset yang digunakan dalam penelitian ini adalah ETL Character Database tipe ETL-5, dengan fokus pada karakter katakana dasar yang berjumlah 46 kelas.
3. Citra yang digunakan berupa citra tulisan tangan (handwritten) dalam format digital, bukan citra cetak atau citra hasil pemindaian dokumen kompleks.
4. Metode yang digunakan dalam penelitian ini dibatasi pada arsitektur Convolutional Neural Network (CNN) ResNet-18 sebagai model utama untuk klasifikasi karakter.
5. Proses preprocessing data dibatasi pada resize citra, konversi format (grayscale ke RGB), normalisasi, serta augmentasi data sederhana tanpa melakukan ekstraksi fitur manual.

