# Project Scrapping Produk Seblak di Tokopedia

## Project Overview
Project ini bertujuan untuk melakukan analisis penjualan produk seblak dari informasi produk serupa yang ada di website e-commerce Tokopedia sebagai pertimbangan pengambilan keputusan.
Scraping data menggunakan teknologi Selenium dan BeautifulSoup.

## Business Understanding/Problem Statement
Tahap ini bertujuan untuk mendapatkan pemahaman tentang bisnis, kebutuhan, tujuan, metriknya.

### Defining Problem Statement
1. Specific : Melakukan analisis untuk mengetahui prospek penjualan produk seblak dengan melihat tingkat customer loyalty
2. Measurable : Tingkat kepuasan konsumen terhadap produk lebih dari 4.7
3. Achievable : Mengetahui harga produk yang sesuai yang menarik minat konsumen
4. Relevant : Meningkatnya customer loyalty akan meningkatkan keuntungan penjualan
5. Time-bound : Proses analisis dilakukan selama sebulan menggunakan data yang diambil per hari

<b>Menganalisis prospek penjualan produk seblak dengan mengevaluasi tingkat customer loyalty dengan melihat tingkat kepuasan konsumen terhadap produk dengan fokus pada harga produk yang menarik minat konsumen dan memperoleh keuntungan yang lebih tinggi</b>

## Data Scraping Result
<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>nama_produk</th>
      <th>harga_produk</th>
      <th>penjual</th>
      <th>kota_toko</th>
      <th>banyaknya_terjual</th>
      <th>rating_produk</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Geli Food Seblak Ceker Tanpa Tulang Super Peda...</td>
      <td>Rp24.000</td>
      <td>Lidigeli</td>
      <td>Kab. Garut</td>
      <td>70+ terjual</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Seblak Rafael, Seblak Coet Instan Halal</td>
      <td>Rp25.000</td>
      <td>Brother Meat Shop</td>
      <td>Depok</td>
      <td>250+ terjual</td>
      <td>4.9</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Kerupuk Seblak Pedas Krupuk Pelangi Pedas Sebl...</td>
      <td>Rp15.500</td>
      <td>toko bemo</td>
      <td>Jakarta Timur</td>
      <td>500+ terjual</td>
      <td>4.9</td>
    </tr>
    <tr>
      <th>3</th>
      <td>kerupuk seblak 1kg</td>
      <td>Rp11.500</td>
      <td>zyvasnack</td>
      <td>Kab. Purworejo</td>
      <td>4 terjual</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>(250 GR) KERUPUK SEBLAK MENTAH / KERUPUK BAWANG</td>
      <td>Rp8.500</td>
      <td>Rejeki Makmur Jaya.</td>
      <td>Kab. Bantul</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>838</th>
      <td>Sebring (Seblak Kering) Original</td>
      <td>Rp19.900</td>
      <td>DapurIbuKita</td>
      <td>Jakarta Barat</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>839</th>
      <td>seblak kencur / okesnack</td>
      <td>Rp10.000</td>
      <td>oke snack</td>
      <td>Jakarta Selatan</td>
      <td>750+ terjual</td>
      <td>4.9</td>
    </tr>
    <tr>
      <th>840</th>
      <td>Siomay Kerikil Kuncup / Siomay Mini / SIomay S...</td>
      <td>Rp8.000</td>
      <td>Aeeshastore</td>
      <td>Bandung</td>
      <td>100+ terjual</td>
      <td>4.6</td>
    </tr>
    <tr>
      <th>841</th>
      <td>Kylafood Seblak karuhun</td>
      <td>Rp12.825</td>
      <td>kylafood</td>
      <td>Bandung</td>
      <td>4rb+ terjual</td>
      <td>4.8</td>
    </tr>
    <tr>
      <th>842</th>
      <td>cemilan SEBLAK KARI PEDAS 65gr</td>
      <td>Rp4.500</td>
      <td>oke snack</td>
      <td>Jakarta Selatan</td>
      <td>100+ terjual</td>
      <td>4.8</td>
    </tr>
  </tbody>
</table>
<p>843 rows × 6 columns</p>
</div>

Dataset berisi 6 kolom, dimana kolom 'nama_produk', 'penjual', dan 'kota_toko' dapat dilakukan analisis sebagai data bertipe kategorik dan kolom 'harga_produk', 'banyaknya_terjual', dan 'rating_produk' dapat dilakukan analisis sebagai data bertipe numerik. 

## Data Preparation (Data Cleaning)
Dilakukan data cleaning untuk mengubah bentuk data menjadi konsisten dan menyesuaikan tipe data agar dapat digunakan untuk perhitungan statisik.<br>
Tahapan Data Cleaning yang dilakukan:
- Menghilangkan karakter 'Rp', '.', '+', ' terjual', dan mengganti 'rb' dengan '000'
- Mengganti nilai NaN dengan '0'
- Mengubah tipe data beberapa kolom object menjadi integer dan float

## Analysis Result
- Potensi pendapatan terkecil/minimum yang didapat dari penjualan seblak perbulan adalah 4675529.107129768 atau Rp. 4,675,529.10 dan potensi pendapatan terbesar/maksimum yang didapat dari penjualan seblak perbulan adalah 7611076.271280671 atau sekitar Rp. 7,611,076.27.
- Rata-rata harga barang di jabodetabek lebih besar dibandingkan rata-rata harga barang di luar daerah jabodetabek. Namum berdasarkan nilai p-value = 0.46 yang dimana lebih besar dibanding critical value = 0.05 maka hasil hipostesisnya adalah terima H0 yang berarti tidak ada perbedaan harga barang di daerah jabodetabek maupun di luar jabodetabek.
- Terdapat hubungan harga produk dengan kategori kepuasan konsumen.

## Conclusion 
Dari proses analisis yang telah dilakukan, produk seblak memiliki prospek atau peluang yang baik. Hal ini dapat dilihat dari potensi pendapatan yang cukup besar, peluang yang sama untuk penjual produk seblak dari luar jabodetabek karena tidak ada perbedaan harga yang signifikan, dan modus atau rating terbanyak dari penjualan produk seblak adalah 5.0 (rating terbaik). Sebagai strategi penjualan produk seblak kedepan dapat dipertimbangkan untuk penentuan harga yang sesuai agar memenuhi kepuasan konsumen.