# Proyek System Rekomendasi Buku

## Domain Project

Selama beberapa dekade terakhir, dengan munculnya Youtube, Amazon, Netflix, dan banyak layanan web serupa lainnya, sistem pemberi rekomendasi semakin banyak berperan dalam kehidupan kita. Dari e-commerce (menyarankan kepada pembeli artikel yang dapat menarik minat mereka) hingga iklan online (menyarankan kepada pengguna konten yang tepat, sesuai dengan preferensi mereka), sistem pemberi rekomendasi saat ini tidak dapat dihindari dalam perjalanan online kita sehari-hari.
Secara umum, sistem pemberi rekomendasi adalah algoritme yang ditujukan untuk menyarankan item yang relevan kepada pengguna (item seperti film untuk ditonton, teks untuk dibaca, produk untuk dibeli, atau apa pun bergantung pada industri).

Sistem pemberi rekomendasi sangat penting di beberapa industri karena dapat menghasilkan pendapatan yang besar jika efisien atau juga menjadi cara untuk menonjol secara signifikan dari pesaing. Sebagai bukti pentingnya sistem pemberi rekomendasi, kami dapat menyebutkan bahwa, beberapa tahun yang lalu, Netflix menyelenggarakan sebuah tantangan (“hadiah Netflix”) yang tujuannya adalah untuk menghasilkan sistem pemberi rekomendasi yang berkinerja lebih baik daripada algoritmanya sendiri dengan sebuah hadiah. dari 1 juta dolar untuk menang.

**Kenapa Proyek Ini Penting**
- Peningkatan Pengalaman Pengguna: Dengan mampu menyajikan konten atau produk yang sesuai dengan preferensi individu, sistem pemberi rekomendasi meningkatkan pengalaman pengguna secara keseluruhan. Pengguna cenderung lebih puas ketika diberikan rekomendasi yang relevan dan menarik bagi mereka.

- Meningkatkan Retensi dan Konversi: Sistem pemberi rekomendasi yang efisien dapat membantu meningkatkan retensi pengguna dan mengubah pengguna menjadi pelanggan yang berulang. Dengan menyarankan produk atau konten yang tepat, peluang untuk pembelian atau interaksi lebih lanjut dengan platform meningkat.

- Peningkatan Pendapatan: Dalam industri seperti e-commerce dan periklanan online, sistem pemberi rekomendasi yang baik dapat membantu meningkatkan pendapatan dengan meningkatkan konversi penjualan dan tarif iklan. Hal ini dapat menghasilkan dampak finansial yang signifikan bagi perusahaan.

- Daya Saing dan Inovasi: Perusahaan yang mampu mengoptimalkan sistem pemberi rekomendasi mereka dapat menonjol dari pesaing dan menciptakan keunggulan kompetitif. Ini dapat mendorong inovasi lebih lanjut dalam pengembangan algoritma dan strategi pemberian rekomendasi.

**Referensi**
- Salah satu referensi utama adalah "The Netflix Prize" yang diselenggarakan oleh Netflix beberapa tahun yang lalu. Ini adalah contoh konkret dari bagaimana perusahaan melihat pentingnya sistem pemberi rekomendasi yang efisien dan dapat memberikan dorongan besar dalam mengembangkannya.

- Referensi penelitian dan publikasi ilmiah dapat dilihat pada link berikut: [Deep Learning Based Recommender System: A Survey and New Perspectives](https://www.researchgate.net/publication/318671349_Deep_Learning_Based_Recommender_System_A_Survey_and_New_Perspectives)

## Business Understanding

**Problem Statement**

Bagaimana kita dapat meningkatkan pengalaman pengguna dan mengoptimalkan konversi penjualan dengan cara menyajikan rekomendasi yang relevan dan menarik?

**Goals** 

Meningkatkan pengalaman pengguna dan mengoptimalkan konversi penjualan dengan cara menyajikan rekomendasi yang relevan dan menarik

**Solution Statement**

Penelitian ini menggunakan 2 algoritma machine learning sistem rekomendasi untuk menyelesaikan problem statement yaitu:

1. Content-Based Filtering: Content-Based Filtering menggunakan informasi tentang item (konten atau produk) yang disukai oleh pengguna sebelumnya untuk merekomendasikan item yang serupa. Ini dilakukan dengan menganalisis fitur atau atribut dari setiap item dan membangun profil pengguna berdasarkan preferensi mereka.

2. Collaborative Filtering: Collaborative Filtering memanfaatkan informasi tentang preferensi pengguna secara kolektif untuk membuat rekomendasi. Ini dilakukan dengan membandingkan perilaku atau preferensi pengguna yang serupa untuk menyarankan item yang disukai oleh pengguna tersebut.

Algoritma Content Based Filtering digunakan untuk merekemondesikan buku berdasarkan aktivitas pengguna pada masa lalu, sedangkan algoritma Collabarative Filltering digunakan untuk merekomendasikan buku berdasarkan ratings yang paling tinggi.

## Data Understanding

Data atau dataset yang digunakan pada proyek ini adalah data Book Recommendation Dataset yang didapat dari situs kaggle. Link dataset dapat dilihat dari tautan berikut [book-recommendation-data](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset/data). Untuk Rangkuman Dataset dapat dilihat pada Tabel 1

Tabel 1. Rangkuman Dataset
| Jenis                  | Keterangan                                                                                                        |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Sumber                 | [Kaggle Dataset: Book Recommendation Dataset](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset/data)  |
| Lisensi                | CC0: Public Domain                                                                                                           |
| Kategori               | Sosial                                                                                                            |
| Jenis & Ukuran berkas  | CSV (26 MB)													|

**Ringkasan Isi Dataset**

Dataset Book-Recomendation-Dataset terdiri dari 3 file:
- Users (Pengguna)
Berisi informasi tentang pengguna. ID pengguna (User-ID) telah di-anonimkan dan dipetakan ke bilangan bulat. Data demografis juga disediakan (Lokasi, Usia) jika tersedia. Jika tidak, kolom-kolom ini berisi nilai NULL.

- Books (Buku)
Buku-buku diidentifikasi oleh ISBN mereka masing-masing. ISBN yang tidak valid telah dihapus dari dataset. Selain itu, informasi berbasis konten tertentu diberikan (Judul Buku, Penulis Buku, Tahun Penerbitan, Penerbit), yang diperoleh dari Layanan Web Amazon. Perlu diperhatikan bahwa dalam kasus beberapa penulis, hanya yang pertama disediakan. URL yang mengarah ke gambar sampul juga diberikan, muncul dalam tiga variasi (Image-URL-S, Image-URL-M, Image-URL-L), yaitu kecil, sedang, besar. URL ini mengarah ke situs web Amazon.

-Ratings (Peringkat)
Berisi informasi peringkat buku. Peringkat (Book-Rating) bisa jelas, diekspresikan dalam skala dari 1-10 (nilai lebih tinggi menunjukkan apresiasi yang lebih tinggi), atau implisit, diekspresikan dengan 0.

Untuk penjelasan mengenai variabel dari Book.csv dapat dilihat pada tabel 2

Tabel 2. Penjelasan Variabel dari Books.csv
| Variabel               | Penjelasan                                                                                                             |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ISBN                   | ISBN (International Standard Book Number) adalah kode unik yang diberikan untuk mengidentifikasi sebuah buku secara global.                                                          |
| Book-Title             | Judul buku.                                                                                                            |
| Book-Author            | Penulis buku.                                                                                                          |
| Year-Of-Publication    | Tahun penerbitan buku.                                                                                                |
| Publisher              | Penerbit buku.                                                                                                         |
| Image-URL-S            | URL gambar kecil (kecil) buku.                                                                                        |
| Image-URL-M            | URL gambar sedang (medium) buku.                                                                                      |
| Image-URL-L            | URL gambar besar (besar) buku.                                                                                        |

Kemudian Untuk penjelasan mengenai variabel dari Users.csv dapat dilihat pada tabel 3

Tabel 3. Penjelasan Variabel dari User.csv
| Variabel | Penjelasan                              |
|----------|-----------------------------------------|
| User-ID  | ID unik yang menandakan setiap pengguna. Digunakan untuk mengidentifikasi pengguna secara unik dalam dataset. |
| Location | Lokasi geografis dari pengguna.         |
| Age      | Usia pengguna.                          |

Dan untuk penjelasan mengenai variabel dari Ratings.csv dapat dilihat pada tabel 4

Tabel 4. Penjelasan Variabel dari Ratings.csv
| Variabel   | Deskripsi                                                |
|------------|----------------------------------------------------------|
| User-ID    | ID unik yang menunjukkan pengguna yang memberikan rating pada buku. |
| ISBN       | Kode unik yang menunjukkan buku yang diberi rating oleh pengguna.   |
| Book-Rating | Penilaian yang diberikan oleh pengguna pada buku tertentu. Nilai berkisar dari 1 hingga 10, di mana 1 menunjukkan rating terendah dan 10 menunjukkan rating tertinggi. |

Untuk tahapan yang dilakukan pada Data Understanding adalah sebagai berikut:
1. Data buku, peringkat, dan pengguna dimuat menggunakan pustaka `pandas`.
2. Dilakukan pemeriksaan jumlah data unik di setiap dataset.
3. Dilakukan pemeriksaan tipe data setiap kolom di setiap dataset.

## Data Preparation

**Tahapan Data Preparation**
### Content-Based Filtering
- Dilakukan penggabungan data peringkat dengan data buku dan data pengguna berdasarkan ISBN dan User-ID.
    - Ini dilakukan agar informasi tentang peringkat, buku, dan pengguna dapat digunakan secara bersamaan dalam analisis.
- Dilakukan pengolahan data untuk mengatasi nilai yang hilang.
    - Nilai yang hilang diidentifikasi dan dihapus dari dataset agar tidak mengganggu analisis.
- Dilakukan pembuangan duplikat dan pengambilan data unik berdasarkan ISBN.
    - Duplikat berdasarkan ISBN dihapus untuk memastikan setiap buku hanya muncul sekali dalam analisis.
- Dilakukan vektorisasi teks menggunakan TF-IDF untuk deskripsi buku.
    - Deskripsi buku dalam bentuk teks diubah menjadi representasi numerik yang dapat digunakan untuk mengukur kesamaan antar-buku.
- Dihasilkan matriks cosine similarity untuk menemukan kesamaan antar-buku.
    - Matriks cosine similarity digunakan untuk menghitung seberapa mirip satu buku dengan yang lain berdasarkan vektor TF-IDF dari deskripsi buku.

### Collaborative Filtering
- Dilakukan encoding untuk User-ID dan ISBN.
    - User-ID dan ISBN diubah menjadi nilai indeks yang dapat digunakan oleh model untuk pemodelan.
- Dilakukan normalisasi peringkat.
    - Peringkat buku dinormalisasi untuk memastikan perbandingan yang konsisten antara nilai peringkat.
- Dilakukan pemisahan data untuk pelatihan dan validasi.
    - Data dibagi menjadi dua subset: data pelatihan dan data validasi, yang digunakan untuk melatih dan menguji model Collaborative Filtering.

## Modelling and Result

**Modelling Step**
### Content-Based Filtering
- **Modelling:**
    - Digunakan metode Content-Based Filtering dengan menggunakan matriks cosine similarity dari deskripsi buku.
    - Fungsi rekomendasi buku dibuat untuk memberikan rekomendasi berdasarkan kesamaan antara deskripsi buku yang ada dalam dataset.
    - Menggunakan fungsi `book_recommendations(book_title)` untuk mendapatkan rekomendasi buku berdasarkan judul buku yang dipilih.

**Result:**
    - Contoh hasil rekomendasi buku berdasarkan judul buku yang dipilih bisa dilihat pada gambar 1
![Hasil Content-Based Filtering](https://raw.githubusercontent.com/4q1l/prediksi-harga-mobil/main/img/10.JPG)

Gambar 1. Hasil rekomendasi buku Content-Based Filtering

    - Anda dapat menggunakan fungsi `book_recommendations(book_title)` untuk mendapatkan rekomendasi buku berdasarkan judul buku yang dipilih.

### Collaborative Filtering
- **Modelling:**
    - Metode Collaborative Filtering digunakan dengan membangun model neural network menggunakan TensorFlow.
    - Model ini memanfaatkan embedding layers untuk merepresentasikan pengguna dan buku dalam ruang laten.
    - Menggunakan fungsi `get_book_recommendations(user_id, model, books_df)` untuk mendapatkan rekomendasi buku untuk pengguna tertentu.

**Result:**
    - Hasil evaluasi model dan contoh rekomendasi buku untuk seorang pengguna dapat dilihat pada gambar 2
![Hasil Collaborative Filtering](https://raw.githubusercontent.com/4q1l/prediksi-harga-mobil/main/img/9.JPG)

Gambar 2. Hasil rekomendasi Collaborative Filtering

    - Menggunakan fungsi `get_book_recommendations(user_id, model, books_df)` untuk mendapatkan rekomendasi buku untuk pengguna tertentu. 

## Evaluasi Model

Evaluasi metrik yang digunakan untuk mengukur kinerja model adalah metrik RMSE (Root Mean Squared Error).

- RMSE adalah metode pengukuran dengan mengukur perbedaan nilai dari prediksi sebuah model sebagai estimasi atas nilai yang diobservasi. Root Mean Square Error adalah hasil dari akar kuadrat Mean Square Error. Keakuratan metode estimasi kesalahan pengukuran ditandai dengan adanya nilai RMSE yang kecil. Metode estimasi yang mempunyai Root Mean Square Error (RMSE) lebih kecil dikatakan lebih akurat daripada metode estimasi yang mempunyai Root Mean Square Error (RMSE) lebih besar

- Kelebihan dan kekurang matriks ini adalah :

  **kelebihan** : menghukum kesalahan besar lebih sehingga bisa lebih tepat dalam beberapa kasus.  
  **Kekurangan** : memberikan bobot yang relatif tinggi untuk kesalahan besar. Ini berarti RMSE harus lebih berguna ketika kesalahan besar sangat tidak diinginkan

- formula dari matriks RMSE adalah sebagai berikut

![formula matriks RMSE](https://raw.githubusercontent.com/onedayxzn/submission_file/master/rumusRMSE.png)

keterangan : <br>
At : Nilai Aktual. <br>
ft = Nilai hasil peramalan.<br>
N = banyaknya dataset<br>

hasil dari model evaluasi visualisasi matriks adalah sebagai berikut :  
![hasil Evaluasi](https://github.com/4q1l/prediksi-harga-mobil/blob/main/8.png)

dari visualisasi proses training model di atas cukup smooth dan model konvergen pada epochs sekitar 100. Dari proses ini, diperoleh nilai error akhir sebesar sekitar 0.2677 dan error pada data validasi sebesar 0.2683.