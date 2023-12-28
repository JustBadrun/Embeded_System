# C. Transmisi Data Menggunakan Protokol MQTT

## 1. Keterangan Singkat (Abstrak)
<p align="justify">Dalam percobaan ini, program ESP32 memanfaatkan protokol MQTT untuk mentransmisikan data dummy, seperti level, rainfall, dan flow. Server broker MQTT yang digunakan adalah layanan EMQ X, yang merupakan platform perangkat lunak open-source untuk implementasi MQTT. Setelah program diupload, dilakukan pemantauan melalui serial monitor untuk memastikan koneksi dan debug pada Node-Red. Hasil output dari percobaan ini meliputi data yang dipublikasikan ke topik "flood/node1", serta visualisasi data pada dashboard Node-Red.
   
## 2. Alat dan Bahan
1. Node-RED
2. ESP32
3. XAMPP

## 3. Source Code

1. Code JSON Multi-Protocol IoT Server dapat dilihat <a href="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/flow%20program%20Multi-Protocol%20IoT.json">disini</a>
2. Program ESP32 dapat dilihat <a href="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/C.%20Transmisi%20Data%20Menggunakan%20Protokol%20MQTT/program/program.ino">disini</a>

## 4. Flow Program
<img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/flow%20program%20.png" width="800">

## 5. Hasil Percobaan

1. Flow chart program ESP32
   
   <img src="https://github.com/brianrahma/system-embedded/assets/82065700/4a5c4459-cc58-41a6-9b6b-97faec768516" height="700">
   
2. Output serial monitor
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/C.%20Transmisi%20Data%20Menggunakan%20Protokol%20MQTT/serial%20monitor.png" width="600">
   
3. Debug Node-RED
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/C.%20Transmisi%20Data%20Menggunakan%20Protokol%20MQTT/debug.png" height="400">
   
4. Dashboard Node-RED
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/C.%20Transmisi%20Data%20Menggunakan%20Protokol%20MQTT/dashboard.png" width="800">
   
5. Tabel database MySQL
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/C.%20Transmisi%20Data%20Menggunakan%20Protokol%20MQTT/database.png" width="500">
