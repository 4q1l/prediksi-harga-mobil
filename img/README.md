# Proyek System Rekomendasi Buku

## Project Overview

Dalam era digital saat ini, sistem rekomendasi telah menjadi bagian integral dari pengalaman online. Mulai dari platform seperti Youtube, Amazon, Netflix, dan banyak lagi, sistem ini berperan penting dalam menyajikan konten atau produk yang sesuai dengan preferensi pengguna. Dalam konteks industri pemasaran dan perdagangan online, sistem rekomendasi buku menjadi relevan karena memiliki dampak besar terhadap pengalaman pengguna, retensi pelanggan, konversi penjualan, dan daya saing perusahaan.

Keberhasilan sebuah platform e-commerce atau perpustakaan digital tidak hanya ditentukan oleh katalog produknya, tetapi juga oleh kemampuannya untuk menyajikan rekomendasi yang relevan kepada pengguna[1]. Dalam konteks ini, proyek sistem rekomendasi buku menjadi penting karena:

Pertama, meningkatnya jumlah buku yang tersedia di pasar membuat konsumen sering kali kesulitan dalam menavigasi pilihan yang ada. Dengan adanya sistem rekomendasi yang efisien, pengguna dapat diberikan rekomendasi buku yang sesuai dengan preferensi mereka, membantu mereka menemukan konten yang relevan dan menarik.

Kedua, sistem rekomendasi buku dapat membantu mengatasi masalah kelelahan keputusan yang sering dialami oleh pengguna. Dalam era di mana dibanjiri dengan informasi, memiliki sistem yang mampu menyaring dan menyarankan buku-buku yang sesuai dapat mengurangi beban pengambilan keputusan pengguna[2].

Contoh konkret dari permasalahan yang dihadapi adalah ketika seorang pengguna ingin menemukan buku baru untuk dibaca tetapi terjebak dalam memilih dari berbagai opsi yang tersedia. Dalam hal ini, sistem rekomendasi buku dapat menganalisis preferensi sebelumnya, pola baca, dan perilaku pengguna lainnya untuk menyajikan rekomendasi yang relevan dan personal.

Penerapan hasil proyek ini diharapkan dapat memberikan manfaat yang nyata kepada pengguna. Misalnya, dengan menggunakan algoritma machine learning yang canggih, sistem ini dapat memprediksi preferensi pengguna dengan lebih akurat dari waktu ke waktu, sehingga menyediakan rekomendasi yang semakin sesuai. Selain itu, integrasi dengan fitur ulasan dan rekomendasi dari pengguna lain dapat meningkatkan interaksi sosial di platform dan memperkaya pengalaman membaca.

Dengan meningkatnya persaingan di pasar buku online, memiliki sistem rekomendasi buku yang efisien dan inovatif dapat menjadi keunggulan kompetitif bagi perusahaan. Ini tidak hanya memungkinkan perusahaan untuk mempertahankan pelanggan yang ada tetapi juga menarik pelanggan baru melalui pengalaman pengguna yang disesuaikan dan memuaskan.

## Business Understanding

**Permasalahan**

Bagaimana cara meningkatkan pengalaman pembaca dengan menyajikan rekomendasi yang spesifik dan menarik?

**Tujuan**

Meningkatkan kepuasan pembaca dengan menyediakan rekomendasi yang sesuai dengan preferensi pengguna.

**Pernyataan Solusi**

Penelitian ini memanfaatkan dua algoritma machine learning untuk menangani permasalahan tersebut:

1. Content-Based Filtering: Menggunakan informasi tentang buku-buku yang disukai oleh pembaca sebelumnya untuk merekomendasikan buku yang serupa. Algoritma ini menganalisis fitur-fitur buku seperti genre, penulis, dan sinopsis untuk membangun profil preferensi pembaca.

2. Collaborative Filtering: Memanfaatkan informasi rating dan ulasan buku dari pembaca lain untuk membuat rekomendasi. Dengan membandingkan preferensi pembaca yang serupa, algoritma ini menyajikan buku yang memiliki rating tertinggi atau yang paling sering disukai oleh pembaca dengan preferensi serupa.

Kedua algoritma ini dirancang khusus untuk konteks rekomendasi buku, memungkinkan rekomendasi disajikan lebih relevan dan menarik kepada pembaca.

**Manfaat Bisnis dan Dampak Ekonomi**

Penelitian ini memiliki potensi untuk memberikan dampak yang signifikan dalam dua bidang utama:

- Kepuasan Pembaca dan Retensi Pelanggan: Dengan menyediakan rekomendasi buku yang sesuai dengan preferensi pembaca, dapat meningkatkan pengalaman membaca dan kepuasan pelanggan. Pembaca akan merasa lebih terhubung dengan platform karena mereka mendapatkan rekomendasi yang relevan, yang kemudian dapat meningkatkan retensi pelanggan.

- Peningkatan Penjualan Buku: Dengan menggunakan algoritma rekomendasi yang canggih, dapat meningkatkan konversi penjualan buku. Rekomendasi yang akurat dan menarik dapat mendorong pembaca untuk mengeksplorasi buku-buku baru dan membuat pembelian tambahan. Hal ini berpotensi meningkatkan pendapatan dari penjualan buku dan memperkuat posisi di pasar.

Stakeholder utama dari penelitian ini meliputi penerbit buku, platform e-commerce buku, dan pembaca. Penerapan hasil penelitian ini secara aplikatif akan melibatkan integrasi algoritma rekomendasi ke dalam platform e-commerce buku yang ada, sehingga pembaca dapat langsung mengakses rekomendasi saat mereka menjelajahi katalog buku. Ini akan memungkinkan pengalaman berbelanja yang lebih personal dan menarik bagi pembaca, sambil membantu penerbit dan platform e-commerce meningkatkan penjualan buku mereka.

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

### Content-Based Filtering
1. Penanganan Nilai yang Hilang

- Missing value adalah nilai yang tidak ada dalam dataset. Untuk mengatasi hal ini, dilakukan identifikasi nilai yang hilang dalam dataset dan menghapusnya agar tidak mengganggu analisis selanjutnya.

2. Penghapusan Duplikat dan Pengambilan Data Unik

- Duplikat berdasarkan ISBN dihapus untuk memastikan setiap buku hanya muncul sekali dalam analisis. Ini dilakukan agar hasil analisis tidak terpengaruh oleh adanya duplikat data.

3. Vektorisasi Teks menggunakan TF-IDF

- Vektorisasi teks adalah proses mengubah teks menjadi representasi numerik yang dapat digunakan untuk analisis. Digunakan metode TF-IDF (Term Frequency-Inverse Document Frequency) untuk mengubah deskripsi buku menjadi vektor numerik. Ini memungkinkan pengkuran kesamaan antar-buku berdasarkan konten teks mereka.

4. Membuat Matriks Cosine Similarity

- Matriks cosine similarity digunakan untuk mengukur seberapa mirip satu buku dengan yang lain berdasarkan vektor TF-IDF dari deskripsi buku. Ini dilakukan dengan menghitung kosinus dari sudut antara vektor TF-IDF dari setiap pasangan buku. Semakin tinggi nilai cosine similarity antara dua buku, semakin mirip konten teksnya.


### Collaborative Filtering
1. Encoding User-ID dan ISBN

- User-ID dan ISBN diubah menjadi nilai indeks yang dapat digunakan oleh model untuk pemodelan. Ini dilakukan untuk mengubah fitur kategorikal menjadi bentuk numerik yang dapat diproses oleh algoritma machine learning.

2. Normalisasi Peringkat

- Normalisasi peringkat buku dilakukan untuk memastikan perbandingan yang konsisten antara nilai peringkat. Ini membantu dalam membandingkan preferensi pengguna secara akurat tanpa adanya bias pada rentang nilai peringkat.

3. Pemisahan Data untuk Pelatihan dan Validasi

- Data dibagi menjadi dua subset: data pelatihan dan data validasi. Data pelatihan digunakan untuk melatih model Collaborative Filtering, sedangkan data validasi digunakan untuk menguji kinerja model. Pemisahan ini penting untuk mengevaluasi seberapa baik model dapat membuat rekomendasi buku yang akurat dan relevan.

## Modelling and Result

**Modelling Step**
### Content-Based Filtering
- **Modelling:**
    - Metode Content-Based Filtering dipilih karena fokus pada kesamaan antara fitur-fitur buku berdasarkan deskripsi mereka.
    - Matriks cosine similarity digunakan untuk mengukur kesamaan antara deskripsi buku dalam dataset.
    - Fungsi rekomendasi buku dibuat untuk memberikan rekomendasi berdasarkan kesamaan deskripsi buku.
    - Matriks cosine similarity digunakan untuk menghasilkan rekomendasi buku yang sesuai dengan preferensi pengguna berdasarkan judul buku yang dipilih.

**Top-N Recommendation**
Rekomendasi Berdasarkan judul bisa dilihat pada tabel 5

Tabel 5. Rekomendasi Berdasarkan judul The Kitchen God's Wife

| No. | Judul Buku                                    |
|-----|-----------------------------------------------|
| 1   | Decision in Normandy                          |
| 2   | Nights Below Station Street                   |
| 3   | The Middle Stories                            |
| 4   | Goodbye to the Buttermilk Sky                |
| 5   | New Vegetarian: Bold and Beautiful Recipes for Every Occasion |


Gambar 1. Hasil rekomendasi buku Content-Based Filtering

Fungsi `book_recommendations(book_title)` digunakan untuk mendapatkan rekomendasi buku berdasarkan judul buku yang dipilih.

### Collaborative Filtering
- **Modelling:**
    - Metode Collaborative Filtering digunakan karena model ini mampu mempelajari preferensi pengguna secara kolektif dan memberikan rekomendasi berdasarkan kesamaan preferensi pengguna.
    - Model neural network dibangun menggunakan TensorFlow dengan menggunakan embedding layers untuk merepresentasikan pengguna dan buku dalam ruang laten.
    - Fungsi get_book_recommendations(user_id, model, books_df) digunakan untuk mendapatkan rekomendasi buku untuk pengguna tertentu.

**Top-N Recommendation**
Top 10 Book Recommendations bisa dilihat pada tabel 6

Tabel 6. Top 10 Book Recommendations for User 276725

| No. | Book Title                                             | ISBN         |
|-----|--------------------------------------------------------|--------------|
| 1   | Die Zwei Turme II                                     | 3608935428   |
| 2   | The Girl Who Loved Tom Gordon : A Novel                | 0684867621   |
| 3   | The Watsons Go to Birmingham - 1963 (Yearling Newbery) | 0440414121   |
| 4   | Die Wiederkehr Des Konigs III                          | 3608935436   |
| 5   | Title Kassandra. ErzÃ?Â¤hlung. ( Sammlung Luchterhand im dtv) | 3423118709   |
| 6   | Parque JurÃ¡sico                                      | 840149236X   |
| 7   | Agu Trot [spanish edition]                             | 8420444367   |
| 8   | Unknown Title                                          | 0099414732   |
| 9   | Momo (Spanish Language Edition)                        | 8420432113   |
| 10  | The Music of Chance                                   | 0140154078   |


## Evaluasi Model

Evaluasi metrik yang digunakan untuk mengukur kinerja model adalah metrik RMSE (Root Mean Squared Error).

- RMSE adalah metode pengukuran dengan mengukur perbedaan nilai dari prediksi sebuah model sebagai estimasi atas nilai yang diobservasi. Root Mean Square Error adalah hasil dari akar kuadrat Mean Square Error. Keakuratan metode estimasi kesalahan pengukuran ditandai dengan adanya nilai RMSE yang kecil. Metode estimasi yang mempunyai Root Mean Square Error (RMSE) lebih kecil dikatakan lebih akurat daripada metode estimasi yang mempunyai Root Mean Square Error (RMSE) lebih besar

- Kelebihan dan kekurang matriks ini adalah :

  **kelebihan** : menghukum kesalahan besar lebih sehingga bisa lebih tepat dalam beberapa kasus.  
  **Kekurangan** : memberikan bobot yang relatif tinggi untuk kesalahan besar. Ini berarti RMSE harus lebih berguna ketika kesalahan besar sangat tidak diinginkan

- Formula dari matriks RMSE adalah sebagai berikut

$$
\begin{aligned}
\text{RMSE} &= \sqrt{\frac{1}{N} \sum_{i=1}^{N} (A_i - \hat{A}_i)^2}
\end{aligned}
$$

Keterangan:

- $\( A_i \)$ adalah nilai aktual.
- $\( \hat{A}_i \)$ adalah nilai hasil peramalan.
- $\( N \)$ adalah banyaknya dataset.

Hasil dari model evaluasi visualisasi matriks dapat dilihat pada gambar 1  

![Hasil Evaluasi](https://raw.githubusercontent.com/4q1l/prediksi-harga-mobil/main/img/8.png)

Gambar 1. Hasil dari model evaluasi visualisasi matriks

**Hasil Evaluasi**

Dari visualisasi proses training model di atas, terlihat bahwa proses training berjalan dengan lancar dan model konvergen pada epochs sekitar 100. Nilai RMSE akhir yang diperoleh adalah sekitar 0.2677 untuk data training dan 0.2683 untuk data validasi.

**Interpretasi**

Dalam konteks proyek ini, tujuan utama adalah meningkatkan pengalaman pengguna dengan menyajikan rekomendasi yang relevan dan menarik. Dengan nilai RMSE yang rendah, menunjukkan bahwa model memiliki tingkat kesalahan prediksi yang rendah. Oleh karena itu, dapat disimpulkan bahwa model berhasil dalam memberikan rekomendasi buku yang akurat dan relevan, sesuai dengan goals dan solusi yang diinginkan dari proyek ini.

Hasil evaluasi yang memuaskan ini menunjukkan bahwa proyek ini berhasil dalam menyelesaikan permasalahan yang diangkat, yaitu meningkatkan pengalaman pengguna melalui rekomendasi buku. Model yang dihasilkan mampu memberikan rekomendasi yang tepat dan sesuai dengan preferensi pengguna, sehingga mencapai tujuan proyek secara efektif.

## Referensi

[1] Y. Koren, R. Bell, dan C. Volinsky, "Matrix factorization techniques for recommender systems," Computer, vol. 42, no. 8, hal. 30-37, 2009.

[2] S. Zhang, L. Yao, A. Sun, dan Y. Tay, "Deep learning based recommender system: A survey and new perspectives," ACM Computing Surveys (CSUR), vol. 52, no. 1, hal. 1-38, 2019.

[3] Netflix Prize, "Diakses pada 26 Maret 2024," [Online]. Tersedia: https://www.netflixprize.com/.



