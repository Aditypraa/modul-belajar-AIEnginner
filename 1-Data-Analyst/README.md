# 📊 Belajar Analisis Data Dengan Python: Data Wrangling

## 📑 Daftar Isi

- [Background](#background)
- [Tujuan](#tujuan)
- [Alur Latihan](#alur-latihan)
- [Persiapan Environment](#persiapan-environment)
  - [Menggunakan Conda](#membuat-virtual-environment-menggunakan-conda)
  - [Menggunakan Pipenv](#membuat-virtual-environment-menggunakan-pipenv)
- [Memulai Proyek](#memulai-proyek)
- [Latihan Analisis Data](#latihan-analisis-data)
  - [Data Wrangling](#data-wrangling)
  - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Membuat Visualisasi Data](#membuat-visualisasi-data)
  - [Membuat Dashboard dengan Streamlit](#membuat-dashboard-dengan-streamlit)

## 🏢 Background

**Dicoding Collection** atau sering disingkat **DiCo** merupakan sebuah perusahaan yang bergerak di bidang fashion. Ia memproduksi berbagai item fashion dan menjualnya melalui platform online.

![DiCo Fashion Company](dos:1c183d6627f771f902fa1c5a86de6b2420230309133244.png)

Sebagai perusahaan kekinian, DiCo menyadari betapa pentingnya data bagi perkembangan sebuah bisnis. Oleh karena itu, ia menyimpan semua history penjualan beserta informasi terkait produk dan customers dalam sebuah database. Database ini terdiri dari empat buah tabel:

| Tabel         | Deskripsi                                                                                                                                                          |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **customers** | Menyimpan berbagai informasi terkait customer, seperti `customer_id`, `customer_name`, `gender`, `age`, `home_address`, `zip_code`, `city`, `state`, dan `country` |
| **orders**    | Menyimpan berbagai informasi terkait sebuah order yang terdiri dari `order_id`, `customer_id`, `order_date`, dan `delivery_date`                                   |
| **products**  | Berisi berbagai informasi terkait sebuah produk, seperti `product_id`, `product_type`, `product_name`, `size`, `colour`, `price`, `quantity`, dan `description`    |
| **sales**     | Mengandung informasi detail terkait penjualan, seperti `sales_id`, `order_id`, `product_id`, `price_per_unit`, `quantity`, dan `total_price`                       |

Nah, sebagai calon praktisi data profesional, Anda akan diminta untuk menganalisis seluruh data tersebut. So, apakah Anda siap untuk menjawab tantangan ini? Tentunya siap dong! 💪

## 🎯 Tujuan

First of all, kita akan mulai proyek analisis data ini dengan menjalankan proses data wrangling terlebih dahulu. Proses ini memiliki tujuan antara lain:

1. Mengumpulkan seluruh data yang dibutuhkan _(data gathering)_
2. Menilai kualitas dari data yang telah dikumpulkan _(data assessing)_
3. Membersihkan data tersebut sehingga siap untuk dianalisis _(data cleaning)_

## 🛣️ Alur Latihan

Berikut merupakan tahapan dalam latihan ini:

1. Tahap persiapan
2. Tahap gathering data
3. Tahap assessing data
4. Tahap cleaning data
5. Exploratory Data Analysis (EDA)
6. Membuat Visualisasi Data
7. Membuat Dashboard dengan Streamlit

## 🛠️ Persiapan Environment

Pertama, siapkan environment untuk menjalankan proyek ini. Pada proyek latihan ini, Anda dapat menggunakan berbagai IDE seperti:

- 📓 Jupyter Notebook
- ☁️ Google Colaboratory (Google Colab)

> **💡 Saran Penting**: Kami sangat menyarankan Anda untuk selalu membuat virtualenv baru pada setiap proyek. Hal ini untuk meminimalisasi masalah yang berhubungan dengan dependency pada library yang akan digunakan.

### Membuat Virtual Environment Menggunakan Conda

Apabila menginstal Python melalui Anaconda ataupun miniconda, Anda dapat menggunakan conda sebagai package manager dan environment management system. Berikut merupakan tahapan dalam membuat virtual environment menggunakan conda:

1. **Buka terminal atau PowerShell**

2. **Jalankan perintah berikut:**

   ```bash
   conda create --name main-ds python=3.9
   ```

3. **Aktifkan virtual environment dengan menjalankan perintah berikut:**

   ```bash
   conda activate main-ds
   ```

4. **Instal semua library yang dibutuhkan menggunakan perintah berikut:**

   ```bash
   pip install numpy pandas scipy matplotlib seaborn jupyter
   ```

5. **Buat sebuah folder baru bernama proyek_analisis_data. Folder tersebut akan menjadi directory utama dalam proyek ini:**

   ```bash
   mkdir proyek_analisis_data
   ```

6. **Pindah ke folder terbaru tersebut:**

   ```bash
   cd proyek_analisis_data
   ```

7. **Buka jupyter-notebook:**
   ```bash
   jupyter-notebook .
   ```

### Membuat Virtual Environment Menggunakan Pipenv

Jika menginstal python melalui official home, Anda dapat menggunakan pip sebagai package manager dan pipenv sebagai environment management. Berikut merupakan tahapan dalam membuat virtual environment menggunakan pipenv:

1. **Buka terminal atau PowerShell**

2. **Buat sebuah folder baru bernama proyek_analisis_data:**

   ```bash
   mkdir proyek_analisis_data
   ```

3. **Pindah ke folder terbaru tersebut:**

   ```bash
   cd proyek_analisis_data
   ```

4. **Buat sebuah virtual environment:**

   ```bash
   pipenv install
   ```

5. **Aktifkan virtual environment:**

   ```bash
   pipenv shell
   ```

6. **Instal semua library yang dibutuhkan:**

   ```bash
   pip install numpy pandas scipy matplotlib seaborn jupyter
   ```

7. **Buka jupyter-notebook:**
   ```bash
   jupyter-notebook .
   ```

## 📝 Memulai Proyek

1. Buat sebuah berkas baru bernama `notebook.ipynb`. Pada berkas inilah, seluruh proses analisis data akan dikerjakan.
2. Buka berkas `notebook.ipynb`.
3. Untuk memulai pengerjaan proyek ini, kita perlu memanggil semua library yang dibutuhkan:

```python
# Import necessary libraries
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

Last but not least, siapkan sebuah camilan sebagai suplai energi selama mengikuti latihan ini! ☕🍪

## 📊 Latihan Analisis Data

### Data Wrangling

Ini adalah fase pertama dalam proyek analisis data, di mana kita akan melakukan:
- Pengumpulan data (data gathering)
- Penilaian kualitas data (data assessing)
- Pembersihan data (data cleaning)

### Exploratory Data Analysis (EDA)

> **Penting!** 
> Pastikan Anda telah menyelesaikan latihan Data Wrangling sebelum melanjutkan ke tahap ini.

#### Tujuan
Pada tahap ini kita akan:
1. Membuat pertanyaan analisis atau bisnis yang ingin dicari jawabannya
2. Melakukan eksplorasi terhadap setiap data untuk mencari insight menarik

#### Pertanyaan Bisnis
Sebagai perusahaan online fashion, DiCo perlu:
1. Mengevaluasi performa penjualan dan memahami item fashion yang paling laris
2. Memahami pelanggan untuk membuat strategi campaign yang efisien

Berdasarkan kebutuhan tersebut, kami mendefinisikan beberapa pertanyaan bisnis:
1. Bagaimana performa penjualan dan revenue perusahaan dalam beberapa bulan terakhir?
2. Produk apa yang paling banyak dan paling sedikit terjual?
3. Bagaimana demografi pelanggan yang kita miliki?
4. Kapan terakhir pelanggan melakukan transaksi?
5. Seberapa sering seorang pelanggan melakukan pembelian dalam beberapa bulan terakhir?
6. Berapa banyak uang yang dihabiskan pelanggan dalam beberapa bulan terakhir?

### Membuat Visualisasi Data

> **Penting!** 
> Pastikan Anda telah menyelesaikan latihan Exploratory Data Analysis sebelum melanjutkan ke tahap ini.

#### Tujuan
Pada tahap ini kita akan:
1. Menjawab seluruh pertanyaan bisnis yang sebelumnya telah dibuat
2. Membuat visualisasi data untuk mempermudah penyampaian hasil analisis data

### Membuat Dashboard dengan Streamlit

> **Penting!** 
> Pastikan Anda telah menyelesaikan latihan Membuat Visualisasi Data sebelum melanjutkan ke tahap ini.

#### Tujuan
Pada tahap ini kita akan:
1. Membuat sebuah report analisis data yang interaktif dalam bentuk dashboard
2. Mempermudah audiens atau user dalam melihat hasil analisis data

#### Persiapan Dashboard

1. **Persiapkan Data yang Telah Dibersihkan**:
   - Jalankan kembali seluruh kode pada notebook sebelumnya
   - Tambahkan kode berikut di bagian akhir notebook untuk menyimpan data:
   ```python
   all_df.to_csv("all_data.csv", index=False)
   ```
   - Unduh berkas data tersebut dengan mengklik tombol Download pada bagian file
   ![Download Data](dos:b6710246b93a5ae15c64fef083e24ee020230310141757.jpeg)

2. **Instal Library untuk Dashboard**:
   ```bash
   conda activate main-ds
   pip install streamlit babel
   ```

3. **Buat Proyek Dashboard**:
   - Buka code editor favorit Anda
   - Buat sebuah proyek baru dengan nama `dashboard`
   - Pindahkan berkas data yang sudah diunduh ke dalam folder proyek

4. **Jalankan Dashboard**:
   - Arahkan Terminal/PowerShell/Command Prompt ke path folder proyek dashboard
   - Jalankan dashboard dengan perintah:
   ```bash
   streamlit run dashboard.py
   ```

5. **Siapkan Camilan dan Minuman** untuk mendukung proses pengembangan dashboard Anda! ☕🍪
