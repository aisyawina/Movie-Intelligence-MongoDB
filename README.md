![Logo IPB University_Horizontal (1)](https://github.com/user-attachments/assets/a2473f19-385e-459a-9c90-409481f5b313)

<h1 align="center">🎬 <b>MOVIE INTELLIGENCE!</b> 🚀🍿</h1>
                                             
<h2 align="center"> A Data-Driven Strategy to Build Smarter Entertainment Ecosystems and Maximize Viewer Monetization 

<p align="center"> 👥 Vistameta Team </p>

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

3. Jalankan database MongoDB:
```bash
mongod --dbpath mongodb+srv://root:1234@mds-db.dtk5gzr.mongodb.net/?retryWrites=true&w=majority&appName=mds-db
```

4. Akses dashboard visualisasi:

   Buka link dashboard berikut untuk melihat insight real-time dan interaktif:

   https://bit.ly/dashboardmovieintelligence-mds 


6. Akses dashboard visualisasi untuk insight real-time (link atau instruksi akan diberikan)

---

## PPT 
Presentasi dalam bentuk power point dapat dilihat disini :

https://bit.ly/moviintelligence-mds 


## Data Praktikum UAS Manajemen Data Statistika

[https://bit.ly/3HrbSJF](https://bit.ly/dataprakmdsuas) 

---

## 🙌 Contributors

Siti Nuradilla - M0501241010

Reyuli Andespa - M0501241072

Riza Rahmah Angelia - M0501241008

Aisya Wina Wahda - M0501241053

![tim](https://github.com/user-attachments/assets/41952981-5a40-41ed-8369-d3187ece50de)




