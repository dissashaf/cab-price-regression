# Cab Price Prediction using Regression
**Exercises**  
_R. Dissa | May 9, 2023_

**Objektif:**

Proyek ini merupakan analisis serta prediksi untuk perusahaan kompetitor berbasis transportasi. Tujuan dari proyek ini adalah untuk mengembangkan model prediksi dari data transportasi berbasis aplikasi yakni Uber dan Lyft; untuk memprediksi harga tarif berdasarkan atribut yang diberikan. Atribut atau fitur tersebut diantara lain; tipe kendaraan, jarak, lokasi penjemputan, lokasi tujuan, kenaikan harga, serta waktu, dimana data merupakan data yang diambil dari kota Boston, Massachusetts pada tahun 2018.

**Problem Statement:**

Industri transportasi berbasis aplikasi telah berkembang pesat dalam dekade terakhir. Diperlukannya strategi untuk dapat mengoptimalkan harga agar tetap kompetitif di pasar. Uber dan Lyft memiliki model penetapan harga yang berbeda yang diasumsikan berdasarkan cab, *rush hour*, jarak, dan sebagainya. Diperlukan model *machine learning* untuk memprediksi harga tarif dengan akurasi yang tinggi. Prediksi harga tarif sangat penting untuk mengoptimalkan strategi penetapan harga, meningkatkan pendapatan, serta meningkatkan kepuasan pelanggan.

Dataset yang akan digunakan mencakup atribut sebagai berikut:

* distance: the distance between pickup and drop-off locations in miles.
* cab_type: the type of cab (Uber or Lyft).
* name: Name of the product used in the ride             
* surge_multiplier: Surge multiplier for the ride    
* destination: the drop-off location.
* source: the pickup location.
* price: the fare price for the ride.

Dataset ini memiliki 693.071 baris data. Data diambil dari tanggal 26 November 2018 hingga 18 Desember 2018, atau memiliki kisaran kurang lebih tiga minggu. Tujuan kami adalah untuk mengembangkan model yang dapat memprediksi harga tarif dengan akurasi tinggi berdasarkan atribut lain yang tersedia dalam dataset. Akurasi model akan dievaluasi menggunakan metrik evaluasi yang tepat, seperti Root *Mean Square Error* (RMSE), Mean *Absolute Error* (MAE), atau *R-squared (R2) score*.

Sementara deskripsi kolom pada dataset yang **belum** difilter adalah sebagai berikut:

| Column              | Description                                      |
|---------------------|--------------------------------------------------|
| id                  | Unique identifier for each column                |
| timestamp           | Unix timestamp of the ride start time            |
| hour                | Hour of the day when the ride started            |
| day                 | Day of the week when the ride started            |
| month               | Month of the year when the ride started          |
| datetime            | Date value of the ride start time                 |
| timezone            | Timezone of the ride start location              |
| source              | Initial source location of the ride              |
| destination         | Destination location of the ride                  |
| cab_type            | The type of cab used for the ride                  |
| product_id          | Unique identifier for the product used in the ride|
| name                | Name of the product used in the ride              |
| price               | Price of the ride                                 |
| distance            | Total distance of the requested ride              |
| surge_multiplier    | Surge multiplier for the ride                      |
| latitude            | Latitude of the ride start location                |
| longitude           | Longitude of the ride start location               |
| temperature         | Temperature at the ride start location             |
| apparentTemperature | Apparent temperature at the ride start location    |
| short_summary       | Short summary of the weather at the ride start location|
| long_summary        | Long summary of the weather at the ride start location |
| precipIntensity     | Precipitation intensity at the ride start location  |
| precipProbability   | Precipitation probability at the ride start location|
| humidity            | Humidity at the ride start location                 |
| windSpeed           | Wind speed at the ride start location                |
| windGust            | Wind gust at the ride start location                 |
| windGustTime        | Time of wind gust at the ride start location          |
| visibility          | Visibility at the ride start location                |
| temperatureHigh     | Highest temperature on the day of the ride start     |
| temperatureHighTime | Time of highest temperature on the day of the ride start|
| temperatureLow      | Lowest temperature on the day of the ride start      |
| temperatureLowTime  | Time of lowest temperature on the day of the ride start |
| apparentTemperatureHigh | Highest apparent temperature on the day of the ride start|
| apparentTemperatureHighTime | Time of highest apparent temperature on the day of the ride start|
| apparentTemperatureLow  | Lowest apparent temperature on the day of the ride start |
| apparentTemperatureLowTime | Time of lowest apparent temperature on the day of the ride start |
| icon                | Weather icon at the ride start location             |
| dewPoint            | Dew point at the ride start location                 |
| pressure            | Pressure at the ride start location                  |
| windBearing         | Wind bearing at the ride start location              |
| cloudCover          | Cloud cover at the ride start location                |
| uvIndex             | UV index at the ride start location                   |
| visibility.1        | Visibility at the ride start location (duplicate column)|
| ozone               | Ozone at the ride start location                      |
| sunriseTime         | Time of sunrise at the ride start location            |
| sunsetTime          | Time of sunset at the ride start location             |
| moonPhase           | Moon phase at the ride start location                  |
| precipIntensityMax  | Maximum precipitation intensity on the day of the ride start|
| uvIndexTime         | Time of UV index at the ride start location              |
| temperatureMin      | Lowest temperature on the day of the ride start           |
| temperatureMinTime  | Time of lowest temperature on the day of the ride start    |