# Implementation of Supervised Learning on Regression Task
Implementasi supervised Learning pada tugas regresi.

# About The Project
Implementasi supervised Learning pada tugas regresi melibatkan pelatihan model untuk memprediksi nilai numerik kontinu berdasarkan data pelatihan yang diberi label, di mana setiap input dikaitkan dengan output target. Tujuannya adalah untuk mempelajari hubungan mendasar antara input dan output agar dapat membuat prediksi yang akurat pada data baru yang belum pernah dilihat sebelumnya.

# Dataset 
Data yang digunakan adalah Dataset ‘Range Queries Aggregates’

## Tentang Dataset
### Konteks
Data set “Range Queries Aggregates” adalah kumpulan data yang mencakup tiga set beban kerja kueri rentang/radius dari distribusi Gaussian di atas dataset nyata. Setiap kueri dikaitkan dengan nilai skalar agregat (hitungan/jumlah/rata-rata).

### Konten
Dataset ‘Range Queries Aggregates’ berisi catatan dengan format: {`X-coordinate`,`Y-coordinate`, `X-range`, `Y-range`, `Count`, `SUM`, `AVG`}.

### Jenis Kueri
Dataset ini berisi tiga jenis kueri:

1. Kueri Radius: Mereka mendefinisikan disk di atas ruang 2D dengan pusat `(X,Y)` dan radius `R` untuk menyelidiki jumlah insiden kejahatan, total penangkapan, dan rata-rata beat dari area disk (area spasial) yang didefinisikan oleh setiap kueri.

2. Kueri Radius Count: Mereka mendefinisikan disk di atas ruang 2D dengan pusat `(X,Y)` dan radius `R` dan jumlah insiden kejahatan Count dari area disk (area spasial) yang didefinisikan oleh setiap kueri.

3. Kueri Rentang Agregat: Mereka mendefinisikan persegi panjang di atas ruang 2D dengan koordinat/poin: `X +/- X-range` dan `Y +/- Y-range`. `Count`, `SUM`, dan `AVG` adalah jumlah insiden, total penangkapan, dan rata-rata beat dari area persegi panjang (area spasial) yang didefinisikan oleh setiap kueri.


### Atribut:

`ID` = nomor seri kueri (opsional)

`X-coordinate` = koordinat spasial x (float)

`Y-coordinate` = koordinat spasial y (float)

`X-range` = rentang x spasial untuk kueri rentang (float)

`Y-range` = rentang y spasial untuk kueri rentang (float)

`Count` = jumlah insiden kejahatan di lingkaran 2D (kueri radius) atau persegi panjang (kueri rentang)

`SUM` = total penangkapan di lingkaran 2D (kueri radius) atau persegi panjang (kueri rentang)

`AVG` = rata-rata Beat di lingkaran 2D (kueri radius) atau persegi panjang (kueri rentang)

# Metode
Metode yang digunakan adalah Metode ANN

## Berikut adalah ringkasan metode yang digunakan :

### Pemilihan Fitur
Fitur independen yang dipilih adalah `X-coordinate`, `Y-coordinate`, `X-range`, `Y-range`, `Count`, dan `SUM`, sementara fitur dependen adalah `AVG`.

### Pembagian Data 
Data dibagi menjadi set pelatihan dan pengujian dengan proporsi 80:20.

### Penyekalaan Fitur 
Fitur disekala menggunakan StandardScaler sehingga mereka memiliki rata-rata 0 dan standar deviasi 1. Ini penting untuk beberapa algoritma pembelajaran mesin.

### Pembangunan Model
Didefinisikan tiga model Artificial Neural Network (ANN) dengan arsitektur yang berbeda. Model pertama memiliki satu lapisan tersembunyi dengan dropout, model kedua memiliki dua lapisan tersembunyi dengan dropout, dan model ketiga memiliki tiga lapisan tersembunyi dengan dropout untuk mencegah overfitting.

### Pelatihan Model 
Setiap model dilatih selama 100 epoch dengan ukuran batch 3125. Data pengujian juga digunakan sebagai data validasi selama pelatihan.

### Evaluasi Model 
Setiap model dievaluasi dengan menghitung `Mean Squared Error (MSE)`, `Root Mean Squared Error (RMSE)`, dan `R-squared (R^2)` pada data pengujian.

### Prediksi 
Setiap model digunakan untuk membuat prediksi pada data pengujian, dan kemudian prediksi tersebut dipetakan terhadap nilai sebenarnya.

### Konversi R^2 ke Persentase 
Nilai `R^2` untuk setiap model dikonversi menjadi persentase untuk interpretasi yang lebih mudah.

### Plot Residual 
Plot residual dibuat untuk setiap model. Residual adalah perbedaan antara nilai sebenarnya dan nilai yang diprediksi oleh model. Plot ini membantu dalam memahami sejauh mana kesalahan tersebar dan apakah ada pola tertentu dalam kesalahan tersebut.

# Hasil dan Analisis
Berdasarkan hasil evaluasi model, ketiga model Artificial Neural Network (ANN) yang dibangun memiliki kinerja yang sebanding. 

## Hasil metrik evaluasi utama
### Model 1:
    Mean Squared Error (MSE): 0.6936
    Root Mean Squared Error (RMSE): 0.8328
    R-squared (RS): 0.3064

### Model 2:
    Mean Squared Error (MSE): 0.7024
    Root Mean Squared Error (RMSE): 0.8381
    R-squared (RS): 0.2976

#### Model 3:
    Mean Squared Error (MSE): 0.6744
    Root Mean Squared Error (RMSE): 0.8212
    R-squared (RS): 0.3256

## Analisis 

### Analisis Model

#### Mean Squared Error (MSE)
Model 3 memiliki MSE terendah, menunjukkan bahwa model tersebut memiliki tingkat error yang lebih rendah dalam memprediksi target dibandingkan dengan Model 1 dan Model 2.

#### Root Mean Squared Error (RMSE)
Model 3 juga memiliki RMSE terendah, menunjukkan bahwa model tersebut memiliki tingkat kesalahan prediksi yang lebih rendah.

#### R-squared (RS)
R-squared mengukur sejauh mana variasi dalam data target dapat dijelaskan oleh model. Model 3 memiliki nilai RS tertinggi, menunjukkan kemampuannya untuk menjelaskan variasi yang lebih besar dalam data target.
    
### Analisis Persentase

#### Mean Squared Error (MSE)
Model 3 memiliki MSE terendah, menunjukkan bahwa model tersebut memiliki tingkat error yang lebih rendah dalam memprediksi target dibandingkan dengan Model 1 dan Model 2.

#### Root Mean Squared Error (RMSE)
Model 3 juga memiliki RMSE terendah, menunjukkan bahwa model tersebut memiliki tingkat kesalahan prediksi yang lebih rendah.

#### R-squared (RS)
R-squared mengukur sejauh mana variasi dalam data target dapat dijelaskan oleh model. Model 3 memiliki nilai RS tertinggi, menunjukkan kemampuannya untuk menjelaskan variasi yang lebih besar dalam data target.

# Kesimpulan
Ketiga model ANN yang dibangun menunjukkan kinerja yang sebanding dalam memprediksi target. Namun, Model 3 menonjol dengan MSE dan RMSE terendah, serta R-squared tertinggi, menunjukkan kemampuannya untuk memberikan prediksi dengan tingkat akurasi yang lebih baik. Hal ini mengindikasikan bahwa Model 3 lebih efisien dalam menangkap hubungan antara variabel input dan output dibandingkan dengan Model 1 dan Model 2.

Analisis metrik utama memperkuat keunggulan Model 3, dengan nilai MSE dan RMSE yang lebih rendah, menunjukkan bahwa hasil prediksinya lebih dekat dengan nilai sebenarnya. Selain itu, nilai R-squared yang lebih tinggi menunjukkan bahwa Model 3 mampu menjelaskan variasi yang lebih besar dalam data target. Analisis persentase juga mengonfirmasi bahwa Model 3 memiliki tingkat kesalahan yang lebih rendah dan kemampuan penjelasan yang lebih baik dibandingkan model lainnya, menjadikannya pilihan terbaik di antara ketiga model yang diuji.
