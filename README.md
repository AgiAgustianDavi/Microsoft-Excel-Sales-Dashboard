# Excel Interactive Dashboard

Sebuah proyek analisis data ritel interaktif menggunakan **Excel** dan **SQL Database**. Dashboard ini dirancang untuk memantau performa penjualan (*Sales*), jumlah pesanan (*Orders*), serta profitabilitas (*Profit* & *Profit Margin*) lintas kategori, wilayah, segmentasi pelanggan, dan periode waktu secara dinamis.

---

## 🎥 Dashboard Preview

![Retail Sales Dashboard Demo](assets/demo.gif)

---

## Langkah-Langkah Pembuatan Dashboard

<details>
<summary><b>Klik di sini untuk melihat langkah-langkah pembuatan scara umum (SQL, Power Query, & Formula)</b></summary>

<br>

### 1. Penarikan Data dari Database (SQL)

Proses diawali dengan melakukan querying data transaksi penjualan dari database SQL (Postgresql) relasional. Proses ini menggunakan Python sebagai penghubung dengan database, kemudian melakukan query data di dalam kode python tersebut. Selengkapnya ada di file [get_data_from_database.ipynb](get_data_from_database.ipynb)

![screenshot query sql](assets/query_sql.png)

<br>

### 2. Persiapan data (Cleaning & Feature Engineering)

Setelah data didapatkan, proses selanjutnya adalah mempersiapkan data supaya data yang digunakan terjamin kualitasnya. Menurut prinsip "Garbage in Garbage out" maka proses ini wajib dilakukan. Persiapan data dilakukan dengan memanfaatkan Power Query pada Microsoft Excel. Proses yang dilakukan secara keseluruhan meliputi:
- Menyesuaikan tipe data
- Menghapus data duplikat
- Normalisasi dan konsistensi penulisan data kategorikal
- Mengatasi data kosong (Null Value)
- Mengatasi nilai outlier
  
![screenshot power query 1](assets/power_query1.png)

![screenshot power query 2](assets/power_query2.png)

Setelah itu, dilanjutkan dengan feature engineering, seperti membuat kolom Sales, Profit, Profit Margin, Month, Month_num, Year, dan Day. Proses ini memanfaatkan fitur formula pada Microsoft Excel

![screenshoot kolom yang baru dibuat](assets/add_column.png)

<br>

### 3. Perhitungan KPI & Pembuatan Grafik

Tahap berikutnya adalah melakukan penghitungan KPI & grafik dengan mengandalkan berbagai fitur pada Microsoft Excel, mulai dari Formula, Pivot Table, Name manager, Slicer, Insert Graph, dll. Proses yang disajikan hanya beberapa bagian. untuk lengkapnya silahkan buka file [dashboard_sales.xlsx](dashboard_sales.xlsx)

- Membuat Pivot tabel master untuk mempermudah proses perhitungan dan pembuatan slicer
  
![Screenshot pivot tabel master](assets/pivot_table_master.png)

- Membuat proses perhitungan KPI. <br>Proses dilakukan dengan memanfaatkan fitur formula pada microsoft excel seperti IF, SUMIFS, COUNTIFS, VLOOKUP, dll.
  
![Screenshot proses pembuatan kpi](assets/kpi.png)

- Membuat tabel untuk line chart dinamis. <br>Proses ini juga memanfaatkan fitur name manager untuk membuat line chart peka terhadap perubahan tahun atau bulan dari slicer
  
![Screenshot formula line chart](assets/dinamic_line_chart.png)

![Screenshot pembuatan name manager](assets/name_manager.png)

![Screenshot semua name manager](assets/name_manager2.png)

- Membuat pivot tabel untuk grafik
  
![Screenshot semua pivot tabel grafik](assets/pivot_table_for_chart.png)

<br>

### 4. Mendesain Tampilan Dashboard menggunakan Microsoft Power Point

Setelah semua siap, tahapan berikutnya adalah mendesain background tampilan dashboardnya agar rapi dan nyaman dipandang. Proses ini memanfaatkan Microsoft Power Point karena mengatur desainya lebih mudah dan dapat dengan mudah di copy ke Microsoft Excel.

![Screenshot proses pembuatan desin](assets/bg_design.png)

<br>

### 5. Put it all together

Setelah desain siap, selanjutnya tinggal copy semuanya ke sheet baru bernama dashboard di microsoft excel. Mulai dari desain, KPI, Grafik, dan Slicer yang sudah dibuat. Atur menyesuaikan desain backgroundnya.

Selesai
