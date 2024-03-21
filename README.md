# Prediksi Harga Mobil dengan Analisis Data

## Pernyataan Masalah

Sebuah perusahaan otomotif Tiongkok, Geely Auto, bermimpi untuk memasuki pasar AS dengan mendirikan unit manufaktur mereka di sana dan memproduksi mobil secara lokal untuk bersaing dengan pesaing-pesaing mereka di AS dan Eropa.

Mereka telah mengontrak sebuah perusahaan konsultan otomotif untuk memahami faktor-faktor yang memengaruhi penetapan harga mobil. Secara khusus, mereka ingin memahami faktor-faktor yang memengaruhi penetapan harga mobil di pasar Amerika, karena faktor-faktor tersebut mungkin sangat berbeda dari pasar Tiongkok. Perusahaan tersebut ingin mengetahui:

1. Variabel apa yang signifikan dalam memprediksi harga sebuah mobil.
2. Seberapa baik variabel-variabel tersebut menjelaskan harga sebuah mobil.

Berdasarkan berbagai survei pasar, perusahaan konsultan tersebut telah mengumpulkan kumpulan data besar dari berbagai jenis mobil di pasar Amerika.

## Pemahaman Data

Dari deskripsi dataframe yang diberikan, kita dapat melihat statistik deskriptif untuk setiap variabel. Dari sini, kita dapat memilih variabel yang paling signifikan untuk dimasukkan ke dalam model prediksi harga mobil.

| Variabel       | Alasan Memilihnya                                                     |
|----------------|------------------------------------------------------------------------|
| carlength      | Panjang mobil memiliki variasi yang cukup besar dan dapat mempengaruhi harga mobil.                                         |
| carwidth       | Lebar mobil juga memiliki variasi yang signifikan dan memainkan peran penting dalam penetapan harga mobil.                                    |
| curbweight     | Berat kosong mobil dapat menjadi faktor penting dalam menentukan harga mobil karena variasi yang signifikan dalam data.  |
| carheight      | Meskipun variasinya tidak terlalu besar, tinggi mobil juga dapat mempengaruhi harga mobil dalam skala yang lebih kecil.                     |
| highwaympg     | Konsumsi bahan bakar di jalan raya adalah faktor yang penting dalam menentukan harga mobil karena efisiensinya.                      |

## Persiapan Data

Setelah memilih variabel-variabel yang signifikan, langkah selanjutnya adalah mempersiapkan data untuk pelatihan model. Ini melibatkan penskalaan fitur-fitur numerik dan membagi data menjadi set pelatihan dan pengujian.

## Pelatihan Model

Model dilatih menggunakan jaringan saraf tiruan (neural network) dengan menggunakan variabel-variabel yang dipilih. Kami menggunakan metrik koefisien determinasi (R-squared) untuk mengevaluasi seberapa baik model kami cocok dengan data.

## Evaluasi Model

Model dievaluasi menggunakan R-squared untuk memeriksa seberapa baik model tersebut memprediksi harga mobil. Dari nilai R-squared sebesar 0.6525, kami menyimpulkan bahwa model kami mampu menjelaskan sekitar 65.25% variasi dalam data harga mobil.

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
- Dokementasi Dataset: [https://www.kaggle.com/datasets/hellbuoy/car-price-prediction?resource=download](https://www.kaggle.com/datasets/hellbuoy/car-price-prediction?resource=download)