# B. Transmisi Data Menggunakan Protokol HTTP

## 1. Keterangan Singkat (Abstrak)
<p align="justify">Percobaan ini dimulai dengan pembuatan database lokal "banjir_db" dan tabel "smartwater" menggunakan phpMyAdmin. Lalu diberikan kode JSON untuk flow program Multi-Protocol IoT Server yang perlu diimport di Node-RED. Selanjutnya, melalui program pada ESP32 dilakukan transmisi data dummy ke Node-Red menggunakan protokol HTTP metode GET dan protokol HTTP metode POST. Output dari percobaan ini berupa hasil dari serial monitor, debugging Node-Red, dan tampilan dashboard Node-RED.
   
## 2. Alat dan Bahan
1. Node-RED
2. ESP32
3. XAMPP

## 3. Source Code

1. Code JSON Multi-Protocol IoT Server dapat dilihat <a href="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/flow%20program%20Multi-Protocol%20IoT.json">disini</a>
2. Program ESP32 transmisi data dummy menggunakan protokol HTTP metode GET dapat dilihat <a href="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/transmisi_data_dummy_keNode-Red_protokol_HTTP_metode_Get/transmisi_data_dummy_keNode-Red_protokol_HTTP_metode_Get.ino">disini</a>
3. Program ESP32 transmisi data dummy menggunakan protokol HTTP metode POST dapat dilihat <a href="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/transmisi_data_dummy_ke_Node-Red_protokol_HTTP_metode_POST/transmisi_data_dummy_ke_Node-Red_protokol_HTTP_metode_POST.ino">disini</a>

## 4. Flow Program
<img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/flow%20program%20.png" width="800">

## 5. Hasil Percobaan Transmisi Data Dummy Menuju Node-Red Menggunakan Protokol HTTP Metode GET

1. Flow chart program ESP32
   
   <img src="https://github.com/brianrahma/system-embedded/assets/82065700/02604bf3-6f4b-43d2-972e-67b6389b2692" width="400">
   
2. Output serial monitor
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/serial%20monitor-metode%20get.png" width="600">
   
3. Debug Node-RED
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/debug-metode%20GET.png" height="500">
   
4. Dashboard Node-RED
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/dashboard-metode%20get.png" width="700">
   
5. Tabel database MySQL
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/tabel%20smartwater-metode%20get.png" width="500">

## 6. Hasil Percobaan Transmisi Data Dummy Menuju Node-Red Menggunakan Protokol HTTP Metode POST
1. Flow chart program ESP32
   
   <img src="https://github.com/brianrahma/system-embedded/assets/82065700/2695c115-65ec-401f-a5e3-c4c076658693" width="400">

2. Output serial monitor
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/serial%20monitor-metode%20POST.png" width="600">
   
3. Debug Node-RED
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/debug-metode%20POST.png" height="300">
   
4. Dashboard Node-RED
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/dashboard-metode%20POST.png" width="700">
