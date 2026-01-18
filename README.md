\# Analisis Jalur Evakuasi Taktis: Studi Kasus Pulau Sebatik



!\[Banner Proyek](gambar/1.png)



> \*\*Status Proyek:\*\* \*Completed (UAS Data Spasial)\* > \*\*Lokasi:\*\* Pulau Sebatik, Kalimantan Utara (Perbatasan Indonesia-Malaysia)



\## 📖 Ringkasan Eksekutif

Proyek ini bertujuan untuk merancang \*\*Jalur Evakuasi Taktis\*\* bagi warga sipil di Pulau Sebatik di tengah potensi eskalasi konflik blok Ambalat. Menggunakan analisis geospasial (GIS), penelitian ini menentukan rute teraman dan tercepat dengan menghindari area yang terpantau oleh radar musuh (Viewshed Analysis) dan memanfaatkan topografi alami sebagai pelindung.



---



\## 📌 Latar Belakang Masalah

Ketegangan di Blok Ambalat (luas ~15.235 km²) dipicu oleh sengketa klaim wilayah antara Indonesia dan Malaysia. Indonesia berpegang pada UNCLOS 1982 (Landas Kontinen), sedangkan Malaysia menggunakan Peta Baru 1979.



Situasi ini menuntut kesiapan mitigasi bencana non-alam, salah satunya adalah perencanaan evakuasi yang memperhitungkan:

1\.  \*\*Efisiensi Waktu:\*\* Seberapa cepat warga bisa mencapai titik aman.

2\.  \*\*Keamanan Visual:\*\* Seberapa tersembunyi jalur tersebut dari pantauan laut/musuh.



---



\## 🛠️ Metodologi \& Algoritma



\### 1. Load Balancing \& Penerapan Algoritma

!\[Algoritma dan Pembagian Sektor](gambar/3.png)



Analisis ini menggunakan algoritma \*\*Dijkstra Shortest Path\*\* dengan modifikasi \*Cost Attribute\* (pembobotan biaya):

\* \*\*Zona Aman:\*\* Diberi bobot kecepatan \*\*50 km/jam\*\* (Hambatan rendah).

\* \*\*Zona Bahaya:\*\* Diberi bobot kecepatan \*\*1 km/jam\*\* (Hambatan tinggi/harus dihindari).



Untuk mencegah penumpukan (bottleneck), area evakuasi dibagi menjadi 3 sektor utama: \*\*Utara, Tengah, dan Selatan\*\*.



\### 2. Analisis Viewshed (Jangkauan Pandang)

!\[Analisis Viewshed](gambar/2.png)



Analisis ini mensimulasikan visibilitas dari kapal perang musuh untuk menentukan area "Blind Spot" yang aman dilalui.

\* \*\*Observer (Radar Kapal):\*\* Tinggi 25 meter.

\* \*\*Target (Evakuee):\*\* Tinggi 1.6 meter.

\* \*\*Jangkauan Maksimal:\*\* 25 km.



---



\## 📊 Hasil Analisis \& Visualisasi

Berdasarkan simulasi komputasi, \*\*Sektor Selatan\*\* teridentifikasi sebagai jalur evakuasi paling taktis.



!\[Visualisasi Hasil Akhir](gambar/4.png)



\### Perbandingan Efisiensi Rute



| Sektor | Rata-Rata Jarak (KM) | Rata-Rata Waktu (Menit)\* | Kesimpulan |

| :--- | :---: | :---: | :--- |

| \*\*Utara\*\* | 45.42 | 90.85 | Kurang Efisien |

| \*\*Tengah\*\* | 44.98 | 89.97 | Moderat |

| \*\*Selatan\*\* | \*\*34.38\*\* | \*\*68.76\*\* | \*\*✅ Paling Efisien\*\* |



> \*Rumus Perhitungan Waktu ($t$): $t = \\frac{s}{v}$ dimana $v$ disesuaikan dengan bobot zona aman/bahaya.\*



---



\## 💻 Tech Stack \& Data Source

\*\*Software:\*\*

\* QGIS (Analisis Vektor, Raster, Network Analysis)

\* GitHub (Dokumentasi \& Version Control)



\*\*Sumber Data:\*\*

\* DEM (Digital Elevation Model) - Geospasial untuk Negeri

\* Batas Wilayah - Indonesia Geospasial



---



\## 👤 Author

\*\*Fikri Hanif\*\*

\* \*\*NIM:\*\* 247056016

\* \*\*Instansi:\*\* Universitas Sumatera Utara (USU)

\* \*Program Studi Magister/Lanjutan (Sesuaikan jika perlu)\*



---

\*Dibuat sebagai bagian dari tugas akhir mata kuliah Data Spasial.\*

