# Proyek Kedua Machine Learning Terapan | Movie Recommendation Using Content Based Filltering and Collaborative Filltering

###### Disusun oleh : Ida Bagus Agung Bajerapany

Proyek ini membangun model yang dapat memberikan rekomendasi film

## 1. Project Domain

Sistem rekomendasi film merupakan alat penting dalam membantu pengguna menemukan konten yang sesuai dengan preferensi mereka di tengah banyaknya pilihan yang tersedia. Dengan perkembangan teknologi digital, jumlah film yang dirilis setiap tahun meningkat pesat, sehingga memunculkan tantangan bagi pengguna untuk memilih film yang tepat. Sistem rekomendasi berfungsi untuk memberikan saran berdasarkan data interaksi pengguna sebelumnya dan karakteristik film, sehingga pengguna dapat dengan mudah menemukan film yang mungkin mereka sukai. Terdapat dua pendekatan utama dalam pengembangan sistem rekomendasi: content-based filtering dan collaborative filtering.

Content-based filtering merekomendasikan film berdasarkan kemiripan atribut dari film yang sudah disukai pengguna sebelumnya, seperti genre, sutradara, atau aktor [1] [2]. Metode ini memungkinkan sistem untuk memberikan rekomendasi yang relevan dengan minat pengguna tanpa memerlukan data dari pengguna lain. Di sisi lain, collaborative filtering memanfaatkan data interaksi dari banyak pengguna untuk menemukan pola dan hubungan antar film, sehingga dapat merekomendasikan film berdasarkan kesamaan preferensi di antara pengguna [3]. Pendekatan ini sangat efektif dalam mengatasi masalah data sparsity dan cold start yang sering dihadapi oleh sistem rekomendasi. Kombinasi kedua metode ini dalam sistem rekomendasi film dapat meningkatkan akurasi dan relevansi rekomendasi yang diberikan kepada pengguna. Penelitian sebelumnya menunjukkan bahwa penggunaan metode hybrid, yang menggabungkan content-based dan collaborative filtering, dapat memberikan hasil yang lebih baik dibandingkan dengan menggunakan salah satu metode secara terpisah [4]. Dengan demikian, pengembangan sistem rekomendasi film yang mengintegrasikan kedua pendekatan ini tidak hanya akan meningkatkan pengalaman pengguna tetapi juga akan memperluas jangkauan konten yang dapat ditemukan oleh pengguna.

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
| Source | [LINK DATASET](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset/data) |
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
- links.csv: Ini adalah file yang mencantumkan ID TMDB (The Movie Database) dan IMDB (Internet Movie Database) untuk semua film yang terdapat dalam dataset MovieLens. ID ini sangat penting jika ingin menemukan informasi lebih lanjut mengenai film di platform luar atau untuk integrasi dengan sistem lain.
- links_small.csv: Merupakan versi kecil dari file links.csv, yang hanya mencakup ID TMDB dan IMDB dari subset yang lebih kecil yaitu 9.000 film dari keseluruhan dataset. Ini berguna untuk analisis yang lebih cepat dan ringan, khususnya saat bekerja dengan jumlah data yang lebih sedikit.
- ratings_small.csv: File ini berisi subset 100.000 rating yang diberikan oleh 700 pengguna untuk 9.000 film. Data ini memungkinkan analisis perilaku penonton, tren rating, serta membantu dalam pengembangan model rekomendasi film yang lebih baik.

![image](https://github.com/user-attachments/assets/73f4eb17-7d58-4030-8e89-5f6e488105dd)

![image](https://github.com/user-attachments/assets/6b8a4c2f-6ab1-4c41-b91e-394d4ceda710)

Dapat dilihat pada gambar diatas, masing-masing tabel yang ada pada dataset memiliki jumlah data dan baris seperti dibawah ini :
- Data Ratings
Data ratings terdiri dari 26.024.289 data dan memiliki 4 kolom yang terdiri dari 'userId' (Memuat ID dari user), 'movieId', 'rating', 'timestamp'. Berikut merupakan kondisi dari data ratings :

![image](https://github.com/user-attachments/assets/612548fb-f742-4c68-a78e-1f0d258168b2)

Dapat dilihat pada gambar diatas, tabel ratings sudah lengkap tidak memiliki data yang kosong dan tidak memiliki data yang duplikat.

- Data Links Small
Data links small terdiri dari 9125 data dan memiliki 3 kolom yang terdiri dari 'movieId', 'imdbId', 'tmdbId'. Berikut merupakan kondisi dari link small :

![image](https://github.com/user-attachments/assets/25e8722d-1a07-4d2d-8329-9bea6fcdcd45)

Dapat dilihat pada gambar diatas, tabel links small memiliki data yang kosong pada kolom tmdbid dan tidak memiliki data yang duplikat.

- Data Credits
Data credits terdiri dari 45.476 data dan memiliki 3 kolom yang terdiri dari 'cast', 'crew', 'id'. Berikut merupakan kondisi dari data credits :

![image](https://github.com/user-attachments/assets/e1f889fc-680d-4edf-ac79-86685684b22a)

Dapat dilihat pada gambar diatas, tabel credits tidak memiliki data yang kosong dan memiliki 37 data duplikat.

- Data Keywords
Data keywords terdiri dari 46.419 data dan memiliki 2 kolom yang terdiri dari 'id', 'keywords'. Berikut merupakan kondisi dari data keywords :

![image](https://github.com/user-attachments/assets/64a0ab71-52d1-48b0-85cf-7603a60238d0)

Dapat dilihat pada gambar diatas, tabel keywords tidak memiliki data yang kosong dan memiliki 987 data yang duplikat.

- Data Metadata
Data metadata terdiri dari 45.466 data dan memiliki 24 kolom yang terdiri dari 'adult', 'belongs_to_collection', 'budget', 'genres', 'homepage', 'id', 'imdb_id', 'original_language', 'original_title', 'overview', 'popularity', 'poster_path', 'production_companies', 'production_countries', 'release_date', 'revenue', 'runtime', 'spoken_languages', 'status', 'tagline', 'title', 'video', 'vote_average', 'vote_count'. Berikut merupakan kondisi dari metadata :

![image](https://github.com/user-attachments/assets/02c5307d-10f6-4ad1-b956-2f261b50151e)
![image](https://github.com/user-attachments/assets/a3f98fa2-4091-4b9b-b5c6-74e8ba744363)

Dapat dilihat pada gambar diatas, tabel metadata memiliki data yang kosong pada hampir sebgian besar kolomnya seperti contoh pada kolom popularity (5 data), pada kolom status (87 data) dan yang lainnya, dan memiliki 13 data duplikat.
 
- Data Ratings Small
Data ratings small terdiri dari 100.004 data dan memiliki 4 kolom yang terdiri dari 'userId', 'movieId', 'rating', 'timestamp'. Berikut merupakan kondisi dari ratings small :

![image](https://github.com/user-attachments/assets/fc7950b7-6bcc-42a6-b530-c67d71cd8e79)

Dapat dilihat pada gambar diatas, tabel ratings small sudah lengkap tidak memiliki data yang kosong dan tidak memiliki data yang duplikat.
 
- Data Links
Data links terdiri dari 45.843 data dan memiliki 3 kolom yang terdiri dari 'movieId', 'imdbId', 'tmdbId'. Berikut merupakan kondisi dari data links :

![image](https://github.com/user-attachments/assets/a00d8154-d659-4ee2-b010-57c29037b397)

Dapat dilihat pada gambar diatas, tabel links memiliki 219 data yang kosong dan tidak memiliki data duplikat.

Setiap file dataset memiliki fiturnya masing-masing, berikut merupakan penjelasan dari masing-masing fitur yang ada pada dataset :

1. Ratings / Ratings Small
- userId: Merupakan identitas unik setiap pengguna yang terdaftar dalam sistem. ID ini digunakan untuk melacak aktivitas pengguna, seperti memberikan rating terhadap film tertentu.
- movieId: Identitas unik yang diberikan untuk setiap film dalam dataset. Kolom ini dapat digunakan untuk menghubungkan data antar tabel seperti Metadata, Keywords, atau Credits.
- rating: Nilai atau skor yang diberikan pengguna kepada film. Biasanya, rating diberikan dalam skala 1–5, dengan 1 menunjukkan rating terendah (sangat tidak disukai) dan 5 menunjukkan rating tertinggi (sangat disukai).
- timestamp: Waktu ketika pengguna memberikan rating, dalam format UNIX timestamp. Timestamp ini dapat dikonversi ke format tanggal dan waktu standar untuk analisis lebih lanjut, seperti melihat tren penilaian berdasarkan waktu.

2. Links / Links Small
- movieId: ID unik untuk setiap film, sama dengan kolom movieId di tabel Ratings. Kolom ini berfungsi sebagai penghubung antar tabel.
- imdbId: ID unik dari IMDb (Internet Movie Database), yang merupakan salah satu platform film terbesar di dunia. Kolom ini dapat digunakan untuk mengambil data tambahan dari IMDb.
- tmdbId: ID unik dari TMDB (The Movie Database), sebuah platform komunitas berbasis data film. TMDB menyediakan API yang memungkinkan pengembang untuk mengambil informasi lebih detail, seperti poster film atau data box office.

3. Credits
- cast: Menyimpan informasi tentang daftar pemeran dalam film, seperti nama aktor atau aktris. Data ini disimpan dalam format JSON, sehingga perlu diproses lebih lanjut untuk analisis, misalnya menentukan aktor yang paling sering bermain dalam film tertentu.
- crew: Menyimpan informasi tentang anggota kru yang terlibat dalam produksi film. Kolom ini mencakup informasi tentang sutradara, produser, penulis naskah, dan lainnya, juga dalam format JSON.
- id: ID unik yang merujuk pada film tertentu, yang dapat digunakan untuk menghubungkan tabel Credits dengan tabel lainnya seperti Metadata atau Ratings.

4. Keywords
- id: ID unik untuk setiap film, digunakan untuk menghubungkan data dengan tabel lainnya.
- keywords: Menyimpan daftar kata kunci atau istilah yang relevan dengan film, dalam format JSON. Kata kunci ini mencerminkan tema atau elemen penting dari film tersebut, seperti “perjalanan waktu” atau “perang luar angkasa”. Kolom ini berguna untuk membangun sistem rekomendasi berbasis konten.

5. Meta Data
- adult: Indikator apakah film ditujukan hanya untuk penonton dewasa. Bernilai True jika film memiliki konten dewasa, dan False jika tidak.
- belongs_to_collection: Menyimpan informasi tentang koleksi atau seri film, jika film tersebut merupakan bagian dari suatu waralaba (franchise). Data ini disimpan dalam format JSON.
- budget: Total anggaran produksi film dalam satuan USD. Data ini sering digunakan untuk analisis korelasi antara anggaran dan pendapatan.
- genres: Daftar genre film (misalnya, Action, Comedy, Drama), disimpan dalam format JSON. Genre membantu dalam pengelompokkan film berdasarkan kategori tertentu.
- homepage: URL yang mengarah ke halaman resmi film. Berguna untuk memberikan referensi tambahan terkait promosi film.
- id: ID unik untuk setiap film, yang berfungsi sebagai kunci utama untuk menghubungkan data antar tabel.
- imdb_id: ID film di database IMDb. Berguna untuk mengambil detail tambahan menggunakan API IMDb.
- original_language: Kode bahasa asli film, seperti en untuk Bahasa Inggris atau fr untuk Bahasa Prancis.
- original_title: Judul asli film sebelum diterjemahkan atau diadaptasi.
- overview: Ringkasan singkat atau sinopsis film, memberikan gambaran umum tentang alur cerita film.
- popularity: Skor yang mencerminkan tingkat popularitas film berdasarkan berbagai metrik, seperti jumlah vote dan interaksi pengguna.
- poster_path: Path atau URL menuju poster resmi film. Poster ini dapat digunakan untuk membuat antarmuka visual, seperti aplikasi rekomendasi film.
- production_companies: Informasi tentang perusahaan produksi yang terlibat dalam pembuatan film, dalam format JSON.
- production_countries: Daftar negara tempat produksi film dilakukan, dalam format JSON.
- release_date: Tanggal rilis resmi film.
- revenue: Pendapatan yang dihasilkan oleh film (dalam USD), biasanya diukur berdasarkan box office global.
- runtime: Durasi film dalam menit.
- spoken_languages: Bahasa yang digunakan dalam dialog film, dalam format JSON.
- status: Status rilis film, misalnya “Released” (sudah dirilis) atau “Post Production” (masih dalam tahap pasca-produksi).
- tagline: Slogan atau kalimat pendek yang menggambarkan film.
- title: Judul resmi film yang digunakan untuk promosi.
- video: Indikator apakah ada video promosi terkait film tersebut (True/False).
- vote_average: Skor rata-rata berdasarkan voting pengguna, sering digunakan sebagai indikator kualitas film.
- vote_count: Jumlah total voting yang diberikan pengguna.

Secara keseluruhan, kumpulan data ini memberikan gambaran komprehensif tentang dunia perfilman dan dapat digunakan dalam berbagai analisis, seperti studi tren film, pengembangan algoritma rekomendasi, atau penelitian akademis dalam bidang media dan komunikasi. Data yang kosong maupun duplikat akan dibersihkan pada bagian pre-processing sebelum modal dibentuk untuk menghasilkan model yang memiliki rekomendasi baik.

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
Berikut merupakan data preparation yang diterapkan pada project ini :

1. Perubahan Tipe Data : Perubahan tipe data ini dilakukan untuk memudahkan analisis dan melakukan modeling, seperti pada projek ini terdapat tipe data yang kurang cocok seperti kolom release date dan release year yang sebelumnya bertipe data object dirubah menjadi tipe data datetime, untuk memperbaiki kualitas dataset sebelum dilakukan modeling.

2. Penangan Duplikasi Data : Selanjutnya melakukan pengecekan duplikasi data dengan fungsi duplicated(). pemeriksaan ini dilakukan untuk mengetahui apakah terdapat duplikasi pada kolom yang ada pada dataset, langkah penanganan ini adalah dengan menghapus duplikasi data yang terdapat pada kolom untuk menjaga performa dataset. Dalam kasus ini, hasil pemeriksaan menunjukan terdapat duplikasi data pada kolom kredit, keyword dan metadata yang akan dihapus sebelum membuat model rekomendasi.

3. Penanganan Missing Values : Memastikan tidak ada data yang hilang (missing values) pada dataset. Pemeriksaan dilakukan untuk mengetahui apakah terdapat kolom atau baris dengan nilai kosong. Jika terdapat missing values, langkah penanganan seperti mengisi dengan Nan atau value unknown perlu diterapkan untuk menjaga integritas dataset. Dalam kasus ini, hasil pemeriksaan menunjukkan  ada data yang hilang, sehingga diperlukan langkah penanganan lebih lanjut untuk missing values. pada proyek ini missing value terdapat pada tabel link, link small dan metadata.

4. Feature MinMaxscaler : Feature ini digunakan untuk menormalkan kolom dalam dataset yang termasuk dalam daftar binned_features menggunakan MinMaxScaler. Dengan cara ini, nilai-nilai dalam kolom tersebut diubah ke dalam rentang 0 hingga 1, yang membantu memastikan bahwa semua fitur memiliki skala yang sama. Hal ini penting untuk mencegah fitur dengan rentang nilai lebih besar mendominasi model dan untuk meningkatkan efisiensi serta stabilitas pelatihan model, terutama untuk algoritma yang sensitif terhadap skala data seperti sistem rekomendasi ini.

5. Dummies : Fungsi dummies digunakan untuk mengonversi data kategorikal menjadi representasi numerik dalam bentuk variabel dummy (atau one-hot encoding). Dalam proyek ini, pd.get_dummies diterapkan pada kolom original_language dari dataset movie_data, menghasilkan sebuah DataFrame baru bernama languages, di mana setiap kolom mewakili satu bahasa unik dari kolom asli. Nilainya berupa 1 jika film tersebut menggunakan bahasa tertentu, dan 0 jika tidak. Representasi ini memungkinkan algoritma pembelajaran mesin untuk memahami data kategorikal tanpa memperkenalkan urutan atau skala numerik yang tidak sesuai, sehingga dapat digunakan dalam model prediktif dengan lebih akurat.

6. Tokenizer dengan nltk : Fungsi tokenizer digunakan untuk memproses teks dan menghasilkan daftar kata dasar (stemming) yang sudah dibersihkan dari kata-kata yang tidak relevan. Fungsi ini pertama-tama membagi teks menjadi token-token menggunakan nltk.word_tokenize, kemudian menghapus kata-kata yang termasuk dalam daftar stop words bahasa Inggris, serta hanya mempertahankan token yang berupa alfabet dan memiliki panjang lebih dari satu karakter. Selanjutnya, setiap token yang tersisa diproses dengan Porter Stemmer untuk mengubahnya menjadi bentuk dasar (stem), yang berguna dalam analisis teks dan pemodelan machine learning agar model dapat fokus pada bentuk dasar kata dan bukan variasi kata yang berbeda.

7. TF-IDF : TF-IDF digunakan untuk memproses teks yang terdapat dalam kolom overview, tagline, dan keywords pada dataset movie_data dan menggabungkannya menjadi satu kolom baru bernama text. Setelah itu, TF-IDF Vectorizer diterapkan untuk mengubah teks menjadi representasi numerik menggunakan teknik Term Frequency-Inverse Document Frequency (TF-IDF), yang menilai pentingnya kata dalam setiap dokumen. Konfigurasi TfidfVectorizer seperti min_df, max_df, dan ngram_range diatur untuk memilih fitur yang relevan, dengan tokenisasi yang disesuaikan menggunakan fungsi tokenizer yang telah didefinisikan sebelumnya. Hasilnya adalah matriks fitur dari teks yang diubah menjadi DataFrame tfidf_df, yang berfungsi untuk merepresentasikan teks dalam format yang bisa digunakan untuk analisis lebih lanjut atau model pembelajaran mesin.

8. CountVectorizer : CountVectorizer digunakan untuk mengubah data teks menjadi representasi numerik dalam bentuk matriks fitur, di mana setiap kolom mewakili sebuah kata unik dari teks, dan setiap baris mewakili dokumen (atau item data) yang berisi jumlah kemunculan kata tersebut. Dalam konteks proyek ini, CountVectorizer diterapkan pada kolom "CC" dari dataset movie_data, dengan parameter lowercase=False untuk mempertahankan huruf besar-kecil dan min_df=4 untuk hanya menyertakan kata-kata yang muncul setidaknya empat kali di seluruh dataset. Proses ini menghasilkan matriks sparse yang diubah menjadi DataFrame (cast_df) untuk kemudahan analisis, dengan kata-kata unik sebagai kolom dan jumlah kemunculan kata dalam setiap dokumen sebagai nilai, memungkinkan data teks digunakan sebagai input dalam algoritma pembelajaran mesin atau analisis lebih lanjut.

9. Merge data dengan Concat : Fungsi concat digunakan untuk menggabungkan beberapa DataFrame atau Series menjadi satu DataFrame baru, baik secara horizontal (kolom) maupun vertikal (baris). Dalam proyek ini, pd.concat menggabungkan DataFrame languages, genres_df, cast_df, writing_df, dan tfidf_df secara horizontal (dengan axis=1), menghasilkan DataFrame baru bernama train. Gabungan ini mengintegrasikan berbagai fitur seperti bahasa, genre, cast, penulis, dan hasil transformasi TF-IDF ke dalam satu struktur data, sehingga dapat digunakan sebagai matriks fitur lengkap untuk melatih model pembelajaran mesin. Setelah penggabungan, tipe data seluruh nilai dalam DataFrame diubah menjadi np.int8 untuk mengurangi penggunaan memori.

10. Encoding : Encoding digunakan untuk mengubah userId dalam dataset rating_small menjadi daftar unik yang berisi semua ID pengguna tanpa duplikasi. Setelah itu, ID pengguna tersebut di-encode menjadi nilai numerik dengan membuat kamus user_to_user_encoded yang memetakan setiap userId ke angka unik. Kamus kedua, user_encoded_to_user, dibuat untuk memetakan angka yang sudah di-encode kembali ke ID pengguna asli. Proses ini penting dalam pemrosesan data untuk sistem rekomendasi, karena banyak algoritma machine learning yang memerlukan input numerik dan tidak dapat langsung menangani ID berbasis string.

11. Split Dataset : Dataset dibagi menjadi dua subset:
   - Data latih (training set): Digunakan untuk melatih model agar dapat mengenali pola dalam data.
   - Data uji (test set): Digunakan untuk mengevaluasi performa model pada data baru yang belum pernah dilihat sebelumnya.
Pembagian dilakukan dengan rasio 80:20, di mana 80% digunakan untuk pelatihan dan 20% untuk pengujian. Random state juga digunakan untuk memastikan hasil pembagian dataset konsisten di setiap eksekusi.

## 5. Modeling

### 1. Content Based Filltering

Algoritma Content-Based Filtering yang digunakan dalam proyek ini bekerja dengan membandingkan kesamaan antar film berdasarkan fitur-fitur yang relevan, seperti deskripsi, genre, atau atribut lainnya yang telah diubah menjadi representasi numerik. Langkah pertama adalah menghitung Cosine Similarity antar film dengan menggunakan matriks fitur dari data pelatihan. Selanjutnya, fungsi get_recommendations digunakan untuk mencari film yang paling mirip dengan film yang diberikan sebagai input (title). Fungsi ini mengidentifikasi indeks film yang sesuai dengan judul yang dimasukkan, menghitung skor kesamaan dengan semua film lainnya, dan menyusun daftar film yang paling mirip berdasarkan skor tersebut.

Algoritma Content-Based Filtering dimulai dengan mengekstrak fitur relevan dari dataset, seperti deskripsi, genre, dan bahasa, yang diubah menjadi representasi numerik menggunakan teknik seperti CountVectorizer atau TF-IDF. Fitur-fitur ini kemudian digabungkan dalam sebuah matriks fitur, di mana setiap baris mewakili satu film sementara setiap kolom mewakili fitur tertentu, menjadi dasar untuk menghitung kesamaan antar film. Kesamaan dihitung dengan menggunakan Cosine Similarity, yang mengukur sudut antara dua vektor, dengan nilai berkisar antara 0 (tidak ada kesamaan) hingga 1 (identik). Setelah itu, algoritma mencari indeks film sesuai dengan judul yang diberikan agar dapat mengakses skor kesamaan film tersebut dengan film lainnya, yang kemudian diurutkan secara menurun untuk menemukan film paling relevan. Selanjutnya, algoritma memilih sejumlah film teratas untuk direkomendasikan, mengambil data tambahan seperti judul, genre, dan ID IMDb. Hasil rekomendasi akhirnya disusun dalam bentuk tabel atau DataFrame serta dievaluasi akurasinya, contohnya dengan membandingkan genre film input dengan genre film dalam daftar rekomendasi untuk menghitung persentase presisi. Dengan demikian, algoritma ini mampu memberikan rekomendasi film yang relevan berdasarkan atribut yang mirip dengan film input.

Kelebihan dari pendekatan ini adalah sistem dapat memberikan rekomendasi berdasarkan atribut yang relevan dengan film yang disukai pengguna, tanpa memerlukan data interaksi dari pengguna lain. Ini memungkinkan sistem untuk bekerja bahkan untuk pengguna baru yang belum memberikan interaksi. Selain itu, content-based filtering memberikan rekomendasi yang lebih personal karena didasarkan pada kesamaan fitur dari film itu sendiri. Namun, kekurangannya adalah pendekatan ini hanya mengandalkan atribut yang ada, sehingga dapat menghasilkan rekomendasi yang terbatas atau kurang variatif, terutama jika film yang memiliki kesamaan fitur terbatas. Selain itu, content-based filtering sering kali mengalami masalah ketika ada film dengan deskripsi yang kurang lengkap atau tidak mencolok, sehingga mengurangi kualitas rekomendasi.

Berikut merupakan top 15 rekomendasi menggunakan content based filltering dengan film Dead Man Walking bergenre drama :

![image](https://github.com/user-attachments/assets/f23bbca5-db3a-406c-b31c-56c366c669f9)

### 2. Collaborative Filltering

Collaborative Filtering merupakan metode rekomendasi yang bekerja dengan menganalisis pola interaksi antara pengguna dan item, seperti film, untuk memberikan rekomendasi yang sesuai dengan preferensi pengguna. Pada proyek ini, langkah awal adalah melakukan encoding terhadap userId dan movieId, sehingga setiap pengguna dan film direpresentasikan dalam bentuk angka unik. Selanjutnya, data dibagi menjadi dua set: data pelatihan (80%) dan data validasi (20%). Model yang digunakan, RecommenderNet, dirancang dengan pendekatan embedding, yang memetakan setiap pengguna dan film ke dalam ruang vektor berdimensi tertentu (ditentukan oleh parameter embedding_size). Embedding ini merepresentasikan karakteristik pengguna dan film dalam bentuk vektor numerik. Model memiliki empat komponen utama: embedding untuk pengguna (user_embedding) dan film (movie_embedding), serta bias untuk pengguna (user_bias) dan film (movie_bias). Dalam proses prediksi, model menghitung produk titik (dot product) antara vektor pengguna dan film, kemudian menambahkan bias untuk mendapatkan nilai prediksi rating. Nilai ini dihitung menggunakan fungsi aktivasi sigmoid, yang menghasilkan output dalam rentang 0 hingga 1. Model dilatih menggunakan algoritma optimasi Adam dengan tingkat pembelajaran (learning_rate) sebesar 0.001, dan fungsi kehilangan yang digunakan adalah Binary Crossentropy untuk meminimalkan kesalahan prediksi. Selama pelatihan, performa model dievaluasi menggunakan metrik Root Mean Squared Error (RMSE), yang mengukur seberapa baik model memprediksi rating.

Parameter yang digunakan dalam algoritma Collaborative Filtering pada proyek ini diantaranya Jumlah Pengguna (num_users) merujuk pada total pengguna unik dari proses encoding kolom userId, yang menentukan dimensi untuk embedding pengguna. Jumlah Film (num_movies) adalah total film unik dari encoding kolom movieId, menentukan dimensi untuk embedding film. Ukuran Embedding (embedding_size) ditetapkan pada 50, mewakili pengguna dan film dalam vektor berdimensi 50. Tingkat Pembelajaran (learning_rate) diatur pada 0.001, mempengaruhi kecepatan pembaruan bobot model. Fungsi Kehilangan (loss) menggunakan Binary Crossentropy untuk menghitung kesalahan antara rating prediksi dan aktual. Metrik Evaluasi (metrics) menggunakan Root Mean Squared Error (RMSE) untuk menilai performa model. Ukuran Batch (batch_size) ditetapkan pada 8, memastikan efisiensi pelatihan pada dataset kecil. Jumlah Epoch (epochs) adalah 50, cukup untuk belajar tanpa overfitting. Regularisasi (embeddings_regularizer) menggunakan L2 dengan nilai penalti 1×10^-6 untuk mengurangi risiko overfitting, dan Fungsi Aktivasi (tf.nn.sigmoid) membatasi prediksi antara 0 dan 1 untuk menghasilkan probabilitas. Semua parameter bekerja sama untuk mengoptimalkan pelatihan dan menghasilkan rekomendasi yang akurat berdasarkan interaksi antara pengguna dan film.

Kelebihan dari pendekatan Collaborative Filtering ini adalah model dapat memberikan rekomendasi yang sangat personal dengan memanfaatkan data interaksi pengguna, tanpa membutuhkan informasi tambahan tentang film, seperti deskripsi atau genre. Pendekatan ini juga mampu menangani masalah sparsity (kurangnya data) dengan mengandalkan kesamaan antar pengguna atau film. Namun, ada beberapa kekurangan, seperti masalah cold start, di mana model kesulitan memberikan rekomendasi untuk pengguna atau film baru yang tidak memiliki cukup interaksi sebelumnya. Selain itu, Collaborative Filtering juga rentan terhadap masalah skala besar, di mana model mungkin membutuhkan waktu dan sumber daya yang banyak untuk memproses data dengan jutaan pengguna dan film.

Berikut merupakan top 10 rekomendasi menggunakan collaborative filltering :

![image](https://github.com/user-attachments/assets/9bb8b69c-6871-4190-afe4-8d2b2b1c1e11)


## 6. Evaluation

Pada proyek ini, memiliki dua evaluasi dari content based filltering dan collaborative filltering, berikut merupakan penjelasannya :

1. Content Based Filltering
Model Content Based Filltering menggunakan metrik precision untuk mengevaluasi kinerja model yang dihasilkan. berikut merupakan rumus metrik evaluasi dari model :

![image](https://github.com/user-attachments/assets/36621cd6-36dc-48e9-917a-8667ad2a70f9)

dengan menerapkan rumus tersebut dapat melakukan evaluasi precision dengan membagi hasil dari rekomendasi yang relevant dibagi dengan jumlah rekomendasi yang diberikan sehingga mendapatkan evaluasi berbentuk persentase keberhasilan rekomendasi yang diukur dengan precision. berikut merupakan hasil dari evaluasi model :

![image](https://github.com/user-attachments/assets/8d2d8aef-ede9-4787-afbc-ce1344e126ea)

Hasil perhitungan diatas didapat dari jumlah genre yang benar dalam hasil rekomendasi pada film "Dead Man Walking" yang memiliki genre drama, dan hasil rekomendasi yang didapat 14 rekomendasi memiliki genre drama dan hanya satu rekomendasi yang tidak memiliki genre drama, jadi hasil yang didapat precision pada model collaborative filltering ini adalah 93.33%.

![image](https://github.com/user-attachments/assets/e37637df-0d02-46fd-a71d-5e39f1678071)

![image](https://github.com/user-attachments/assets/b49ac144-c42f-4f6a-b243-22ee4835d6be)

2. Collaborative Filltering
Model Collaborative Filltering menggunakan metrik RMSE (Root Mean Square Error) untuk mengevaluasi kinerja model yang dihasilkan. RMSE merupakan salah satu metode yang paling umum digunakan untuk mengukur kesalahan dalam model prediktif, khususnya ketika berurusan dengan data kuantitatif. Dengan menggunakan RMSE,  dapat secara efektif menilai seberapa baik model dalam memprediksi nilai-nilai yang diharapkan berdasarkan data yang telah diamati sebelumnya. Berikut merupakan rumus metrik evaluasi dari model :

![image](https://github.com/user-attachments/assets/919ef4e0-d75f-45e7-a10f-2ddd8238b48b)

Keterangan :
- RMSE = nilai root mean square error
- y = nilai hasil observasi
- ŷ = nilai hasil prediksi
- i = urutan data
- n = jumlah data

RMSE bekerja dengan cara menghitung nilai kesalahan antara prediksi yang dihasilkan model dan nilai observasi aktual. Proses perhitungannya dimulai dengan menghitung selisih kuadrat antara nilai prediksi dan nilai observasi, yang kemudian dijumlahkan dan dibagi dengan jumlah data. Akhirnya, hasil tersebut akan diambil akar kuadratnya. Nilai RMSE yang rendah mengindikasikan bahwa variasi yang dihasilkan oleh model prakiraan mendekati variasi yang terdapat dalam data observasi, yang berarti model tersebut memiliki akurasi yang baik.

Berikut ini adalah plot metrik RMSE setelah proses pelatihan model:

![image](https://github.com/user-attachments/assets/9ad9f1fc-6e95-4e9a-b2fb-c02f01404f7d)

Setelah melakukan pelatihan model, dapat dilihat plot metrik RMSE yang menunjukkan kinerja model dalam bentuk grafik. Dari plot tersebut, dapat terlihat bahwa model menghasilkan nilai RMSE sebesar 0.1809 pada train dan 0.2052 pada validation. Angka ini menunjukkan bahwa kinerja model sudah cukup baik, karena nilai RMSE yang lebih rendah menunjukkan kesalahan yang lebih kecil dalam prediksi.

## Kesimpulan

Kesimpulan dari analisis ini menunjukkan bahwa model yang menggabungkan content-based filtering dan collaborative filtering berhasil memberikan hasil yang relevan dan akurat dalam sistem rekomendasi film. Melalui analisis dan pelatihan model, diperoleh hasil yang menunjukkan performa yang memadai. Berdasarkan plot metrik RMSE, model menghasilkan nilai RMSE sebesar 0.1809 pada data latih dan 0.2052 pada data validasi, yang menunjukkan bahwa kesalahan prediksi cukup rendah. Ini menandakan bahwa model telah belajar dengan baik dalam memprediksi preferensi pengguna dan karakteristik film. Selain itu, pendekatan ini dapat memberikan wawasan yang berguna dalam industri film dengan mengidentifikasi pola preferensi pengguna dan film yang sering dipilih, serta meningkatkan pengalaman pengguna melalui rekomendasi yang lebih personal dan relevan. Evaluasi model juga menunjukkan hasil yang sangat baik pada content-based filtering, dengan nilai precision sebesar 93.33%, yang menandakan bahwa model mampu memberikan rekomendasi yang sangat akurat sesuai dengan preferensi pengguna. Angka precision yang tinggi ini memperkuat efektivitas pendekatan content-based filtering dalam menyarankan film yang relevan berdasarkan kesamaan fitur atau atribut film. Gabungan kedua metode ini memungkinkan model untuk memanfaatkan kekuatan masing-masing, menghasilkan rekomendasi yang lebih baik dan lebih sesuai dengan kebutuhan pengguna.

## Kesimpulan Dampak Model Terhadap Business Understanding

Pengembangan dan penerapan model sistem rekomendasi film yang mengintegrasikan content-based filtering dan collaborative filtering memberikan dampak signifikan terhadap pemahaman bisnis dalam industri hiburan, khususnya platform streaming film. Sistem rekomendasi ini mampu meningkatkan pengalaman pengguna dengan menyarankan film yang relevan dan sesuai dengan preferensi individu, mengatasi tantangan overload informasi, dan mempermudah penemuan konten yang lebih personal. Ini akan menghemat waktu pengguna dalam menemukan film yang disukai, yang pada akhirnya meningkatkan tingkat keterlibatan dan kepuasan pelanggan. Bagi penyedia platform streaming, sistem rekomendasi ini memberikan keuntungan tambahan berupa retensi pengguna yang lebih tinggi dan peningkatan loyalitas pelanggan, karena rekomendasi yang tepat meningkatkan pengalaman pengguna secara keseluruhan. Selain itu, dengan menggabungkan dua pendekatan, yaitu content-based filtering yang mengandalkan atribut film dan collaborative filtering yang mengidentifikasi pola preferensi pengguna, sistem ini lebih mampu mengatasi masalah seperti cold start dan data sparsity yang sering terjadi pada model rekomendasi. Dengan hasil analisis data dan pemilihan model terbaik melalui optimasi parameter seperti learning rate dan batch size, model ini dapat memberikan rekomendasi yang lebih akurat dan efisien. Hal ini tidak hanya bermanfaat bagi pengguna tetapi juga memberikan wawasan penting bagi industri film untuk memahami tren preferensi dan pola perilaku konsumen, yang pada akhirnya dapat membantu dalam peningkatan produksi film, pengembangan konten, dan strategi pemasaran yang lebih tepat sasaran. Evaluasi model juga menunjukkan hasil yang sangat baik pada content-based filtering, dengan precision sebesar 93.33%, yang mengindikasikan kemampuan model untuk memberikan rekomendasi yang sangat relevan dan akurat bagi pengguna. Secara keseluruhan, model rekomendasi ini membuka peluang baru dalam mengoptimalkan pengalaman pengguna di platform streaming dan memberikan insight berbasis data yang dapat digunakan untuk pengambilan keputusan yang lebih baik dalam industri film.

## Daftar Pustaka

1. unairnews. (2023, May 8). Systematic Literature Review pada Sistem Rekomendasi Film untuk Layanan Streaming - Universitas Airlangga Official Website. Universitas Airlangga Official Website. https://unair.ac.id/systematic-literature-review-pada-sistem-rekomendasi-film-untuk-layanan-streaming/
2. Salim, E., Pragantha, J., & Lauro, M. (n.d.). Perancangan Sistem Rekomendasi Film menggunakan metode Content- based Filtering. https://lintar.untar.ac.id/repository/penelitian/buktipenelitian_10390001_7A281222103549.pdf
3. Liang, S., & Susanto, J. (2022). Rancang Bangun Aplikasi Rekomendasi Restoran Menggunakan Metode K-Nearest Neighbors dan Content-Based Filtering. JURIKOM (Jurnal Riset Komputer), 9(1), 8–8 https://doi.org/10.30865/jurikom.v9i1.3816
4. MESIN REKOMENDASI FILM MENGGUNAKAN METODE KEMIRIPAN GENRE BERBASIS COLLABORATIVE FILTERING. (n.d.). https://repository.its.ac.id/42018/1/2215206701-Master-Thesis.pdf
5. Pradeep, N., Rao Mangalore, K., Rajpal, B., Prasad, N., & Shastri, R. (2020). Content Based Movie Recommendation System. https://www.riejournal.com/article_121501_a3717e6cf19a1845e350acb9148751ee.pdf
6. Gupta, M., Thakkar, A., Aashish, Gupta, V., & Rathore, D. P. S. (2020). Movie Recommender System Using Collaborative Filtering. 2020 International Conference on Electronics and Sustainable Communication Systems (ICESC), 415–420. https://doi.org/10.1109/icesc48915.2020.9155879







