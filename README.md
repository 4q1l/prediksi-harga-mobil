# Proyek Prediksi Harga Mobil dengan Analisis Data

## Domain Project

Dalam industri otomotif, perusahaan sering menghadapi tantangan dalam menetapkan harga mobil yang kompetitif dan mengoptimalkan keuntungan mereka. Masalah utama yang dihadapi adalah kesulitan dalam memahami faktor-faktor apa yang sebenarnya memengaruhi harga mobil dan bagaimana variabel-variabel tersebut dapat dimanfaatkan secara efektif untuk merespons perubahan pasar.

Pada proyek ini, masalah yang dihadapi adalah kurangnya pemahaman tentang variabel-variabel yang paling berpengaruh dalam menentukan harga mobil di pasar AS. Oleh karena itu, diperlukan sebuah model machine learning yang dapat memprediksi harga mobil berdasarkan fitur-fitur tertentu, sehingga membantu manajemen dalam mengambil keputusan yang lebih tepat dalam penetapan harga.

**Urgensi Proyek**
Dengan memahami faktor-faktor yang memengaruhi harga mobil, perusahaan dapat merespons perubahan pasar dengan lebih cepat dan tepat. Hal ini dapat meningkatkan daya saing perusahaan dalam industri otomotif, terutama dalam menghadapi pasar AS yang kompetitif.

**Kontribusi Machine Learning**
Dengan menggunakan teknik machine learning, kita dapat mengidentifikasi pola dan hubungan antara variabel-variabel tertentu dengan harga mobil. Hasil prediksi dari model yang dikembangkan dapat menjadi panduan bagi manajemen dalam menetapkan harga yang kompetitif, merencanakan strategi pemasaran, dan mengoptimalkan keuntungan perusahaan.

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

- Pemodelan: Setelah seleksi fitur dilakukan, akan dilakukan pemodelan menggunakan berbagai algoritma machine learning seperti regresi linear, regresi polinomial, dan model ensemble. Pada tahap ini, variabel-variabel yang dipilih akan digunakan sebagai fitur masukan untuk memprediksi harga mobil.

- Evaluasi: Setiap model akan dievaluasi menggunakan metrik evaluasi yang sesuai seperti R-squared, Mean Squared Error, dan lainnya. Hal ini akan membantu dalam menilai seberapa baik model mampu menjelaskan variasi dalam data harga mobil.

## Data Understanding

Dataset yang digunakan dapat diakses menggunakan Kaggle [disini](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction)
Informasi dari dataset dapat dirangkum sebagai berikut: 

Tabel 1. Rangkuman informasi Dataset

| Jenis                  | Keterangan                                                                                                        |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Sumber                 | [Kaggle Dataset: Car Price Prediction Multiple Linear Regression](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction)  |
| Lisensi                | Unknown                                                                                                           |
| Kategori               | Sosial                                                                                                            |
| Jenis & Ukuran berkas  | CSV (26.72KB)

**Data Pra-Preparation Steps**
Langkah-langkah pra-pemrosesan data
1. Mendownload _dataset_ dari kaggle
2. Membaca _dataset_ yang telah didownload ke _DataFrame menggunakan _pandas_
3. Menampilkan informasi dari _dataset_
4. Mengecek dan mengani missing value di _dataset_ (jika ditemukan).
5. Mengecek _sample text_ yang ada di _DataFrame_

**Download Dataset dari Kaggle**
Pada proyek ini _dataset_ di download melalui Kaggle [disini](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction), untuk mendownload _dataset_, penulis mengunduh secara manual dan mengupload dataset tersebut kedalam folder content di google colab.

**Membaca dataset ke dalam Dataframe**
Pada bagian ini akan digunakan fungsi `pandas.read_csv()` untuk membaca berkas csv dan menyimpannya di dalam variabel `df` dan bisa dilihat pada tabel 3

| car_ID | symboling | CarName               | fueltype | aspiration | doornumber | carbody   | drivewheel | enginelocation | wheelbase |
|--------|-----------|-----------------------|----------|------------|------------|-----------|------------|----------------|-----------|
| 1      | 3         | alfa-romero giulia    | gas      | std        | two        | convertible | rwd        | front          | 88.6      |
| 2      | 3         | alfa-romero stelvio   | gas      | std        | two        | convertible | rwd        | front          | 88.6      |
| 3      | 1         | alfa-romero Quadrifoglio | gas   | std        | two        | hatchback  | rwd        | front          | 94.5      |
| 4      | 2         | audi 100 ls           | gas      | std        | four       | sedan      | fwd        | front          | 99.8      |
| 5      | 2         | audi 100ls            | gas      | std        | four       | sedan      | 4wd        | front          | 99.4      |

**Cek Missing Value**
Pada bagian ini digunakan fungsi `isna().sum()` untuk _DataFrame_. Saat dicek tidak ditemukan adanya _missing value_ pada _DataFrame_

**Memperbaiki Beberapa Value yang Salah Eja**
Variabel yang salah eja adalah sebagai berikut 
| Variabel salah eja | Koreksi   |
|-------------------|-----------|
| maxda             | mazda     |
| nissan            | Nissan    |
| porcshce          | porsche   |
| toyouta           | toyota    |
| vokswagen         | volkswagen|
| vw                | volkswagen|

**Deskripsi Variabel yang akan Dipakai:**
- Variabel Independent(Variabel yang akan dipakai): carlength,carwidth,curbweight,enginesize, horsepower
- Variabel Dependant(Variabel Target): price

Dari deskripsi dataframe yang diberikan, kita dapat melihat statistik deskriptif untuk setiap variabel. Dari sini, kita dapat memilih variabel yang paling signifikan untuk dimasukkan ke dalam model prediksi harga mobil. Alasan dipilihnya variabel-variabel tersebut dapat dilihat pada gambar dibawah

![Korelasi Antar Kolom](https://raw.githubusercontent.com/4q1l/prediksi-harga-mobil/main/img/1.png)

Pada gambar tersebut bisa dilihat bahwasanya nilai korelasi variabel independent atas variabel dependent yang diatas 0.6 akan dipakai untuk menguji apakah variabel-variabel tersebut adalah variabel yang berpengaruh besar terhadap variabel harga.

## Data Preparation

**Data Preparation Steps:**
1. Plot Outlier dari kelima variabel tersebut dengan fungsi `detect_and_handle_outliers`, bisa dilihat pada gambar berikut


 
2. Penskalaan fitur menggunakan `StandardScaler` dari library sklearn.
3. Pembagian dataset menjadi set pelatihan dan pengujian dengan fungsi `import_test_train` library sklearn.

## Pelatihan Model

- Model dilatih menggunakan jaringan saraf tiruan (neural network) dengan menggunakan variabel-variabel yang dipilih. Hal ini dipilih karena neural network mudah dipakai dan bisa dicostum dengan bebas.
- Di sini menggunakan metrik koefisien determinasi (R-squared) untuk mengevaluasi seberapa baik kecocokan model tersebut dengan data.

Model Machine Learning:
Membangun model neural network dengan TensorFlow.

Tahapan Pemodelan:
- Menentukan arsitektur model.
- Mengompilasi model dengan optimizer Adam dan loss function Mean Squared Error (MSE).
- Melatih model dengan data pelatihan.

```python
# Arsitektur model
model = Sequential()
model.add(Dense(10, activation='relu', input_dim=X_train.shape[1]))
model.add(Dense(10, activation='relu'))
model.add(Dense(1, activation='linear'))

# Mengompilasi model
model.compile(optimizer="Adam",loss='mean_squared_error')

# Melatih model
history = model.fit(X_train,y_train,batch_size=10,epochs=100,verbose=1,validation_split=0.2)
```

## Evaluasi Model

Model dievaluasi menggunakan R-squared untuk memeriksa seberapa baik model tersebut memprediksi harga mobil. Dari nilai R-squared sebesar 0.6525, kami menyimpulkan bahwa model kami mampu menjelaskan sekitar 65.25% variasi dalam data harga mobil.
```
y_pred = model.predict(X_test)
from sklearn.metrics import r2_score
r2_score(y_test,y_pred)
```

**Visualisasi Plot Loss Training**
```
plt.plot(history.history['loss'])
plt.plot(history.history['val_loss'])
```
![Plot Loss Training](https://raw.githubusercontent.com/4q1l/prediksi-harga-mobil/main/img/2.png)

## Kesimpulan Prediksi
**Gambar Plot Nilai Aktual vs Nilai Prediksi**
![Plot Nilai Aktual vs Nilai Prediksi](https://raw.githubusercontent.com/4q1l/prediksi-harga-mobil/main/img/3.png)

- Model yang telah dilatih memiliki kinerja yang cukup baik dalam memprediksi harga mobil berdasarkan fitur-fitur yang dipilih.
- Meskipun demikian, masih ada sekitar beberapa variasi dalam data yang tidak dapat dijelaskan oleh model.
- Terdapat beberapa faktor lain di luar fitur yang digunakan dalam model yang mungkin juga mempengaruhi harga mobil seperti variabel lain yang tidak dipakai, dan dapat menjadi fokus penelitian lebih lanjut untuk meningkatkan kinerja model.

**Kesimpulan Problem Statement**
1. Pertanyaan 1: Variabel-variabel apa yang signifikan dalam memprediksi harga sebuah mobil?
- carlength (Panjang Mobil): Variabel ini memiliki rentang nilai yang bervariasi cukup signifikan dari 141.1 hingga 208.1 dengan standar deviasi sekitar 12.34, menunjukkan variasi yang cukup besar dalam panjang mobil. Hal ini menandakan bahwa panjang mobil dapat menjadi faktor yang signifikan dalam menentukan harga mobil, karena ada variasi yang cukup besar antara mobil-mobil yang lebih pendek dan lebih panjang.
- carwidth (Lebar Mobil): Variabel ini juga menunjukkan variasi yang cukup besar dari 60.3 hingga 72.3 dengan standar deviasi sekitar 2.15. Ini menunjukkan bahwa lebar mobil juga bisa menjadi faktor yang signifikan dalam menentukan harga mobil, karena ada variasi yang cukup besar antara mobil-mobil yang lebih sempit dan lebih lebar.
- curbweight (Berat Kosong Mobil): Variabel ini memiliki rentang nilai yang cukup besar dari 1488 hingga 4066 dengan standar deviasi sekitar 520.68, menunjukkan variasi yang signifikan dalam berat kosong mobil. Hal ini menandakan bahwa berat kosong mobil dapat menjadi faktor penting dalam menentukan harga mobil, karena ada variasi yang cukup besar antara mobil-mobil yang lebih ringan dan lebih berat.
- carheight (Tinggi Mobil): Meskipun tinggi mobil tidak menunjukkan variasi yang terlalu besar seperti variabel lainnya, tetapi masih ada variasi yang signifikan dari 47.8 hingga 59.8 dengan standar deviasi sekitar 2.44. Ini menandakan bahwa tinggi mobil juga dapat mempengaruhi harga mobil dalam skala yang lebih kecil, terutama jika ada variasi yang signifikan antara mobil-mobil dengan tinggi yang lebih rendah dan lebih tinggi.
- highwaympg (Konsumsi Bahan Bakar di Jalan Raya): Variabel ini memiliki rentang nilai yang cukup besar dari 16 hingga 54 dengan standar deviasi sekitar 6.89, menunjukkan variasi yang cukup besar dalam konsumsi bahan bakar di jalan raya. Hal ini menandakan bahwa konsumsi bahan bakar di jalan raya dapat menjadi faktor penting dalam menentukan harga mobil, karena ada variasi yang cukup besar antara mobil-mobil dengan konsumsi bahan bakar yang lebih efisien dan kurang efisien.

2. Pertanyaan 2: Seberapa baik variabel-variabel tersebut menjelaskan harga sebuah mobil?
Dari nilai koefisien determinasi (R-squared) sebesar 0.6525 yang diperoleh dari model yang telah dilatih, kita dapat membuat beberapa kesimpulan tentang kinerja model dengan memakai 5 variabel tersebut:

- Interpretasi Koefisien Determinasi (R-squared): Nilai R-squared berkisar antara 0 hingga 1. Semakin mendekati 1, semakin baik model dalam menjelaskan variasi dalam data. Nilai 0.6525 menunjukkan bahwa model kita dapat menjelaskan sekitar 65.25% variasi dalam data harga mobil.
- Evaluasi Prediksi Model: Dengan menggunakan metrik R-squared, kita dapat melihat seberapa baik model kita cocok dengan data aktual. Nilai R-squared yang tinggi menunjukkan bahwa model kita memiliki kemampuan yang baik dalam memprediksi harga mobil.

## Cara Menjalankan Proyek

1. Pastikan Anda memiliki lingkungan Python yang tersedia.
2. Unduh semua file proyek dari repositori ini.
3. Buka notebook Jupyter yang berisi kode proyek.
4. Jalankan setiap sel kode dalam notebook secara berurutan untuk melatih model dan melakukan evaluasi.

## Referensi

- Dokumentasi scikit-learn: [https://scikit-learn.org/stable/documentation.html](https://scikit-learn.org/stable/documentation.html)
- Dokumentasi TensorFlow: [https://www.tensorflow.org/api_docs/python/tf](https://www.tensorflow.org/api_docs/python/tf)
- Dokementasi Dataset: [https://www.kaggle.com/datasets/hellbuoy/car-price-prediction?resource](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction?resource)
