![image](https://github.com/user-attachments/assets/9098c705-6eb7-44d7-8ef9-a76ba84c4704)# Proyek Kedua Machine Learning Terapan | Movie Recommendation Using Content Based Filltering and Collaborative Filltering

###### Disusun oleh : Ida Bagus Agung Bajerapany

Proyek ini membangun model yang dapat memberikan rekomendasi film

## 1. Project Domain

Sistem rekomendasi film merupakan alat penting dalam membantu pengguna menemukan konten yang sesuai dengan preferensi mereka di tengah banyaknya pilihan yang tersedia. Dengan perkembangan teknologi digital, jumlah film yang dirilis setiap tahun meningkat pesat, sehingga memunculkan tantangan bagi pengguna untuk memilih film yang tepat. Sistem rekomendasi berfungsi untuk memberikan saran berdasarkan data interaksi pengguna sebelumnya dan karakteristik film, sehingga pengguna dapat dengan mudah menemukan film yang mungkin mereka sukai. Terdapat dua pendekatan utama dalam pengembangan sistem rekomendasi: content-based filtering dan collaborative filtering.

Content-based filtering merekomendasikan film berdasarkan kemiripan atribut dari film yang sudah disukai pengguna sebelumnya, seperti genre, sutradara, atau aktor [1] [2]. Metode ini memungkinkan sistem untuk memberikan rekomendasi yang relevan dengan minat pengguna tanpa memerlukan data dari pengguna lain. Di sisi lain, collaborative filtering memanfaatkan data interaksi dari banyak pengguna untuk menemukan pola dan hubungan antar film, sehingga dapat merekomendasikan film berdasarkan kesamaan preferensi di antara pengguna [3]. Pendekatan ini sangat efektif dalam mengatasi masalah data sparsity dan cold start yang sering dihadapi oleh sistem rekomendasi.

Kombinasi kedua metode ini dalam sistem rekomendasi film dapat meningkatkan akurasi dan relevansi rekomendasi yang diberikan kepada pengguna. Penelitian sebelumnya menunjukkan bahwa penggunaan metode hybrid, yang menggabungkan content-based dan collaborative filtering, dapat memberikan hasil yang lebih baik dibandingkan dengan menggunakan salah satu metode secara terpisah [4]. Dengan demikian, pengembangan sistem rekomendasi film yang mengintegrasikan kedua pendekatan ini tidak hanya akan meningkatkan pengalaman pengguna tetapi juga akan memperluas jangkauan konten yang dapat ditemukan oleh pengguna.

### Mengapa Proyek Ini Penting Untuk Diselesaikan?

Proyek pengembangan sistem rekomendasi film ini sangat penting untuk diselesaikan karena mampu menjawab tantangan yang dihadapi oleh pengguna dalam memilih film di tengah jumlah konten yang terus meningkat. Sistem ini bertujuan untuk memberikan rekomendasi yang relevan dan personal, sehingga dapat meningkatkan pengalaman pengguna secara signifikan. Berikut adalah beberapa alasan mengapa proyek ini penting:

#### 1. Mengatasi Overload Informasi
Dengan ribuan film yang dirilis setiap tahun, pengguna sering kesulitan menemukan film yang sesuai dengan preferensi mereka. Sistem rekomendasi membantu menyaring dan memprioritaskan pilihan berdasarkan data yang relevan, sehingga mempermudah proses pengambilan keputusan.

#### 2. Peningkatan Pengalaman Pengguna
Sistem rekomendasi yang akurat dapat memberikan pengalaman yang lebih personal dan menyenangkan bagi pengguna, dengan menyajikan pilihan film yang sesuai dengan minat mereka tanpa perlu mencari secara manual.

#### 3. Menggunakan Teknologi Terkini
Menggabungkan metode content-based filtering dan collaborative filtering dalam pendekatan hybrid memungkinkan sistem untuk memberikan rekomendasi yang lebih akurat, relevan, dan efisien. Hal ini juga memperlihatkan inovasi dalam penggunaan data dan algoritma.

#### 4. Memecahkan Masalah Umum dalam Sistem Rekomendasi
Sistem ini dirancang untuk mengatasi masalah umum seperti cold start dan data sparsity, yang sering menjadi kendala dalam pengembangan sistem rekomendasi. Dengan pendekatan hybrid, pengguna baru maupun pengguna lama dapat memperoleh rekomendasi yang berkualitas.

#### 5. Meningkatkan Aksesibilitas Konten
Sistem rekomendasi memungkinkan pengguna untuk menemukan film-film yang mungkin tidak mereka pertimbangkan sebelumnya, memperluas wawasan mereka terhadap berbagai jenis konten.

#### 6. Kontribusi pada Industri Digital dan Hiburan:
Sistem ini tidak hanya bermanfaat bagi pengguna, tetapi juga membantu platform penyedia film untuk meningkatkan keterlibatan pengguna dan kepuasan mereka, yang pada akhirnya dapat meningkatkan pendapatan.


### State Of The Art Penelitian Sebelumnya

1. Jurnal "Content Based Movie Recommendation System" oleh N. Pradeep et al. mengembangkan sistem rekomendasi film yang berfokus pada analisis konten untuk membantu pengguna menemukan film yang sesuai dengan minat mereka. Sistem ini memanfaatkan atribut seperti pemeran, kata kunci, kru, dan genre untuk merekomendasikan film berdasarkan film yang sebelumnya disukai oleh pengguna. Hasil dari penelitian ini menunjukkan bahwa sistem yang diusulkan dapat memberikan rekomendasi yang relevan dan akurat. Pengguna dapat memasukkan nama film yang mereka sukai, dan sistem akan menghitung kesamaan menggunakan matriks kosinus untuk menampilkan sepuluh film yang mirip. Selain itu, sistem juga menyediakan informasi tentang lima film terpopuler dan lima film dengan suara terbanyak, sehingga pengguna dapat menjelajahi pilihan yang lebih luas. Kesimpulan dari penelitian ini menegaskan bahwa sistem rekomendasi berbasis konten ini efektif dalam mengatasi tantangan informasi berlebih yang sering dihadapi oleh pengguna saat mencari film. Dengan tidak bergantung pada data pengguna lain, sistem ini memberikan rekomendasi yang lebih personal dan relevan, serta menjaga privasi pengguna karena mereka tidak perlu membagikan informasi pribadi. Penelitian ini menunjukkan bahwa pendekatan berbasis konten memiliki potensi besar untuk meningkatkan pengalaman pengguna dalam menemukan film yang sesuai dengan preferensi mereka, serta dapat diimplementasikan dalam aplikasi web untuk memudahkan akses pengguna [5].

2. Jurnal "Movie Recommender System Using Collaborative Filtering" oleh Meenu Gupta et al. membahas sistem rekomendasi film yang menggunakan teknik collaborative filtering, khususnya algoritma K-Nearest Neighbors (K-NN) dan cosine similarity, untuk meningkatkan akurasi rekomendasi dibandingkan dengan metode filtering berbasis konten tradisional. Sistem ini bertujuan untuk mengatasi tantangan dalam menemukan konten film yang diinginkan di antara banyak pilihan dengan menganalisis penilaian dan preferensi pengguna. Penelitian ini menekankan pentingnya kepuasan pengguna dalam sistem rekomendasi dan membandingkan berbagai metode filtering, termasuk pendekatan berbasis konten, kolaboratif, dan hibrida. Sistem yang diusulkan menggunakan teknik collaborative filtering berbasis item, memanfaatkan dataset dari MovieLens yang berisi jutaan penilaian dan informasi film. Implementasinya melibatkan pra-pemrosesan data, perhitungan kesamaan, dan menghasilkan daftar film yang direkomendasikan berdasarkan interaksi pengguna. Hasil penelitian menunjukkan bahwa pendekatan Item-based Collaborative Filtering lebih unggul dibandingkan dengan filtering berbasis konten tradisional dalam hal akurasi, presisi, recall, dan Mean Absolute Error (MAE). Sistem ini mencapai MAE sebesar 0.248, yang lebih rendah dibandingkan dengan metode lainnya. Kesimpulan dari studi ini adalah bahwa menggabungkan filtering berbasis konten dan kolaboratif dapat lebih meningkatkan akurasi rekomendasi, serta menyarankan perbaikan di masa depan dengan mengintegrasikan fitur tambahan ke dalam dataset [6]. 

## 2. Business Understanding

Pengembangan sistem rekomendasi film memiliki potensi besar dalam meningkatkan pengalaman pengguna, mengatasi overload informasi, dan mendorong penemuan konten yang relevan. Dalam era digital saat ini, jumlah film yang tersedia meningkat secara signifikan setiap tahun, membuat pengguna sering kesulitan menemukan film yang sesuai dengan preferensi mereka. Sistem rekomendasi mampu menyaring pilihan berdasarkan data historis dan karakteristik film, memberikan saran personal yang lebih relevan dan efisien.

Bagi pengguna, sistem rekomendasi ini membantu menghemat waktu dalam menemukan film yang sesuai dengan selera mereka. Bagi platform streaming dan penyedia konten, keberadaan sistem ini tidak hanya meningkatkan keterlibatan pengguna tetapi juga membantu mempertahankan pelanggan dengan menyediakan rekomendasi yang memuaskan. Dengan menggabungkan pendekatan content-based filtering dan collaborative filtering, sistem ini bertujuan untuk memberikan rekomendasi yang lebih akurat dan relevan, sekaligus mengatasi masalah seperti cold start dan data sparsity.

### Problem Statements

Berdasarkan latar belakang tersebut, masalah yang dapat diselesaikan dalam proyek ini adalah:
- Bagaimana membangun sistem rekomendasi film yang mengintegrasikan content-based filtering dan collaborative filtering untuk memberikan rekomendasi yang relevan dan akurat?
- Algoritma apa yang memberikan performa terbaik dalam menghasilkan rekomendasi berdasarkan karakteristik film dan preferensi pengguna?
- Bagaimana hasil analisis data dapat digunakan untuk memberikan wawasan dalam industri film?

### Goals

Tujuan dari proyek ini meliputi:
- Mengembangkan sistem rekomendasi film berbasis content-based filtering dan collaborative filtering.
- Membandingkan performa berbagai pendekatan dalam menghasilkan rekomendasi untuk menentukan kombinasi terbaik.
- Menghasilkan insight berbasis data yang mendukung dalam menambah wawasan dalam industri film.

### Solution Approach

#### 1. Analisis Data dan Preprocessing
- Analisis Data
Untuk memahami distribusi data dan hubungan antar fitur, seperti genre, sutradara, aktor dan lain sebegainya.

- Data Cleaning dan Encoding:
Membersihkan data dari nilai yang hilang atau duplikasi, serta melakukan encoding pada fitur seperti genre atau kategori film untuk mempersiapkan data bagi algoritma rekomendasi.

#### 2. Implementasi Model Content-Based Filtering
- Membuat profil pengguna berdasarkan atribut film yang telah mereka sukai (misalnya genre, aktor, sutradara).
- Menggunakan teknik TF-IDF untuk merepresentasikan atribut film dalam format vektor.
- Menghitung kesamaan antara film menggunakan metrik cosine similarity untuk memberikan rekomendasi.

#### 3. Implementasi Model Collaborative Filtering
- Pendekatan Berbasis Memori
Menggunakan metode seperti user-user similarity dan item-item similarity untuk menemukan pola dalam preferensi pengguna.
- Pendekatan Berbasis Model
Menggunakan teknik seperti matrix factorization dengan algoritma seperti RecommenderNet untuk menangkap hubungan kompleks antara pengguna dan film.

#### 4. Optimalisasi Model
- Menggunakan TF-IDF sebagai vectorizer
TF-IDF mengubah atribut berbasis teks (misalnya, sinopsis film, genre, aktor, sutradara) menjadi vektor numerik. Dengan representasi vektor ini,  dapat menghitung kesamaan antar film menggunakan metrik seperti cosine similarity.
- Menerapkan learning rate saat proses training
Learning rate merupakan parameter yang menentukan seberapa besar langkah pembaruan bobot model selama proses pelatihan. Nilai ini memengaruhi kecepatan dan stabilitas konvergensi model, di mana learning rate yang terlalu besar dapat menyebabkan pelatihan tidak stabil, sementara yang terlalu kecil dapat memperlambat proses pelatihan.
- Menerapkan batch size saat proses training
Batch size merupakan jumlah sampel data yang diproses sekaligus sebelum memperbarui bobot model selama pelatihan. Ukuran ini memengaruhi kecepatan pelatihan dan penggunaan memori, di mana batch kecil memberikan pembaruan yang lebih sering namun lebih lambat, sedangkan batch besar lebih efisien tetapi memerlukan memori lebih besar.
- Evaluasi Model
Menggunakan metrik root mean square error (RMSE) untuk mengevaluasi kualitas rekomendasi yang dihasilkan.

## 3. Data Understanding
### EDA - Deskripsi Variabel

| Jenis | Keterangan |
| ------ | ------ |
| Title | _The Movies Dataset_ |
| Source | [Kaggle](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset/data) |
| Maintainer | [Rounak Banik ⚡](https://www.kaggle.com/rounakbanik) |
| License | Data files © Original Authors |
| Visibility | Publik |
| Tags | _Movies and TV Shows_ |
| View | 1.87M |

Informasi Dataset ini berisi informasi sebagai berikut ini : 
- Dataset berupa CSV (Comma-Seperated Values).
- Dataset memiliki 7 file berbeda (credits.csv, keywords.csv, links.csv, links_small.csv, movies_metadata.csv, ratings.csv, ratings_small.csv)
- Masing-masing file dataset memiliki kolom yang berbeda.
- Terdapat beberapa missing value terutama pada movies_metadata.csv (yang digunakan sebagai dataset utama dalam project ini)

### Variable - variable pada dataset
Dataset ini terdiri dari beberapa file penting yang berisi informasi tentang film. Berikut adalah penjelasan lebih rinci mengenai masing-masing file:

- movies_metadata.csv: Ini adalah file metadata film utama yang mencakup informasi tentang 45.000 film yang terdapat dalam dataset MovieLens lengkap. File ini berisi berbagai fitur seperti poster film, backdrop, anggaran, pendapatan, tanggal rilis, bahasa, serta negara dan perusahaan produksi. Data ini sangat berguna bagi siapa saja yang tertarik untuk menganalisis atau memahami lebih dalam tentang film yang ada.
- keywords.csv: File ini berisi kata kunci plot untuk film-film yang ada dalam MovieLens. Data disajikan dalam bentuk objek JSON yang ter-string, yang memungkinkan pengguna untuk dengan mudah mengidentifikasi tema atau elemen penting dari masing-masing film berdasarkan kata kunci tersebut.
- credits.csv: File ini menyediakan informasi mengenai pemeran dan kru untuk semua film dalam dataset. Seperti keywords, data di sini juga disajikan dalam bentuk JSON yang telah diubah menjadi string, yang memudahkan untuk melihat siapa saja yang terlibat dalam produksi film tersebut, termasuk sutradara, produser, serta anggota cast lainnya.
- links.csv: Ini adalah file yang mencantumkan ID TMDB (The Movie Database) dan IMDB (Internet Movie Database) untuk semua film yang terdapat dalam dataset MovieLens. ID ini sangat penting jika Anda ingin menemukan informasi lebih lanjut mengenai film di platform luar atau untuk integrasi dengan sistem lain.
- links_small.csv: Merupakan versi kecil dari file links.csv, yang hanya mencakup ID TMDB dan IMDB dari subset yang lebih kecil yaitu 9.000 film dari keseluruhan dataset. Ini berguna untuk analisis yang lebih cepat dan ringan, khususnya saat bekerja dengan jumlah data yang lebih sedikit.
- ratings_small.csv: File ini berisi subset 100.000 rating yang diberikan oleh 700 pengguna untuk 9.000 film. Data ini memungkinkan analisis perilaku penonton, tren rating, serta membantu dalam pengembangan model rekomendasi film yang lebih baik.

Secara keseluruhan, kumpulan data ini memberikan gambaran komprehensif tentang dunia perfilman dan dapat digunakan dalam berbagai analisis, seperti studi tren film, pengembangan algoritma rekomendasi, atau penelitian akademis dalam bidang media dan komunikasi. 

### EDA

1. Top 10 Language by Movie

![image](https://github.com/user-attachments/assets/3cd4ac0b-0613-4ba0-8c21-76c545318d97)

Gambar 1. Top 10 Language by Movie

Pada gambar 1 terlihat top 10 dari bahasa teratas berdasarkan film, dimulai dari yang teratas adalah bahasa inggris hingga yang terakhir adalah bahasa thionghoa.

2. Top 10 Movie Spoken Language

![image](https://github.com/user-attachments/assets/7b1bd754-9aac-4346-b9f4-06b873b1879a)

Gambar 2. Top 10 Movie Spoken Language

Pada gambar 2 terlihat top 10 dari bahasa teratas yang digunakan dalam film. dimulai dari yang teratas adalah bahasa inggris hingga yang terakhir adalah bahasa portugis.

3. Top 10 Genre Movie

![image](https://github.com/user-attachments/assets/8708519c-3175-48c5-a7b6-714d615f16aa)

Gambar 3. Top 10 Genre Movie

Pada gambar 3 terlihat top 10 dari genre teratas yang terdapat pada film, dimulai dari yang teratas adalah genre drama hingga yang terakhir adalah genre science fiction.

4. Top 10 Movie Production Countries

![image](https://github.com/user-attachments/assets/87127082-2d62-45e8-b2e0-466cc8d4b64c)

Gambar 4. Top 10 Movie Production Countries

Pada gambar 4 terlihat top 10 dari negara produksi pada film, dimulai dari yang teratas adalah Negara Amerika hingga yang terakhir adalah Negara India.

5. Top 10 Movie Production Companies

![image](https://github.com/user-attachments/assets/2ebb569e-b979-49cc-9862-46c6b15c0fee)

Gambar 5. Top 10 Movie Production Companies

Pada gambar 5 terlihat top 10 dari perusahaan produksi pada film, dimulai dari yang teratas adalah Warner Bros hingga yang terakhir adalah United Artists.

6. Top 10 Movie by Popular

![image](https://github.com/user-attachments/assets/b77153fd-b62f-4208-b72d-288cf70bc330)

Gambar 6. Top 10 Movie by Popular

Pada gambar 6 terlihat top 10 movie dari kepopuleran berdasarkan vote, dimulai dari yang teratas adalah Inception hingga yang terakhir adalah The Hunger Game.

7. WordCloud Graph Movie Overview

![image](https://github.com/user-attachments/assets/57e39b98-011a-47b7-a888-3b2765790f3c)

Gambar 7. WordCloud Graph Movie Overview

Pada gambar 7 terlihat word cloud dari overview pada dataset, dapat dilihat terdapat kata-kata yang sering muncul dan memiliki ukuran lebih besar dari yang lainnya.

8. WordCloud Graph Movie Tagline

![image](https://github.com/user-attachments/assets/feb256a5-8157-43d4-b742-6eef00712523)

Gambar 8. Wordcloud graph movie tagline

Pada gambar 8 terlihat word cloud dari tagline pada dataset, dapat dilihat terdapat kata-kata yang sering muncul dan memiliki ukuran lebih besar dari yang lainnya.

9. Top 10 Budget Movie Making

![image](https://github.com/user-attachments/assets/09429fc3-cf37-4fda-8c21-0e371ffe88e7)

gambar 9. top 10 budget movie making

pada gambar 9 terlihat top 10 movie dengan budget terbesar yang diantaranya yang paling atas terdapat Pirates of The Caribian dan yang paling bawah adalah Captain Amerika: Civil War.

10. Top 10 Revenue Movie

![image](https://github.com/user-attachments/assets/65aa24db-bd9c-4656-8db4-2e49aedd761f)

gambar 10. top 10 revenue movie

pada gambar 10 terlihat top 10 movie dengan pendapatan terbesar yang diantaranya yang paling atas terdapat Avatar dan yang paling bawah adalah Beauty and the Beast.

## 4. Data Preparation



## 5. Modeling



## 6. Evaluation


## Kesimpulan



## Kesimpulan Dampak Model Terhadap Business Understanding



## Daftar Pustaka

1. unairnews. (2023, May 8). Systematic Literature Review pada Sistem Rekomendasi Film untuk Layanan Streaming - Universitas Airlangga Official Website. Universitas Airlangga Official Website. https://unair.ac.id/systematic-literature-review-pada-sistem-rekomendasi-film-untuk-layanan-streaming/
2. Salim, E., Pragantha, J., & Lauro, M. (n.d.). Perancangan Sistem Rekomendasi Film menggunakan metode Content- based Filtering. https://lintar.untar.ac.id/repository/penelitian/buktipenelitian_10390001_7A281222103549.pdf
3. Liang, S., & Susanto, J. (2022). Rancang Bangun Aplikasi Rekomendasi Restoran Menggunakan Metode K-Nearest Neighbors dan Content-Based Filtering. JURIKOM (Jurnal Riset Komputer), 9(1), 8–8 https://doi.org/10.30865/jurikom.v9i1.3816
4. MESIN REKOMENDASI FILM MENGGUNAKAN METODE KEMIRIPAN GENRE BERBASIS COLLABORATIVE FILTERING. (n.d.). https://repository.its.ac.id/42018/1/2215206701-Master-Thesis.pdf
5. Pradeep, N., Rao Mangalore, K., Rajpal, B., Prasad, N., & Shastri, R. (2020). Content Based Movie Recommendation System. https://www.riejournal.com/article_121501_a3717e6cf19a1845e350acb9148751ee.pdf
6. Gupta, M., Thakkar, A., Aashish, Gupta, V., & Rathore, D. P. S. (2020). Movie Recommender System Using Collaborative Filtering. 2020 International Conference on Electronics and Sustainable Communication Systems (ICESC), 415–420. https://doi.org/10.1109/icesc48915.2020.9155879
7. 

‌






