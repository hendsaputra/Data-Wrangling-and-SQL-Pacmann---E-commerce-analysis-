# Data Wrangling and SQL-Pacmann- E-commerce analysis

# 1.OBJECTIVES
Menganalisa data e-commerce untuk mencari :
a. Mencari penjualan terbanyak dari kategori 
b. Mencari Distribusi Penjualan Dari order
c. Analisis korelasi pada product dan seller

Analisis menggunakan Jupyter Notebook (python)

# 2. DATASET
Untuk melihat relasi antar data, dataset dapat dilihat pada berikut ini
<img width="619" alt="Screenshot 2023-09-06 at 17 30 31" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/a234324a-44cc-4d17-be2c-fe3af5df7e4d">

# 3. EKSPLORISASI DAN PEMROSESAN DATA

## Import Libraries dan Mengakses data tipe .db
<img width="1079" alt="Screenshot 2023-09-06 at 17 33 18" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/d2e07b25-6b1d-4f82-8cee-938f8925478d">
<img width="1085" alt="Screenshot 2023-09-06 at 17 34 45" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/835e61aa-4887-4e04-81c7-feb05d72e1d1">

## Melakukan Data Merging
Data merging dilakukan untuk menggabungkan data yang memiliki relasi antar data, sehingga bisa dilihat berikut ini

### Data merging pada order_id
<img width="1075" alt="Screenshot 2023-09-06 at 17 36 41" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/5293824a-9742-4423-ba8c-9b99d9816148">

### Data merging pada product_id
<img width="838" alt="Screenshot 2023-09-06 at 17 37 47" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/21f88d89-7cd1-4b61-839b-136425f48ae0">

### Data merging pada seller_id
<img width="794" alt="Screenshot 2023-09-06 at 17 39 33" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/aedb9bf8-9345-4051-b6c1-3e9c8f0e9572">

### Data merging pada zip_code_prefix
<img width="1083" alt="Screenshot 2023-09-06 at 17 40 54" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/5998e93a-be77-4598-a141-b2b5db06736e">


## Handling Missing Value
Handling missing value dilakukan untuk mengidentifikasi data yang bersifat NaN.

### Identifikasi Nan pada order_id
<img width="1007" alt="Screenshot 2023-09-06 at 17 43 08" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/591cc388-50a5-4497-9b44-1cf5752cbe4c">
<img width="938" alt="Screenshot 2023-09-06 at 17 43 34" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/9feb91a5-fde3-42b2-b828-cd5d929cb1f7">

### Identifikasi Nan pada product_id
<img width="1082" alt="Screenshot 2023-09-06 at 17 44 25" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/127e0918-f646-4497-a6d0-c6058badcc1d">
<img width="981" alt="Screenshot 2023-09-06 at 17 45 19" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/91dd172d-8f43-4276-8785-867e205b40f7">

### Identifikasi Nan pada seller_id
<img width="1078" alt="Screenshot 2023-09-06 at 17 46 10" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/9625512f-698d-4889-8738-71716c905aa4">
<img width="940" alt="Screenshot 2023-09-06 at 17 46 34" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/d225bdbe-1e46-4381-81fe-cfcab6053aa0">

### Identifikasi Nan pada zip_code_prefix
<img width="1001" alt="Screenshot 2023-09-06 at 17 47 05" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/2f1b0fc0-e222-4deb-997c-9ad734dd3f75">
<img width="836" alt="Screenshot 2023-09-06 at 17 47 18" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/78959810-5bc4-473c-ba5c-7d1faa2b209b">

### Kesimpulan pada identifikasi NaN
Bedasarkan hasil Handling Missing Value, terdapat NaN pada product_id. Diantaranya adalah : product_category_name, product_name_lenght, product description_lenght, product_description_lenght, product_photos_qty, product_weight_g, product_lenght_cm, product_height_cm, product_width_cm

### Melakukan drop pada product_id
<img width="823" alt="Screenshot 2023-09-06 at 17 49 30" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/6913e795-02c7-4e41-8ff8-875fa58dadf1">
<img width="280" alt="Screenshot 2023-09-06 at 17 49 53" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/7bc177d5-3533-46bb-9cc3-011d4a3c3beb">

## Handling Duplicate
Handling duplicate dilakukan untuk mengidentifikasi data yang bersifat duplikasi.

### Handling duplicate pada order_id
<img width="292" alt="Screenshot 2023-09-06 at 17 50 55" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/3e262958-d3ca-487b-b330-44762dd1fe63">

### Handling duplicate pada product_id
<img width="311" alt="Screenshot 2023-09-06 at 17 51 40" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/98c9ec6a-2a89-45ce-9069-dafa0cbd68fa">

### Handling duplicate pada seller_id
<img width="307" alt="Screenshot 2023-09-06 at 17 53 34" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/288eeb41-cb7f-406f-aaeb-769890e74374">

### Handling duplicate pada zip_code_prefix
<img width="353" alt="Screenshot 2023-09-06 at 17 54 16" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/866d86e1-7f46-41f3-a222-98368ba9d4f0">

### Kesimpulan
Tidak terdapat duplicate data pada order_id, product_id, seller_id, dan zip_code_prefix

# 4. ANALYSIS DATA
Selanjutnya, melakukan analisis setelah melakukan pemrosesan data. Visualisasi menggunakan seaborn dan matpotlib untuk membuat tabel dan melihat persebaran data.

## a. Mencari penjualan terbanyak dari kategori 
### Menampilkan tabel order_id
<img width="1072" alt="Screenshot 2023-09-06 at 23 40 26" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/921be019-0d5c-4ec7-8131-28f42f439ab7">

### Mencari banyaknya penjualan dari order_item_id
<img width="1095" alt="Screenshot 2023-09-06 at 23 41 10" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/d626ca66-0529-4329-89ea-7c383761e67b">

### Membuat table
<img width="639" alt="Screenshot 2023-09-06 at 23 41 51" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/af566037-f264-455c-bec7-36230b4672ba">
![image](https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/76156a6c-56ab-420d-b118-fa19f82d21d5)

### Kesimpulan
penjualan terbanyak dari tiap kategori adalah pada kategori moveis_decoracao

## b. Mencari Distribusi Penjualan Dari order_id
### Membuat categorial collumn
<img width="745" alt="Screenshot 2023-09-06 at 23 49 19" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/4aa68580-184a-406e-94d5-6ebed23dd9ca">

### Membuat grafik kriteria penjualan dari tiap kategori
<img width="488" alt="Screenshot 2023-09-06 at 23 46 54" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/6e74ce39-ddc8-4215-80f7-60f60ff846b2">
<img width="690" alt="Screenshot 2023-09-06 at 23 57 39" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/93d847b7-9635-4209-af8e-939f73b72d6b">

### Kesimpulan
Dari Histogram diatas, tidak ada data dengan distribusi normal dikarenakan variasi data yang cukup banyak didalamnya. Sehingga tidak bisa melakukan pencarian distribusi dari penjualan


## c. Analisis korelasi pada product dan seller
### Analisa korelasi order
<img width="673" alt="Screenshot 2023-09-06 at 23 53 11" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/32a5dda4-0678-4783-aa9f-0ae76bb59da2">
<img width="631" alt="Screenshot 2023-09-06 at 23 56 49" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/862451f7-a068-4643-99af-a66cf2b74dff">


### Kesimpulan
ditemukan korelasi positif antara freight value dengan price yang menandakan semakin banyak produk yang dibeli, maka semakin tinggi freight value yang dihasilkan membuat price semakin meningkat.

### Analisa korelasi seller
<img width="668" alt="Screenshot 2023-09-06 at 23 54 27" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/3c048b7b-bdf3-4a86-ad4f-fed23a0b1791">
<img width="720" alt="Screenshot 2023-09-06 at 23 57 10" src="https://github.com/hendsaputra/Data-Wrangling-and-SQL-Pacmann---E-commerce-analysis-/assets/136609782/5765fbdb-7b22-4713-831c-eb5e75754ef3">

### Kesimpulan
Terdapat korelasi positif antara zip_code_prefix dengan freight_value yang menandakan bahwa lokasi menentukan seberapa besar nilai freight_value












