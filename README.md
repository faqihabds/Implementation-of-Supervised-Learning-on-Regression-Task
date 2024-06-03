# Data Analytics COVID-19 di Indonesia
Data Analytics COVID-19 di Indonesia dengan menggunakan menggunakan Excel dan Tableau.

# About The Project
Data Analytics COVID-19 di Indonesia adalah analisis data yang berfokus pada banyaknya jumlah terkena dan teratasi kasus COVID-19 di Indonesia, menggunakan Excel dan Tableu untuk memberikan wawasan dan pengambilan keputusan.

# Dataset 
Dataset yang digunakan adalah dataset COVID-19 Indonesia Dataset yang dapat diakses melalui [Kaggle](https://www.kaggle.com/datasets/hendratno/covid19-indonesia).

## Tentang Dataset

### Konteks
Dataset COVID-19 di Indonesia dibuat untuk mengetahui berbagai faktor yang dapat dipertimbangkan dalam pengambilan keputusan terkait tingkat ketatnya kebijakan di setiap provinsi di Indonesia.

### Konten
Data dikompilasi berdasarkan deret waktu, baik pada tingkat negara (Indonesia), maupun pada tingkat provinsi. Jika diperlukan di provinsi tertentu, data juga mungkin disediakan pada tingkat kota/kabupaten.

Data demografis juga tersedia, serta perhitungan antara data demografis dan data pandemi COVID-19.

### Pengakuan
Terima kasih kepada mereka yang telah menyediakan data secara terbuka sehingga kami dapat mengompilasinya menjadi dataset di sini, yaitu: covid19.go.id, kemendagri.go.id, bps.go.id, dan bnpb-inacovid19.hub.arcgis.com

# Data Cleaning
Setelah mengimpor file CSV yang telah diunduh ke dalam Excel, langkah pertama dalam proses data cleaning adalah dalam proses data cleaning adalah menghapus kolom yang tidak relevan untuk analisis lebih lanjut. 

Kolom-kolom yang dihapus termasuk `Location Level`, `City or Regency`, `Continent`, `Time Zone`, `Special Status`, `Total Regencies`, `Total Cities`, `Total Districts`, `Total Urban Villages`, `Total Rural Villages`, `Area (km2)`, `Population Density`, `Longitude`, `Latitude`, `New Cases per Million`, `Total Cases per Million`, `Growth Factor of New Cases`, dan `Growth Factor of New Deaths`. 

Setelah itu, kolom `Date` dipisahkan menjadi tiga kolom terpisah yaitu `Date`, `Month`, dan `Year` untuk memudahkan analisis berdasarkan waktu. Kolom `DMY` ditambahkan untuk menyimpan kombinasi hari dan bulan dalam format `dd-mmm`. 

Kolom yang dipertahankan dan dibersihkan termasuk `Date`, `Month`, `Year`, `DMY`, `Location ISO Code`, `Location`, `New Cases`, `New Deaths`, `New Recovered`, `New Active Cases`, `Total Cases`, `Total Deaths`, `Total Recovered`, `Total Active Cases`, `Province`, `Country`, `Island`, `Population`, `New Deaths per Million`, `Total Deaths per Million`, `Total Deaths per 100rb`, `Case Fatality Rate`, dan `Case Recovered Rate`. 


Hasil dari proses data cleaning dapat diakses di file Excel yang disimpan dalam repository dengan nama file [covid dataset.xlsx](covid%20dataset.xlsx). 

File Excel ini berisi dataset COVID-19 Indonesia yang telah dibersihkan dan siap untuk digunakan dalam analisis lebih lanjut.

# Visualisasi Data
Visualisasi data dilakukan menggunakan Tableau Public. 

Dashboard
![Dashboard](dashboard_data_analyst_covid.png)

Total case terbanyak terjadi di DKI Jakarta dengan jumlah lebih dari 500 juta.
![Dashboard](Total_case_terbanyak.png)

Total Death terbanyak terjadi di Jawa Timur dengan jumlah lebih dari 15 juta.
![Dashboard](Total_Death_terbanyak.png)

Dashboard visualisasi lengkap dapat dilihat di [Tableau Public - COVID-19 di Indonesia Dashboard](https://public.tableau.com/app/profile/muhammad.faqih.abdussalam/viz/Covid-19diIndonesia_17168070835390/Dashboard1).

## Analisis Data
Dari data yang telah dianalisis, beberapa temuan menarik dapat diidentifikasi:

- **Total Kasus Terbanyak**: DKI Jakarta menjadi provinsi dengan total kasus COVID-19 terbanyak, mencapai lebih dari 500 juta kasus.
- **Total Kematian Terbanyak**: Jawa Timur memiliki jumlah kematian terbanyak akibat COVID-19, dengan lebih dari 15 juta kematian.
- **Puncak Kasus Terkena dan Meninggal**: Puncak kasus terkena dan meninggal terbanyak terjadi pada tahun 2022.
- Dari data yang telah dianalisis, terjadi penurunan kasus COVID-19 baik di DKI Jakarta maupun Jawa Timur pada tahun 2024. Meskipun demikian, perhatian terhadap pencegahan dan penanganan tetap diperlukan untuk mencegah lonjakan kasus di masa mendatang.

## Keputusan yang Disarankan
Berdasarkan penurunan kasus COVID-19, beberapa keputusan yang dapat disarankan adalah:

1. **Pemeliharaan Protokol Kesehatan**: Meskipun kasus menurun, tetap diperlukan pemeliharaan protokol kesehatan untuk mencegah penyebaran virus.
2. **Penguatan Sistem Kesehatan**: Pemerintah perlu memperkuat sistem kesehatan, terutama di DKI Jakarta dan Jawa Timur, untuk menghadapi potensi lonjakan kasus di masa mendatang.
3. **Edukasi Masyarakat**: Edukasi dan sosialisasi mengenai pentingnya protokol kesehatan masih perlu ditingkatkan untuk memastikan kesadaran masyarakat tetap tinggi.

Keputusan yang diambil harus tetap berdasarkan pada data aktual dan kajian yang mendalam, serta melibatkan partisipasi aktif dari berbagai pihak terkait.
