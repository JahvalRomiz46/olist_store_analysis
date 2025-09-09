# Analisis Data Penjualan Online Store dengan Python & Streamlit📊
<br>

## Deskripsi Proyek
Proyek ini merupakan analisis data eksplorasi (Exploratory Data Analysis/EDA) dari dataset e-commerce publik Olist. Tujuan utama proyek ini adalah untuk menganalisis tren penjualan, mengidentifikasi produk yang paling diminati, dan memahami perilaku pelanggan melalui analisis RFM (Recency, Frequency, Monetary). Seluruh proses analisis dan visualisasi data dilakukan menggunakan Python.

---

## Pertanyaan Bisnis & Analisis
* Produk apa yang paling banyak dan paling sedikit terjual?
* Bagaimana pola pembelian pelanggan berdasarkan parameter RFM (Recency, Frequency, Monetary)?
* Bagaimana performa pengiriman dibandingkan dengan waktu estimasi?
* Lokasi mana yang memiliki jumlah penjual dan pelanggan terbanyak?

---

## Teknologi yang Digunakan
* **Python**: Sebagai bahasa pemrograman utama.
* **Pandas**: Digunakan untuk manipulasi dan pembersihan data.
* **Streamlit**: Digunakan untuk membuat dashboard interaktif.
* **Matplotlib & Seaborn**: Digunakan untuk membuat visualisasi data.

---

## Struktur Repositori
├── dashboard/ <br>
│   ├── dashboard.py <br>
│   └── all_data.csv <br>
├── data/ <br>
│   ├── customers_dataset.csv <br>
│   ├── geolocation_dataset.csv <br>
│   ├── ... <br>
│   └── product_category_name_translation.csv <br>
├── notebook.ipynb <br>
└── requirements.txt <br>

* `notebook.ipynb`: Berisi seluruh langkah analisis data, mulai dari pengumpulan data, pembersihan, analisis eksplorasi, hingga penarikan kesimpulan.
* `dashboard/dashboard.py`: Skrip Streamlit yang digunakan untuk menjalankan dashboard.
* `requirements.txt`: Daftar library Python yang diperlukan untuk menjalankan proyek.
* `data/`: Folder yang menyimpan semua tabel dataset mentah.
  
---

## Proses Analisis
### 1. Data Wrangling
* **Penggabungan Data**: Menggabungkan beberapa dataset menjadi satu DataFrame untuk memudahkan analisis.
* **Standardisasi**: Menerjemahkan nama kategori produk dari bahasa Portugis ke bahasa Inggris.
* **Penanganan Data Hilang**: Mengisi nilai `NULL` pada beberapa kolom tanggal dengan nilai modus dan mengkonversi tipe data `date` menjadi `datetime`.
* **Penanganan Duplikat**: Mengidentifikasi dan menghapus data duplikat yang tidak diperlukan.

### 2. Exploratory Data Analysis (EDA)
* Menganalisis total penjualan per kategori produk untuk mengidentifikasi produk terlaris dan terlemah.
* Menghitung parameter RFM untuk mengidentifikasi pelanggan terbaik.
  - Recency: Menghitung jumlah hari sejak pembelian terakhir.
  - Frequency: Menghitung seberapa sering pelanggan melakukan pembelian.
  - Monetary: Menghitung total pengeluaran pelanggan.
* Menganalisis perbedaan antara waktu pengiriman aktual dan estimasi.

---

## Key Insights
* Tren Penjualan Produk: Kategori produk bed_bath_table adalah yang paling banyak terjual, sementara security_and_services adalah yang paling sedikit diminati.
* Pelanggan Terbaik (RFM):
  - Recency: Pelanggan dengan customer_id 4b7decb9b58e2569548b8b4c8e20e8d7 adalah yang paling aktif.
  - Frequency: Berdasarkan data, setiap customer memiliki jumlah pesanan 1
  - Monetary: Pelanggan dengan customer_id 1617b1357756262bfa56ab541c47bc16 adalah yang paling banyak menghabiskan uang.
* Lokasi: Mayoritas penjual dan pelanggan berasal dari kota Sao Paulo, Rio De Janeiro, dan Belo Horizonte.

---

## Kesimpulan
Proyek ini berhasil melakukan pembersihan dan analisis data untuk mendapatkan wawasan penting mengenai Olist Store. Hasil analisis ini dapat menjadi dasar bagi tim bisnis untuk merumuskan strategi promosi, retensi pelanggan, dan manajemen inventaris yang lebih efektif. Dashboard Streamlit yang telah dibuat dapat digunakan sebagai alat bantu visual untuk memantau performa bisnis secara berkelanjutan.

<br>

## Cara Menjalankan Dashboard
* Pastikan telah menginstal semua library yang diperlukan dengan menjalankan: `pip install -r requirements.txt`.
* Masuk ke direktori dashboard.
* Jalankan Streamlit dengan perintah: `streamlit run dashboard.py`.
