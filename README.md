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

Proses diawali dengan melakukan querying data transaksi penjualan dari database SQL (Postgresql) relasional. Proses ini menggunakan Python sebagai penghubung dengan database, kemudian melakukan query data di dalam kode python tersebut.
![](assets/query_sql.png)
