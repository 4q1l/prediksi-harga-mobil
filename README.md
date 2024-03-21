# Proyek Prediksi Harga Mobil dengan Analisis Data

## Latar Belakang

Sebuah perusahaan otomotif Tiongkok, Geely Auto, bermimpi untuk memasuki pasar AS dengan mendirikan unit manufaktur mereka di sana dan memproduksi mobil secara lokal untuk bersaing dengan pesaing-pesaing mereka di AS dan Eropa.

Mereka telah mengontrak sebuah perusahaan konsultan otomotif untuk memahami faktor-faktor yang memengaruhi penetapan harga mobil. Secara khusus, mereka ingin memahami faktor-faktor yang memengaruhi penetapan harga mobil di pasar Amerika, karena faktor-faktor tersebut mungkin sangat berbeda dari pasar Tiongkok. Perusahaan tersebut ingin mengetahui:

1. Variabel apa yang signifikan dalam memprediksi harga sebuah mobil.
2. Seberapa baik variabel-variabel tersebut menjelaskan harga sebuah mobil.

Berdasarkan berbagai survei pasar, perusahaan konsultan tersebut telah mengumpulkan kumpulan data besar dari berbagai jenis mobil di pasar Amerika.

## Business Understanding

**Problem Statements:**
1. Variabel apa yang signifikan dalam memprediksi harga sebuah mobil.
2. Seberapa baik variabel-variabel tersebut menjelaskan harga sebuah mobil.

**Goals:**
1. Menemukan variabel-variabel yang paling berpengaruh dalam menentukan harga mobil di pasar Amerika Serikat.
2. Mengembangkan model machine learning yang dapat memprediksi harga mobil dengan akurasi yang tinggi.

**Solution Statement:**
1. Melakukan pemodelan dengan menggunakan beberapa algoritma machine learning dan membandingkan kinerja mereka.
2. Menyesuaikan parameter pada algoritma untuk meningkatkan akurasi prediksi.

## Pemahaman Data

**Deskripsi Data:**
- Jumlah data: 205
- Fitur-fitur utama: carlength, carwidth, curbweight, carheight, highwaympg
- Target: price

Dari deskripsi dataframe yang diberikan, kita dapat melihat statistik deskriptif untuk setiap variabel. Dari sini, kita dapat memilih variabel yang paling signifikan untuk dimasukkan ke dalam model prediksi harga mobil.

| Variabel       | Alasan Memilihnya                                                     |
|----------------|------------------------------------------------------------------------|
| carlength      | Panjang mobil memiliki variasi yang cukup besar dan dapat mempengaruhi harga mobil.                                         |
| carwidth       | Lebar mobil juga memiliki variasi yang signifikan dan memainkan peran penting dalam penetapan harga mobil.                                    |
| curbweight     | Berat kosong mobil dapat menjadi faktor penting dalam menentukan harga mobil karena variasi yang signifikan dalam data.  |
| carheight      | Meskipun variasinya tidak terlalu besar, tinggi mobil juga dapat mempengaruhi harga mobil dalam skala yang lebih kecil.                     |
| highwaympg     | Konsumsi bahan bakar di jalan raya adalah faktor yang penting dalam menentukan harga mobil karena efisiensinya.                      |

## Persiapan Data

**Data Preparation Steps:**
1. Memilih fitur-fitur yang signifikan.
2. Penskalaan fitur menggunakan StandardScaler.
3. Pembagian dataset menjadi set pelatihan dan pengujian.

```python
# Memilih fitur-fitur yang signifikan
numerical_columns_without_price_carID = [col for col in numerical_columns if col not in ['price', 'car_ID']]
X = df[['carlength','carwidth','curbweight','carheight','highwaympg']]
y=df['price']

# Penskalaan fitur
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
X = scaler.fit_transform(X)
y=scaler.fit_transform(y.values.reshape(-1,1))

# Pembagian dataset
from sklearn.model_selection import train_test_split
X_train,X_test,y_train,y_test = train_test_split(X,y,test_size=0.1,random_state=0,shuffle=True)
```

## Pelatihan Model

Model dilatih menggunakan jaringan saraf tiruan (neural network) dengan menggunakan variabel-variabel yang dipilih. Kami menggunakan metrik koefisien determinasi (R-squared) untuk mengevaluasi seberapa baik model kami cocok dengan data.

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
y_pred = model.predict(X_test)
from sklearn.metrics import r2_score
r2_score(y_test,y_pred)

## Kesimpulan

- Model yang telah dilatih memiliki kinerja yang cukup baik dalam memprediksi harga mobil berdasarkan fitur-fitur yang dipilih.
- Meskipun demikian, masih ada sekitar beberapa variasi dalam data yang tidak dapat dijelaskan oleh model.
- Terdapat beberapa faktor lain di luar fitur yang digunakan dalam model yang mungkin juga mempengaruhi harga mobil seperti variabel lain yang tidak dipakai, dan dapat menjadi fokus penelitian lebih lanjut untuk meningkatkan kinerja model.

## Cara Menjalankan Proyek

1. Pastikan Anda memiliki lingkungan Python yang tersedia.
2. Unduh semua file proyek dari repositori ini.
3. Buka notebook Jupyter yang berisi kode proyek.
4. Jalankan setiap sel kode dalam notebook secara berurutan untuk melatih model dan melakukan evaluasi.

## Referensi

- Dokumentasi scikit-learn: [https://scikit-learn.org/stable/documentation.html](https://scikit-learn.org/stable/documentation.html)
- Dokumentasi TensorFlow: [https://www.tensorflow.org/api_docs/python/tf](https://www.tensorflow.org/api_docs/python/tf)
- Dokementasi Dataset: [https://www.kaggle.com/datasets/hellbuoy/car-price-prediction?resource](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction?resource)
