# Excel Interactive Dashboard

Sebuah proyek analisis data ritel interaktif menggunakan **Excel** dan **SQL Database**. Dashboard ini dirancang untuk memantau performa penjualan (*Sales*), jumlah pesanan (*Orders*), serta profitabilitas (*Profit* & *Profit Margin*) lintas kategori, wilayah, segmentasi pelanggan, dan periode waktu secara dinamis.

---

## 🎥 Dashboard Preview

![Retail Sales Dashboard Demo](assets/demo.gif)

---

## Langkah-Langkah Pembuatan Dashboard

<details>
<summary><b>Klik di sini untuk melihat dokumentasi langkah pembuatan lengkap (SQL, Power Query, & Formulas)</b></summary>

<br>

### 1. Penarikan Data dari Database (SQL)

Proses diawali dengan melakukan querying data transaksi penjualan dari database SQL (Postgresql) relasional. Proses ini menggunakan Python sebagai penghubung dengan database, kemudian melakukan query data di dalam kode python tersebut. Selengkapnya ada di file `get_data_from_database.ipynb`
![screenshot query sql](assets/query_sql.png)

<br>

### 1. Persiapan data (Cleaning & Feature Engineering)

Setelah data didapatkan, proses selanjutnya adalah mempersiapkan data supaya data yang digunakan terjamin kualitasnya. Menurut prinsip "Garbage in Garbage out" maka proses ini wajib dilakukan. Persiapan data dilakukan dengan memanfaatkan Power Query pada Microsoft Excel. Proses yang dilakukan secara keseluruhan meliputi:
- Menyesuaikan tipe data
- Menghapus data duplikat
- Normalisasi dan konsistensi penulisan data kategorikal
- Mengatasi data kosong (Null Value)
- Mengatasi nilai outlier
![screenshoot power query 1](assets/power_query1.png)
![screenshoot power query 2](assets/power_query2.png)
