![Logo IPB University_Horizontal (1)](https://github.com/user-attachments/assets/a2473f19-385e-459a-9c90-409481f5b313)

<h1 align="center">🎬 <b>MOVIE INTELLIGENCE!</b> 🚀🍿</h1>
                                             
<h2 align="center"> A Data-Driven Strategy to Build Smarter Entertainment Ecosystems and Maximize Viewer Monetization 

<p align="center"> 👥 Vistameta Team </p>

---

## Demo  
Berikut adalah tampilan dashboard Movie Intelligence dalam bentuk GIF untuk memberikan gambaran interaktif dan visualisasi data yang telah dikembangkan:

![Movie Intelligence Dashboard Demo](./MDS.gif)

---

## 🔍 Overview

**Movie Intelligence** adalah platform data-driven yang dibangun menggunakan metadata dari [TMDb (The Movie Database)](https://www.themoviedb.org/) dan dikembangkan oleh Tim VistaMeta untuk mengungkap permintaan pasar film secara real-time, memahami demografi audiens, dan memprediksi potensi revenue. Solusi ini membantu platform OTT dan pelaku industri film memilih konten yang pasti ditonton dan memaksimalkan monetisasi penonton.

---

## 📌 Problem Statement

- Metadata film saat ini bersifat **statis** dan tidak merepresentasikan tren penonton terkini.  
- Preferensi penonton sulit diprediksi secara **real-time**.  
- Kurangnya visualisasi insight yang **interaktif dan actionable**.  
- Industri film membutuhkan data insight strategis, bukan hanya data mentah.

---

## 💡 Our Solution

Movie Intelligence menyediakan fitur unggulan berikut:

| Feature                   | Manfaat                                                                                   |
|---------------------------|-------------------------------------------------------------------------------------------|
| 🎯 Audience Demography     | Mengungkap struktur demografi penonton (usia, wilayah, jenis kelamin, genre) secara real-time |
| 📊 Market Demand Analytics | Analisis tren genre, durasi, dan konten paling diminati secara global dan lokal           |
| 💰 Revenue-Cost Analysis   | Evaluasi efisiensi anggaran produksi dan potensi keuntungan film                          |
| 📈 Visualisasi Interaktif  | Dashboard yang mudah dipahami dan digunakan untuk pengambilan keputusan                   |

---

## 🔥 Key Insights

- Mayoritas film memiliki rating 60-80%, menunjukkan kualitas cukup hingga baik.  
- Drama dan Komedi adalah genre paling dominan, dengan durasi yang sesuai kebutuhan pasar.  
- Genre Documentary dan Music cenderung berdurasi panjang dan mendalam.  
- Film dengan budget besar tidak selalu populer; ada film berbudget sedang yang sukses besar.  
- Genre hybrid (Action-Comedy, Horror-Thriller) menunjukkan engagement tinggi.

---

## 📊 Architecture & Pipeline

Platform ini memanfaatkan pipeline agregasi MongoDB sebagai berikut:

1. Grouping data film berdasarkan genre, bahasa, rating, dan parameter lain.  
2. Menghitung rata-rata, total, dan distribusi budget, revenue, popularitas.  
3. Menyajikan insight melalui dashboard interaktif.
- Agregasi yang kami buat bisa diakses melalui
    <a href="Agregasi"> Klik dan Lihat Data Berikut! </a>

---

## 🎯 Use Case & Investor Opportunity

- Menentukan strategi investasi konten berdasarkan genre dan durasi dengan ROI terbaik.  
- Memetakan pasar lokal dan global untuk produksi konten tepat sasaran.  
- Investasi pada franchise dan film dengan fanbase kuat menghasilkan keuntungan stabil.

---

## 📚 Resources & References
- TMDb Official Site

  Sebuah basis data film dan TV yang komprehensif dan didukung oleh komunitas global. Metadata mencakup jutaan data film termasuk genre, bahasa, rating, popularitas, budget, dan revenue.
- MongoDB Aggregation Framework
- Studi kasus investasi dan performa konten dari data TMDb

Link Data yang sudah digabung dan akan digunakan :
  <a href="Data CSV"> Klik dan Lihat Data Berikut! </a>

---

## 🛠️ Installation & Usage

1. Clone repository ini

```bash
git clone https://github.com/yourusername/movie-intelligence.git
cd movie-intelligence
```

2. Setup environment

   Pastikan sudah terinstall Python 3.x, MongoDB, dan library pendukung (pandas, pymongo, dsb).
```bash
pip install -r requirements.txt
```

3. How to Scrapping Data with Python
```bash
from tmdbv3api import TMDb, Movie
import pandas as pd
from time import sleep

# --- Setup TMDb ---
tmdb = TMDb()
tmdb.api_key = '3e730b30512651f4b46a94a014fbfd06'
tmdb.language = 'en'

movie = Movie()

# --- Ambil 200 halaman film populer ---
movie_data = []

for page in range(1, 201):  # Ambil halaman 1 sampai 200 (sekitar 4000 film)
    print(f"Processing page {page}...")
    try:
        popular_movies = movie.popular(page=page)

        for m in popular_movies:
            try:
                details = movie.details(m.id)
                genres = ", ".join([g['name'] for g in details.genres]) if details.genres else None

                movie_data.append({
                    'movie_id': m.id,
                    'title': m.title,
                    'original_title': details.original_title,
                    'overview': m.overview,
                    'release_date': m.release_date,
                    'vote_average (%)': round(m.vote_average * 10, 2),
                    'vote_count': m.vote_count,
                    'popularity': m.popularity,
                    'runtime (min)': details.runtime,
                    'status': details.status,
                    'tagline': details.tagline,
                    'genres': genres,
                    'budget': details.budget,
                    'revenue': details.revenue,
                    'original_language': details.original_language
                })

                sleep(0.5)  # Hindari rate limit
            except Exception as e:
                print(f"Failed to get details for movie ID {m.id}: {e}")
    except Exception as e:
        print(f"Failed to get page {page}: {e}")

# --- Simpan ke DataFrame ---
df = pd.DataFrame(movie_data)
df
# --- Simpan ke CSV ---
df.to_csv('popular_movies_200_pages.csv', index=False)
```


4. Jalankan database MongoDB:
```bash
mongod --dbpath mongodb+srv://root:1234@mds-db.dtk5gzr.mongodb.net/?retryWrites=true&w=majority&appName=mds-db
```

5. Akses dashboard visualisasi:

   Buka link dashboard berikut untuk melihat insight real-time dan interaktif:

   https://bit.ly/dashboardmovieintelligence-mds 



---

##  Project Movie Intelligence PPT 
Presentasi dalam bentuk power point dapat dilihat disini :
<a href="Movie Intelligence PPT.pdf"> Klik dan Lihat PPT Berikut! </a>

https://bit.ly/moviintelligence-mds 


## Data Praktikum UAS Manajemen Data Statistika
<a href="Dataset"> Klik dan Lihat Dataset Berikut! </a>

[https://bit.ly/3HrbSJF](https://bit.ly/dataprakmdsuas) 

---

## 🙌 Contributors Vistameta Team

Siti Nuradilla - M0501241010

Reyuli Andespa - M0501241072

Riza Rahmah Angelia - M0501241008

Aisya Wina Wahda - M0501241053

![tim](https://github.com/user-attachments/assets/41952981-5a40-41ed-8369-d3187ece50de)




