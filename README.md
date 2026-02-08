Analisis RFM dan Segmentasi Customer Berbasis Dataset Olist
Deskripsi
Notebook Jupyter ini melakukan analisis RFM (Recency, Frequency, Monetary) dan segmentasi customer menggunakan dataset e-commerce Olist (dari Brasil). Tujuannya adalah untuk mengidentifikasi perilaku pelanggan berdasarkan metrik RFM, sehingga dapat mendukung strategi pemasaran seperti penargetan loyalitas, retensi, atau akuisisi pelanggan baru.
Proses analisis mencakup:

Pembersihan dan penggabungan data dari tiga dataset utama (orders, order items, dan customers).
Perhitungan metrik RFM:
Recency: Berapa lama sejak transaksi terakhir (dalam hari).
Frequency: Jumlah transaksi per pelanggan.
Monetary: Total nilai pengeluaran per pelanggan (harga produk + biaya pengiriman).

Segmentasi customer menggunakan quantile atau aturan bisnis sederhana untuk mengelompokkan pelanggan menjadi kategori seperti "Champions" (RFM tinggi), "At Risk" (Recency tinggi tapi Frequency rendah), dll.
Visualisasi (menggunakan Matplotlib dan Seaborn) untuk mendeteksi pola, seperti distribusi RFM atau scatter plot segmentasi.
Export hasil ke file CSV (rfm_analysis_result.csv) untuk analisis lanjutan atau integrasi dengan tools lain.

Notebook ini cocok untuk pemula di data analysis e-commerce, dengan fokus pada praktik RFM yang actionable. Hasilnya dapat digunakan untuk rekomendasi seperti email marketing targeted atau program loyalty.
Dataset
Dataset diambil dari Olist E-commerce Public Dataset (Kaggle):

olist_orders_dataset.csv: Detail order (status, timestamp pembelian, pengiriman).
olist_order_items_dataset.csv: Item per order (harga, freight value, product/seller ID).
olist_customers_dataset.csv: Info pelanggan unik (customer ID, zip code).

Total data: ~100.000 order, ~110.000 item, ~96.000 customer unik (periode 2016-2018).
Metode dan Tools

Bahasa: Python 3.x.
Libraries:
pandas & numpy: Manipulasi data.
matplotlib & seaborn: Visualisasi.
datetime: Handling timestamp.

Langkah Kunci:
Load dan inspect data (.head(), .info()).
Merge dataset berdasarkan order_id dan customer_id.
Hitung RFM menggunakan grupby dan datetime diff.
Segmentasi: Binning RFM ke skor 1-5, lalu label seperti "New Customers", "Loyal VIP".
Analisis deskriptif dan plot (e.g., heatmap korelasi RFM, pie chart segmentasi).


Hasil dan Output

File Output: rfm_analysis_result.csv berisi kolom seperti customer_id, recency, frequency, monetary, rfm_score, dan segment.
Insights Contoh (dari analisis tipikal):
~20% customer loyal berkontribusi 80% revenue (Pareto principle).
Segment "Champions" punya Monetary > R$500 dan Frequency > 5.

Visualisasi: Grafik RFM distribution, segment pie chart, dan boxplot per segment.
