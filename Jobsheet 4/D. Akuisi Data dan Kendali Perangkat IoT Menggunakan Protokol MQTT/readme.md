# D. Akuisi Data dan Kendali Perangkat IoT Menggunakan Protokol MQTT

## 1. Keterangan Singkat (Abstrak)
<p align="justify">Dalam percobaan ini program ESP32 menggunakan protokol MQTT untuk mengakuisisi data sensor dan mengendalikan perangkat, seperti LED, melalui topik-topik MQTT. Setelah program diupload, dilakukan pemantauan melalui serial monitor dan dashboard Node-Red untuk mengendalikan nyala LED melalui tombol switch pada dashboard. Program yang kedua merupakan pengendalian LED ESP32 menggunakan layanan Adafruit MQTT, dalam hal ini pengendalian LED melalui dashboard yang ada di laman Adafruit.
   
## 2. Alat dan Bahan
1. Node-RED
2. Laman Adafruit
3. ESP32
4. Kabel jumper
5. LED
6. XAMPP

## 3. Source Code

1. Code JSON Multi-Protocol IoT Server dapat dilihat <a href="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/flow%20program%20Multi-Protocol%20IoT.json">disini</a>
2. Program-1 ESP32 (kontrol nyala LED melalui dashboard Node-RED) dapat dilihat <a href="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/D.%20Akuisi%20Data%20dan%20Kendali%20Perangkat%20IoT%20Menggunakan%20Protokol%20MQTT/program1/program1.ino">disini</a>
3. Program-2 ESP32 (kontrol nyala LED melalui dashboard Adafruit) dapat dilihat <a href="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/D.%20Akuisi%20Data%20dan%20Kendali%20Perangkat%20IoT%20Menggunakan%20Protokol%20MQTT/program2/program2.ino">disini</a>

## 4. Flow Program
<img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/B.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/flow%20program%20.png" width="800">

## 5. Hasil Percobaan Kontrol Nyala LED Melalui Dashboard Node-RED

1. Flow chart program ESP32
   
   <img src="https://github.com/brianrahma/system-embedded/assets/82065700/6d63519d-f4b5-4fc5-b70b-da925b0001ee" width="300">
   
2. Dokumentasi
   
   ![C2 -GIF](https://github.com/brianrahma/system-embedded/assets/82065700/b295425b-ba4a-4c29-b98b-77674c732489)

4. Output serial monitor
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/D.%20Akuisi%20Data%20dan%20Kendali%20Perangkat%20IoT%20Menggunakan%20Protokol%20MQTT/serialmonitor1.png" width="600">

5. Debug Node-RED
   
   <img src="https://github.com/brianrahma/system-embedded/assets/82065700/6f42ea1e-cc21-48d6-8e28-a84fb027c729" height="500">
   
6. Dashboard Node-RED
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/D.%20Akuisi%20Data%20dan%20Kendali%20Perangkat%20IoT%20Menggunakan%20Protokol%20MQTT/dashboard1.png" width="700">

## 6. Hasil Percobaan Kontrol Nyala LED Melalui Dashboard Adafruit
1. Flow chart program ESP32

   <img src="https://github.com/brianrahma/system-embedded/assets/82065700/9986c798-6e72-4c3d-b454-1c55d0c21d70" width="500">

2. Dokumentasi
   
   ![C2 -GIF-2](https://github.com/brianrahma/system-embedded/assets/82065700/70dc304c-4c16-4d59-b78d-903ae099e480)

4. Output serial monitor
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/D.%20Akuisi%20Data%20dan%20Kendali%20Perangkat%20IoT%20Menggunakan%20Protokol%20MQTT/serialmonitor2.png" width="600">
   
5. Widget On/Off Adafruit
   
   <img src="https://github.com/brianrahma/system-embedded/blob/master/jobsheet%204/D.%20Akuisi%20Data%20dan%20Kendali%20Perangkat%20IoT%20Menggunakan%20Protokol%20MQTT/widget-adafruit.png" width="400">
