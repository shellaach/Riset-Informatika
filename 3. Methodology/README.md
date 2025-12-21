# BAB III

## METODOLOGI PENELITIAN

### 3.1 Alur Penelitian

Penelitian ini dilakukan melalui beberapa tahapan, yaitu pengumpulan data, preprocessing data, pembuatan model CNN ResNet-18, serta pengujian dan evaluasi model.

#### 3.1.2 Pengumpulan Data

Data yang digunakan dalam penelitian ini berasal dari dataset ETL-5. Dataset ini diunduh dari sumber resmi dan dipilih khusus untuk karakter katakana. Setiap karakter memiliki jumlah data yang relatif seimbang, sehingga cocok digunakan untuk klasifikasi multikelas.

#### 3.1.3 Preprocessing Data

Tahap preprocessing meliputi pembagian data menjadi data latih dan data uji dengan perbandingan 70:30, konversi citra grayscale menjadi RGB, resize citra menjadi 224 × 224 piksel, normalisasi nilai piksel, serta augmentasi data pada data latih.

#### 3.1.4 Pembuatan Model ResNet-18

Model CNN yang digunakan dalam penelitian ini adalah ResNet-18. Lapisan keluaran dimodifikasi sesuai dengan jumlah kelas karakter katakana, yaitu 46 kelas, dengan fungsi aktivasi softmax. Proses pelatihan dilakukan menggunakan optimizer Adam dengan learning rate tertentu dan mekanisme early stopping untuk mencegah overfitting.

#### 3.1.5 Pengujian dan Evaluasi Model

Pengujian model dilakukan menggunakan data uji yang tidak digunakan selama proses pelatihan. Evaluasi performa model dilakukan menggunakan confusion matrix untuk menghitung nilai accuracy, precision, recall, dan F1-score.

