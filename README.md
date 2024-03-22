# Proyek Prediksi Harga Mobil dengan Analisis Data

## Domain Project

Dalam industri otomotif, perusahaan sering menghadapi tantangan dalam menetapkan harga mobil yang kompetitif dan mengoptimalkan keuntungan mereka. Masalah utama yang dihadapi adalah kesulitan dalam memahami faktor-faktor apa yang sebenarnya memengaruhi harga mobil dan bagaimana variabel-variabel tersebut dapat dimanfaatkan secara efektif untuk merespons perubahan pasar.

Pada proyek ini, masalah yang dihadapi adalah kurangnya pemahaman tentang variabel-variabel yang paling berpengaruh dalam menentukan harga mobil di pasar AS. Oleh karena itu, diperlukan sebuah model machine learning yang dapat memprediksi harga mobil berdasarkan fitur-fitur tertentu, sehingga membantu manajemen dalam mengambil keputusan yang lebih tepat dalam penetapan harga.

**Urgensi Proyek**
Dengan memahami faktor-faktor yang memengaruhi harga mobil, perusahaan dapat merespons perubahan pasar dengan lebih cepat dan tepat. Hal ini dapat meningkatkan daya saing perusahaan dalam industri otomotif, terutama dalam menghadapi pasar AS yang kompetitif.

**Kontribusi Machine Learning**
Dengan menggunakan teknik machine learning, dapat diidentifikasi pola dan hubungan antara variabel-variabel tertentu dengan harga mobil. Hasil prediksi dari model yang dikembangkan dapat menjadi panduan bagi manajemen dalam menetapkan harga yang kompetitif, merencanakan strategi pemasaran, dan mengoptimalkan keuntungan perusahaan.

## Business Understanding

Pada proyek ini, pemodelan harga mobil memiliki dampak yang signifikan terhadap kepentingan bisnis dan ekonomi perusahaan otomotif. Dengan pemahaman yang baik tentang faktor-faktor yang memengaruhi harga mobil di pasar AS, perusahaan dapat merencanakan strategi pemasaran, menetapkan harga yang kompetitif, dan mengoptimalkan keuntungan mereka.

**Dampak terhadap Kepentingan Bisnis dan Ekonomi**

- Meningkatkan Daya Saing: Dengan memahami faktor-faktor yang memengaruhi harga mobil, perusahaan dapat menyesuaikan strategi bisnis mereka untuk menjadi lebih responsif terhadap perubahan pasar. Ini akan membantu mereka mempertahankan atau meningkatkan pangsa pasar dan daya saing mereka.
- Optimasi Keuntungan: Dengan menggunakan model prediksi harga mobil, perusahaan dapat mengoptimalkan keuntungan mereka dengan menetapkan harga yang tepat sesuai dengan fitur-fitur mobil dan kondisi pasar saat ini.

**Contoh Penggunaan Hasil Prediksi dalam Pengambilan Keputusan Bisnis**

- Penetapan Harga yang Optimal: Manajemen dapat menggunakan hasil prediksi untuk menetapkan harga yang optimal untuk mobil baru atau model yang sudah ada. Misalnya, jika model prediksi menunjukkan bahwa mobil dengan fitur-fitur tertentu memiliki permintaan yang tinggi, perusahaan dapat menetapkan harga yang sedikit lebih tinggi untuk meningkatkan margin keuntungan.
 Perencanaan Portofolio Produk: Hasil prediksi juga dapat membantu perusahaan dalam merencanakan portofolio produk mereka. Mereka dapat memutuskan untuk fokus pada mobil dengan fitur-fitur tertentu yang diprediksi memiliki permintaan yang tinggi, atau memperkenalkan varian baru berdasarkan tren yang teridentifikasi.
- Strategi Pemasaran yang Tepat: Dengan pemahaman yang lebih baik tentang preferensi konsumen dan faktor-faktor yang memengaruhi harga, perusahaan dapat mengarahkan strategi pemasaran mereka dengan lebih efektif. Mereka dapat menyesuaikan pesan pemasaran mereka untuk menyoroti fitur-fitur yang dinilai tinggi oleh konsumen potensial.

**Kesesuaian Problem Statement, Goals, dan Solution**

1. Problem Statement

- Variabel-variabel apa yang signifikan dalam memprediksi harga sebuah mobil?
- Seberapa baik variabel-variabel tersebut menjelaskan harga sebuah mobil?

2. Goals 

- Menemukan variabel-variabel yang paling berpengaruh dalam menentukan harga mobil di pasar Amerika Serikat 
- Mengembangkan model machine learning yang dapat memprediksi harga mobil dengan variabel-variabel yang akan digunakan untuk mendapatkan akurasi yang tinggi.

3. Solution Statement

- Analisis Fitur: Pertama, akan dilakukan analisis fitur untuk memahami hubungan antara fitur-fitur yang ada dengan harga mobil. Ini akan melibatkan visualisasi data, perhitungan korelasi, dan pemahaman domain tentang industri otomotif.

- Seleksi Fitur: Berdasarkan analisis fitur, fitur-fitur yang memiliki korelasi yang kuat atau memiliki pengaruh yang signifikan terhadap harga mobil akan dipilih. Ini akan membantu dalam mengurangi dimensi fitur dan meningkatkan fokus pada variabel-variabel yang paling penting.

- Pemodelan: Setelah seleksi fitur dilakukan, akan dilakukan pemodelan menggunakan algoritma machine learning sequential. Pada tahap ini, variabel-variabel yang dipilih akan digunakan sebagai fitur masukan untuk memprediksi harga mobil. Model Sequential memiliki kemampuan representasi yang fleksibel dan mampu melakukan feature learning secara otomatis, sehingga dapat menangani data yang kompleks dengan baik, berbeda dengan model regresi linear dan regresi polinomial yang memerlukan penentuan fitur secara manual.

- Evaluasi: Setiap model akan dievaluasi menggunakan metrik evaluasi yang sesuai seperti R-squared, Mean Squared Error, dan lainnya. Hal ini akan membantu dalam menilai seberapa baik model mampu menjelaskan variasi dalam data harga mobil.

## Data Understanding

Dataset yang digunakan dapat diakses menggunakan Kaggle [disini](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction)
Informasi dari dataset dapat dilihat pada tabel 1: 

Tabel 1. Rangkuman informasi Dataset

| Jenis                  | Keterangan                                                                                                        |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Sumber                 | [Kaggle Dataset: Car Price Prediction Multiple Linear Regression](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction)  |
| Lisensi                | Unknown                                                                                                           |
| Kategori               | Sosial                                                                                                            |
| Jenis & Ukuran berkas  | CSV (26.72KB)

**Download Dataset dari Kaggle**
Pada proyek ini _dataset_ di download melalui Kaggle [disini](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction), untuk mendownload _dataset_, penulis mengunduh secara manual dan mengupload dataset tersebut kedalam folder content di google colab.

**Membaca dataset ke dalam Dataframe**
Pada bagian ini akan digunakan fungsi read_csv() untuk membaca berkas csv dan menyimpannya di dalam variabel df dan bisa dilihat pada tabel 2.

Tabel 2. Dataframe

| car_ID | symboling | CarName               | fueltype | aspiration | doornumber | carbody   | drivewheel | enginelocation | wheelbase |
|--------|-----------|-----------------------|----------|------------|------------|-----------|------------|----------------|-----------|
| 1      | 3         | alfa-romero giulia    | gas      | std        | two        | convertible | rwd        | front          | 88.6      |
| 2      | 3         | alfa-romero stelvio   | gas      | std        | two        | convertible | rwd        | front          | 88.6      |
| 3      | 1         | alfa-romero Quadrifoglio | gas   | std        | two        | hatchback  | rwd        | front          | 94.5      |
| 4      | 2         | audi 100 ls           | gas      | std        | four       | sedan      | fwd        | front          | 99.8      |
| 5      | 2         | audi 100ls            | gas      | std        | four       | sedan      | 4wd        | front          | 99.4      |

**Cek Missing Value**
Pada bagian ini digunakan fungsi sna().sum() untuk _DataFrame_. Saat dicek tidak ditemukan adanya _missing value_ pada _DataFrame_

**Memperbaiki Beberapa Value yang Salah Eja**
Variabel yang salah eja bisa dilihat pada tabel 3.

Tabel 3. List Value dari Variabel CarName yang Salah Eja
| Variabel salah eja | Koreksi   |
|-------------------|-----------|
| maxda             | mazda     |
| nissan            | Nissan    |
| porcshce          | porsche   |
| toyouta           | toyota    |
| vokswagen         | volkswagen|
| vw                | volkswagen|

**Penjelasan Setiap Variabel**
Untuk penjelasan setiap tabel bisa dilihat pada Tabel 4

Tabel 4. Penjelasan Singkat Tentang Variabel pada Dataset
| Nama Variabel        | Penjelasan Singkat                                       |
|----------------------|----------------------------------------------------------|
| car_ID               | ID unik untuk setiap mobil                               |
| symboling            | Penilaian risiko asuransi                               |
| CarName              | Nama merek dan model mobil                               |
| fueltype             | Jenis bahan bakar (misalnya gas atau diesel)             |
| aspiration           | Jenis sistem pengkabutan (misalnya standar atau turbo)   |
| doornumber           | Jumlah pintu mobil                                       |
| carbody              | Tipe bodi mobil (misalnya sedan, hatchback, convertible) |
| drivewheel           | Roda penggerak mobil (misalnya fwd, rwd)                 |
| enginelocation       | Lokasi mesin (depan atau belakang)                        |
| wheelbase            | Jarak sumbu roda depan-belakang                           |
| carlength            | Panjang mobil                                            |
| carwidth             | Lebar mobil                                              |
| carheight            | Tinggi mobil                                             |
| curbweight           | Berat kosong mobil                                       |
| enginetype           | Jenis mesin (misalnya ohc, ohcv)                         |
| cylindernumber       | Jumlah silinder mesin                                    |
| enginesize           | Ukuran mesin (kapasitas silinder)                        |
| fuelsystem           | Sistem bahan bakar mobil (misalnya mpfi, 2bbl)           |
| boreratio            | Rasio diameter silinder dengan langkah                    |
| stroke               | Langkah piston                                           |
| compressionratio     | Rasio kompresi mesin                                     |
| horsepower           | Tenaga mesin dalam horsepower                            |
| peakrpm              | Putaran maksimum mesin per menit                         |
| citympg              | Konsumsi bahan bakar dalam kota (miles per gallon)       |
| highwaympg           | Konsumsi bahan bakar di jalan raya (miles per gallon)   |
| price                | Harga mobil                                              |

**Deskripsi Variabel yang akan Dipakai:**
- Variabel Independent(Variabel yang akan dipakai): carlength, carwidth, curbweight, enginesize, horsepower
- Variabel Dependant(Variabel Target): price

Dari deskripsi dataframe yang diberikan, dapat dilihat statistik deskriptif untuk setiap variabel. Dari sini, dapat dipilih variabel yang paling signifikan untuk dimasukkan ke dalam model prediksi harga mobil. Alasan dipilihnya variabel-variabel tersebut dapat dilihat pada gambar 1

![Korelasi Antar Kolom](https://raw.githubusercontent.com/4q1l/prediksi-harga-mobil/main/img/1.png)
Gambar 1. Menunjukkan Korelasi Antar Variabel

Pada gambar tersebut bisa dilihat bahwasanya nilai korelasi variabel independent atas variabel dependent yang diatas 0.6 akan dipakai untuk menguji apakah variabel-variabel tersebut adalah variabel yang berpengaruh besar terhadap variabel harga.

## Data Preparation

**Data Preparation Steps:**
1. Plot Outlier dari kelima variabel tersebut dengan fungsi detect_and_handle_outliers, bisa dilihat pada gambar 2.

![Plot Outlier](https://raw.githubusercontent.com/4q1l/prediksi-harga-mobil/main/img/4.png)
Gambar 2. Box Plot Outlier dari 5 variabel Independent

Disini metode yang digunakan untuk membersihkan outlier adalah IQR. Interquartile Range (IQR) adalah metode yang umum digunakan untuk mendeteksi dan menangani outlier dalam data. Metode ini didasarkan pada perhitungan kuartil data, yaitu kuartil pertama (Q1) dan kuartil ketiga (Q3), yang digunakan untuk menentukan batas bawah dan batas atas di mana data dianggap sebagai outlier.
 
2. Penskalaan fitur menggunakan StandardScaler dari library sklearn. Penggunaan StandardScaler dari modul sklearn dalam kode tersebut bertujuan untuk melakukan penskalaan fitur. Dengan menggunakan StandardScaler, dapat meningkatkan kinerja dan stabilitas model machine learning, serta membuat interpretasi hasil model menjadi lebih mudah dan konsisten.
  
3. Pembagian dataset menjadi set pelatihan dan pengujian dengan fungsi import_test_train dari modul sklearn.

## Modelling
**Langkah Modelling**
1. Inisialisasi Model Sequential:

- Langkah pertama adalah menginisialisasi model Sequential dari TensorFlow/Keras. Model Sequential adalah tumpukan linear dari layer-layer neural network, yang dijalankan secara berurutan.
- Alasan penggunaan Sequential model adalah karena ini adalah jenis model yang sederhana dan cocok untuk penggunaan dalam jaringan saraf tiruan feedforward yang memiliki arsitektur yang sekuensial. Selain itu, model Sequential memiliki kemampuan representasi yang fleksibel dan mampu melakukan feature learning secara otomatis, sehingga dapat menangani data yang kompleks dengan baik, berbeda dengan model regresi linear dan regresi polinomial yang memerlukan penentuan fitur secara manual.

2. Menambahkan Layer-layer Dense:

- Layer-layer Dense ditambahkan ke dalam model menggunakan method add().
- Layer Dense adalah layer yang terkoneksi penuh, di mana setiap neuron di layer tersebut terhubung dengan setiap neuron di layer sebelumnya dan setelahnya.
- Kemudian ditambahkan dua layer Dense dengan aktivasi ReLU (Rectified Linear Unit). Aktivasi ReLU umumnya digunakan karena kecepatan komputasinya yang cepat dan kemampuannya untuk mengatasi masalah vanish gradient.
- Layer pertama membutuhkan input_dim yang sesuai dengan jumlah fitur pada data latih.
- Layer terakhir memiliki satu neuron karena ini adalah model regresi, dengan aktivasi linear maka output dari model regresi yang dihasilkan adalah prediksi kontinu.

3. Menampilkan Ringkasan Arsitektur Model:
- Fungsi summary() digunakan untuk menampilkan ringkasan arsitektur model yang telah dibuat.
- Ini termasuk jumlah parameter yang akan dioptimalkan selama proses pelatihan, serta ukuran output dari setiap layer. Tampilan dari ringkasan arsitektur model bisa dilihat pada gambar 3.

![Arsitektur Model](https://raw.githubusercontent.com/4q1l/prediksi-harga-mobil/main/img/5.JPG)
Gambar 3. Ringkasan Arsitektur Model Sequential

4. Kompilasi Model:
- Model kemudian dikompilasi menggunakan optimizer Adam dan fungsi loss mean squared error (MSE).
- Adam merupakan algoritma optimizer yang efisien untuk melatih model jaringan saraf tiruan dan seringkali memberikan hasil yang baik.
- Mean squared error (MSE) dipilih sebagai fungsi loss karena ini adalah masalah regresi yang mencoba untuk memprediksi nilai numerik.

5. Pelatihan Model:
- Model dilatih dengan data latih menggunakan method fit().
- Batch size sebesar 10 dipilih, yang berarti data akan dibagi menjadi batch-batch dengan masing-masing batch berukuran 10 sampel. Ini membantu dalam proses optimasi yang lebih efisien.
- Epochs sebesar 100 dipilih, yang berarti model akan melalui seluruh dataset latih sebanyak 100 kali.
- Validation split sebesar 0.2 dipilih, yang berarti 20% data latih akan digunakan sebagai data validasi untuk mengukur kinerja model selama pelatihan.
- Proses ini akan menghasilkan objek history yang berisi riwayat pelatihan model, termasuk metrik-metrik seperti loss dan akurasi pada setiap epoch.

## Evaluasi Model

1. Memprediksi Harga Mobil: Model yang telah dilatih digunakan untuk memprediksi harga mobil menggunakan data uji (X_test).

2. Pada epoch ke-100, dengan menggunakan MSE nilai loss yang diperoleh adalah 0.1077 untuk data latih dan 0.1479 untuk data validasi.

3. Menghitung Koefisien Determinasi (R-squared): Setelah memprediksi harga mobil menggunakan model, langkah selanjutnya adalah mengukur kinerja model dengan metrik evaluasi yang sesuai. Dalam hal ini, koefisien determinasi atau R-squared digunakan sebagai metrik evaluasi.

- **Alasan Penggunaan R-squared:** R-squared adalah salah satu metrik evaluasi yang umum digunakan untuk masalah regresi. Ini memberikan informasi tentang seberapa baik variabel independen menjelaskan variasi dalam variabel dependen. Semakin tinggi nilai R-squared, semakin baik model dapat menjelaskan variasi dalam data. Oleh karena itu, R-squared digunakan untuk mengevaluasi seberapa baik model cocok dengan data aktual.

R-squared yang didapat memiliki nilai sebesar 0.8226028764928757. Ini mengindikasikan bahwa model mampu menjelaskan sekitar 82.26% dari variasi atau keragaman dalam data harga mobil yang diamati. Dengan kata lain, sekitar 82.26% dari perbedaan dalam harga mobil yang ada dalam dataset dapat dijelaskan oleh model yang telah dikembangkan. Semakin tinggi nilai R-squared, semakin baik model dalam menjelaskan variasi dalam data. Dengan demikian, nilai R-squared yang tinggi menunjukkan bahwa model memiliki kemampuan yang baik dalam memprediksi harga mobil berdasarkan fitur-fitur yang dipilih.

- **Rumus R-squared:** R-squared dihitung sebagai koefisien determinasi yang merupakan proporsi variabilitas dalam variabel dependen yang dapat dijelaskan oleh variabel independen dalam model. Rumus matematisnya bisa dilihat pada gambar 4.


![Rumus R-Squared](https://raw.githubusercontent.com/4q1l/prediksi-harga-mobil/main/img/7.png)
Gambar 4. Rumus R-Squared

R-squared = 1 - (SS_res / SS_tot)

di mana:
SS_res adalah jumlah kuadrat residual (sum of squared residuals), yaitu jumlah kuadrat perbedaan antara nilai prediksi dan nilai aktual.
SS_tot adalah jumlah kuadrat total (total sum of squares), yaitu jumlah kuadrat perbedaan antara setiap nilai aktual dan nilai rata-rata dari semua nilai aktual.

R-squared memiliki rentang nilai dari 0 hingga 1, di mana:
R-squared = 0 menunjukkan bahwa model tidak menjelaskan variasi sama sekali.
R-squared = 1 menunjukkan bahwa model menjelaskan seluruh variasi dalam data dengan sempurna.

- **Plot Loss Selama Pelatihan:** Grafik loss selama proses pelatihan digambarkan untuk memantau konvergensi model. Ini membantu dalam mengevaluasi apakah model telah mengalami overfitting atau underfitting, serta seberapa baik model beradaptasi dengan data pelatihan dan validasi. Plot Loss dan Val_Loss dapat dilihat pada gambar 5.

![Plot Loss Training](https://raw.githubusercontent.com/4q1l/prediksi-harga-mobil/main/img/2.png)
Gambar 5. Plot Loss dan Val_Loss Dalam 100 Epoch

3. Plot Nilai Aktual dan Nilai yang Diprediksi: Plot nilai aktual (y_test) dan nilai yang diprediksi (y_pred) digambarkan untuk memvisualisasikan seberapa baik model dalam memprediksi harga mobil. Ini memberikan pemahaman visual tentang seberapa dekat prediksi model dengan nilai aktual, serta apakah ada pola atau tren tertentu dalam prediksi yang perlu diperhatikan.
Plot Loss Selama Pelatihan: Grafik loss selama proses pelatihan digambarkan untuk memantau konvergensi model. Ini membantu dalam mengevaluasi apakah model telah mengalami overfitting atau underfitting, serta seberapa baik model beradaptasi dengan data pelatihan dan validasi.

4. Plot Nilai Aktual dan Nilai yang Diprediksi: Plot nilai aktual (y_test) dan nilai yang diprediksi (y_pred) digambarkan untuk memvisualisasikan seberapa baik model dalam memprediksi harga mobil. Ini memberikan pemahaman visual tentang seberapa dekat prediksi model dengan nilai aktual, serta apakah ada pola atau tren tertentu dalam prediksi yang perlu diperhatikan.

## Kesimpulan Prediksi
- Model yang telah dilatih memiliki kinerja yang cukup baik dalam memprediksi harga mobil berdasarkan fitur-fitur yang dipilih.
- Meskipun demikian, masih ada sekitar beberapa variasi dalam data yang tidak dapat dijelaskan oleh model.
- Terdapat beberapa faktor lain di luar fitur yang digunakan dalam model yang mungkin juga mempengaruhi harga mobil seperti variabel lain yang tidak dipakai, dan dapat menjadi fokus penelitian lebih lanjut untuk meningkatkan kinerja model.

## **Kesimpulan Umum**
1. Interpretasi Koefisien Determinasi (R-squared):
- Nilai R-squared berkisar antara 0 hingga 1.
Semakin mendekati 1, semakin baik model dalam menjelaskan variasi dalam data.
- Nilai 0.8226 menunjukkan bahwa model dapat menjelaskan sekitar 82.26% variasi dalam data harga mobil.

2. Evaluasi Prediksi Model:
- Dengan menggunakan metrik R-squared, dapat dilihat seberapa baik model cocok dengan data aktual.
- Nilai R-squared yang tinggi menunjukkan bahwa model memiliki kemampuan yang baik dalam memprediksi harga mobil.

3. Kesimpulan Umum:
- Model yang telah dilatih memiliki kinerja yang cukup baik dalam memprediksi harga mobil berdasarkan fitur-fitur yang dipilih.
- Meskipun demikian, masih ada sekitar 17.74% variasi dalam data yang tidak dapat dijelaskan oleh model.
- Terdapat beberapa faktor lain di luar fitur yang digunakan dalam model seperti variabel lain yang tidak dimasukkan ke dalam modelling yang mungkin juga mempengaruhi harga mobil, dan dapat menjadi fokus penelitian lebih lanjut untuk meningkatkan kinerja model.

Dengan demikian, meskipun model dapat memberikan prediksi yang relatif baik, masih ada ruang untuk peningkatan dalam model untuk menjelaskan variasi yang lebih besar dalam data harga mobil.

## Referensi

- Dokumentasi scikit-learn: [https://scikit-learn.org/stable/documentation.html](https://scikit-learn.org/stable/documentation.html)
- Dokumentasi TensorFlow: [https://www.tensorflow.org/api_docs/python/tf](https://www.tensorflow.org/api_docs/python/tf)
- Dokementasi Dataset: [https://www.kaggle.com/datasets/hellbuoy/car-price-prediction?resource](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction?resource)
