# GPIO 1
Program pertama akan digunakan untuk membuat blink dengan interval 100ms, 1 detik, 2 detik, dan 3 detik sekali.

1. Alat dan Bahan
   * ESP32             ==> 1 buah
   * LED               ==> 1 buah
   * Resistor 220 Ohm  ==> 1 buah
   * Resistor 10k Ohm  ==> 1 buah
   * Push button       ==> 1 buah

2. Rangkaian

   ![image](https://github.com/alfan459/Embedded-System/assets/54757609/4850f38f-859e-461b-a830-cd9b53a8e40e)

3. Program

    ![beautify-picture (2)](https://github.com/JustBadrun/Embeded_System/assets/128286595/a4125fea-f606-4737-bbac-69fee09ddece)

4. Flowchart

   ![Flowchart1](https://github.com/alfan459/Embedded-System/assets/54757609/3062ca6a-98dd-441c-8fe5-7019fac6f825)

5. Hasil dan Pembahasan

   https://github.com/JustBadrun/Embeded_System/assets/128286595/a0d04c5c-72f7-4751-bc99-6c04fcde8f4c

   Kode di atas adalah program untuk mengendalikan LED dengan menggunakan ESP32. Berikut adalah penjelasan singkat untuk setiap bagian dari kode tersebut:

  * Inisialisasi PIN dan Setup:
   ```cpp
   const int LedPin = 5;  // Led dihubungkan pada pin GPIO 5

   void setup() {
     pinMode(LedPin, OUTPUT);  // Inisialisasi Led sebagai OUTPUT
   }
   ```
   Kode ini menetapkan bahwa LED akan dihubungkan ke pin GPIO 5 dan menginisialisasi pin tersebut sebagai output di dalam fungsi `setup()`. Fungsi `setup()` dijalankan sekali pada awal program.

  * Loop Utama:
   ```cpp
   void loop() {
     // Nyala 100ms dan mati selama 1 detik
     digitalWrite(LedPin, HIGH);
     delay(100);
     digitalWrite(LedPin, LOW);
     delay(1000);

     // Nyala 1 detik dan mati selama 1 detik
     digitalWrite(LedPin, HIGH);
     delay(1000);
     digitalWrite(LedPin, LOW);
     delay(1000);

     // Nyala 2 detik dan mati selama 1 detik
     digitalWrite(LedPin, HIGH);
     delay(2000);
     digitalWrite(LedPin, LOW);
     delay(1000);

     // Nyala 3 detik dan mati selama 1 detik
     digitalWrite(LedPin, HIGH);
     delay(3000);
     digitalWrite(LedPin, LOW);
     delay(1000);
   }
   ```
   Bagian ini merupakan loop utama program yang akan terus diulang. Setiap iterasi loop, LED akan menyala dan mati dengan pola waktu tertentu. Pola tersebut dijelaskan sebagai berikut:
   - LED menyala selama 100ms dan mati selama 1 detik.
   - LED menyala selama 1 detik dan mati selama 1 detik.
   - LED menyala selama 2 detik dan mati selama 1 detik.
   - LED menyala selama 3 detik dan mati selama 1 detik.

   Pola ini akan terus berulang selama program berjalan di dalam fungsi `loop()`. Fungsi `delay()` digunakan untuk memberikan jeda waktu dalam milidetik antara operasi-operasi tersebut.


<br></br>

# GPIO 2
Program pertama akan digunakan untuk membuat blink 1 detik sekali menggunakan timer milis().

1. Alat dan Bahan
    * ESP32             ==> 1 buah
    * LED               ==> 1 buah
    * Resistor 220 Ohm  ==> 1 buah
    * Resistor 10k Ohm  ==> 1 buah
    * Push button       ==> 1 buah

2. Rangkaian

    ![image](https://github.com/alfan459/Embedded-System/assets/54757609/4850f38f-859e-461b-a830-cd9b53a8e40e)

3. Program

    ![beautify-picture (3)](https://github.com/JustBadrun/Embeded_System/assets/128286595/d5461284-0e4a-48e6-acf5-4b3b2b505d8d)

4. Flowchart

    ![Flowchart2](https://github.com/alfan459/Embedded-System/assets/54757609/28954bd9-7499-47e5-b546-ec70c1f35ab9)

5. Hasil dan Pembahasan

    ![GPIO 1](https://github.com/alfan459/Embedded-System/assets/54757609/d6d24241-0add-4543-a049-e1a800bf9378)

    Kode di atas merupakan program sederhana untuk mengendalikan LED dengan menggunakan platform Arduino atau mikrokontroler sejenis. Program ini menggunakan konsep *blinking* (nyala-mati secara bergantian) dengan menggunakan fungsi `millis()` untuk mengatur interval waktu. Berikut adalah penjelasan singkat untuk setiap bagian dari kode tersebut:

  * Inisialisasi PIN dan Variabel:
   ```cpp
   const int ledPin = 5;      // LED dihubungkan pada pin GPIO 5
   int ledState = LOW;        // Kondisi yang akan digunakan untuk mengatur LED
   unsigned long previousMillis = 0;  // Waktu terakhir LED dimatikan
   const long interval = 1000;        // Interval untuk blinking (milliseconds)
   ```

   Kode ini menetapkan bahwa LED akan dihubungkan ke pin GPIO 5 dan menginisialisasi variabel `ledState` sebagai `LOW` (mati), `previousMillis` sebagai `0`, dan `interval` sebagai `1000` milidetik (1 detik).

  * Setup:
   ```cpp
   void setup() {
     pinMode(ledPin, OUTPUT);  // Menginisialisasi LED sebagai Output
   }
   ```

   Fungsi `setup()` dijalankan sekali pada awal program. Di dalamnya, pin LED diinisialisasi sebagai output.

  * Loop Utama:
   ```cpp
   void loop() {
     unsigned long currentMillis = millis();

     if (currentMillis - previousMillis >= interval) {
       previousMillis = currentMillis;  // Menyimpan waktu terakhir LED ngeblink

       // Jika LED dalam keadaan mati, maka nyalakan, dan sebaliknya
       if (ledState == LOW) {
         ledState = HIGH;
       } else {
         ledState = LOW;
       }

       // Atur nyala atau mati LED sesuai dengan nilai variabel ledState
       digitalWrite(ledPin, ledState);
     }
   }
   ```

   Bagian ini merupakan loop utama program yang akan terus diulang. Setiap iterasi loop, program akan mengecek apakah sudah waktunya untuk mengubah keadaan LED (nyala atau mati) berdasarkan interval yang telah ditentukan. Fungsi `millis()` digunakan untuk menghitung waktu dalam milidetik sejak program dimulai.

     - Jika waktu sekarang (`currentMillis`) dikurangi dengan waktu terakhir LED dimatikan (`previousMillis`) lebih besar atau sama dengan interval yang ditentukan, maka:
       - Waktu terakhir LED dimatikan (`previousMillis`) diupdate.
       - Kondisi LED (`ledState`) diubah (dari mati ke nyala atau sebaliknya).
       - LED diatur sesuai dengan kondisi terkini (`ledState`) menggunakan `digitalWrite()`.
<br></br>

# GPIO 3
Program pertama akan digunakan untuk mengendalikan LED menggunakan push button.

1. Alat dan Bahan
    * ESP32             ==> 1 buah
    * LED               ==> 1 buah
    * Resistor 220 Ohm  ==> 1 buah
    * Resistor 10k Ohm  ==> 1 buah
    * Push button       ==> 1 buah

2. Rangkaian

    ![image](https://github.com/alfan459/Embedded-System/assets/54757609/4850f38f-859e-461b-a830-cd9b53a8e40e)

3. Program

    ![beautify-picture (5)](https://github.com/JustBadrun/Embeded_System/assets/128286595/9616f336-0fe5-4d59-916b-334411c46dfc)

4. Flowchart

    ![Flowchart3](https://github.com/alfan459/Embedded-System/assets/54757609/e2f8bf50-de43-4b2e-b198-aa04fa0019ef)

5. Hasil dan Pembahasan

    ![GPIO 3](https://github.com/alfan459/Embedded-System/assets/54757609/ea07038b-8f00-4882-8bbf-3fa435e164d7)

    Kode di atas merupakan program sederhana untuk mengendalikan LED menggunakan push button pada platform Arduino atau mikrokontroler sejenis. Berikut adalah penjelasan singkat untuk setiap bagian dari kode tersebut:

  * Inisialisasi PIN dan Variabel:
   ```cpp
   const int buttonPin = 4;  // Pin 4 terhubung ke push button
   const int ledPin = 5;     // Pin 5 terhubung ke LED
   int buttonState = 0;      // Variabel untuk menyimpan keadaan push button
   ```

   Kode ini menetapkan bahwa push button akan dihubungkan ke pin GPIO 4 dan LED dihubungkan ke pin GPIO 5. Variabel `buttonState` akan digunakan untuk menyimpan keadaan (HIGH atau LOW) dari push button.

  * Setup:
   ```cpp
   void setup() {
     Serial.begin(115200);       // Inisialisasi komunikasi serial pada 115200 bps
     pinMode(buttonPin, INPUT);  // Inisialisasi push button sebagai input
     pinMode(ledPin, OUTPUT);    // Inisialisasi LED sebagai output
   }
   ```

   Fungsi `setup()` dijalankan sekali pada awal program. Di dalamnya, pin untuk push button diinisialisasi sebagai input, dan pin untuk LED diinisialisasi sebagai output. Selain itu, komunikasi serial juga diinisialisasi untuk keperluan debugging.

  * Loop Utama:
   ```cpp
   void loop() {
     buttonState = digitalRead(buttonPin);    // Membaca nilai push button secara digital dan menyimpannya di variabel buttonState
     Serial.println(buttonState);             // Menampilkan nilai buttonState di serial monitor

     // Jika buttonState bernilai HIGH atau push button ditekan, maka akan menyalakan LED
     if (buttonState == HIGH) {
       digitalWrite(ledPin, HIGH);           // Menyalakan LED
     } 
     // Jika tidak ditekan, maka matikan LED
     else {
       digitalWrite(ledPin, LOW);            // Mematikan LED
     }
   }
   ```

   Bagian ini merupakan loop utama program yang akan terus diulang. Pada setiap iterasi loop, program membaca nilai dari push button menggunakan `digitalRead()` dan menyimpannya di variabel `buttonState`. Nilai `buttonState` kemudian ditampilkan di serial monitor untuk pemantauan.

   Berdasarkan nilai `buttonState`, program memutuskan apakah push button ditekan atau tidak. Jika `buttonState` bernilai `HIGH`, artinya push button ditekan, maka program akan menyalakan LED dengan menggunakan `digitalWrite(ledPin, HIGH)`. Jika tidak ditekan, maka LED dimatikan dengan menggunakan `digitalWrite(ledPin, LOW)`.
<br></br>

# GPIO 4
Program pertama akan digunakan untuk mengendalikan LED agar blink setiap 500 ms ketika push button ke-2 ditekan.

**1. Alat dan Bahan**
1. ESP32             ==> 1 buah
2. LED               ==> 2 buah
3. Resistor 220 Ohm  ==> 1 buah
4. Resistor 10k Ohm  ==> 1 buah
5. Push button       ==> 2 buah


**2. Rangkaian**
![Rangkaian GPIO 4](https://github.com/alfan459/Embedded-System/assets/54757609/389106d1-e4a8-41c3-8bed-ea941e62d3db)


**3. Program**

Program dapat dilihat pada folder berikut ini: <a href="https://github.com/alfan459/Embedded-System/tree/master/Jobsheet%201%20Dasar%20Pemrograman%20ESP32/a.%20GPIO/Blink%20500ms%202%20led%202%20button"> Program </a>

**4. Hasil dan Pembahasan**

![GPIO 4](https://github.com/alfan459/Embedded-System/assets/54757609/5c06b0e8-8ff4-441a-baa4-7ff00b3c4a38)

![carbon (4)](https://github.com/alfan459/Embedded-System/assets/54757609/1bd6a672-4911-4fd1-aba6-b61ed23a02a3)

![Flowchart4](https://github.com/alfan459/Embedded-System/assets/54757609/f07744f4-de61-4698-a3f8-3103998632a0)


Program dimulai dengan inisialisasi variable
- `button1` dan `button2` (pin 4 dan pin 2) adalah pin yang terhubung ke dua push button.
- `led1` (pin 5) dan `led2` (pin 18) adalah pin yang terhubung ke dua buah LED.
- `buttonState1` dan `buttonState2` adalah variabel yang akan digunakan untuk menyimpan status (HIGH atau LOW) dari dua push button.
- `ledState` adalah variabel yang akan digunakan untuk mengendalikan status LED.
- `previousMillis` digunakan untuk menyimpan waktu terakhir LED ngeblink.
- `interval` adalah interval waktu (dalam milidetik) untuk blink LED (500 ms).

Dalam blok `setup()`, program menginisialisasi pin-pin yang digunakan:
   - `button1` dan `button2` diatur sebagai input (untuk membaca push button).
   - `led1` dan `led2` diatur sebagai output (untuk mengendalikan LED).

Dalam blok `loop()`, program melakukan beberapa tugas berulang kali:
   - `currentMillis` diisi dengan waktu sekarang menggunakan `millis()`. Ini digunakan untuk menghitung interval waktu.
   - Program kemudian membaca kondisi `button1` dan `button2` menggunakan `digitalRead()`. Ini akan menghasilkan nilai HIGH jika push button ditekan, dan LOW jika tidak.
   - Selanjutnya, program melakukan dua tugas berdasarkan kondisi push button:
   - Jika `button1` (push button pertama) ditekan, maka `digitalWrite(led1, HIGH)` akan dijalankan untuk menyalakan LED pertama.
   - Jika tidak, maka `digitalWrite(led1, LOW)` akan dijalankan untuk mematikan LED pertama.
   - Jika `button2` (push button kedua) ditekan, maka program akan membuat LED1 dan LED2 berkedip dengan interval 500 ms menggunakan variabel `ledState` dan `previousMillis`.


**5. Kesimpulan**

Program ini mengendalikan dua LED (led1 dan led2) dengan dua tombol (button1 dan button2). Ketika tombol 1 ditekan, LED 1 akan menyala, dan ketika tombol 2 ditekan, LED 2 akan menyala secara berkedip. Program akan terus berjalan dalam loop dan memeriksa keadaan tombol serta mengendalikan LED sesuai dengan input dari tombol.


<br></br>

# GPIO 5
Program pertama akan digunakan untuk membuat LED menyala bergantian dari kiri ke kanan ketika push button ke-3 ditekan.

**1. Alat dan Bahan**
1. ESP32             ==> 1 buah
2. LED               ==> 5 buah
3. Resistor 220 Ohm  ==> 1 buah
4. Resistor 10k Ohm  ==> 1 buah
5. Push button       ==> 3 buah


**2. Rangkaian**
![Rangkaian GPIO 5](https://github.com/alfan459/Embedded-System/assets/54757609/81dfe4c2-b0fe-4576-8de2-ab5ee3ced849)


**3. Program**

Program dapat dilihat pada folder berikut ini: <a href="https://github.com/alfan459/Embedded-System/tree/master/Jobsheet%201%20Dasar%20Pemrograman%20ESP32/a.%20GPIO/Running%20Led"> Program </a>

**4. Hasil dan Pembahasan**

![GPIO 5](https://github.com/alfan459/Embedded-System/assets/54757609/e9fa7683-f447-4b10-9758-9ef9b0d55a98)


![Flowchart5](https://github.com/alfan459/Embedded-System/assets/54757609/f33ec0e3-478f-4588-b53f-67eb0437223b)

![carbon](https://github.com/alfan459/Embedded-System/assets/54757609/71f87147-f84f-484e-86d4-1162434eb07e)

Inisialisasi PIN:
   - `button1`, `button2`, dan `button3` diatur sebagai input, mewakili tiga push button yang digunakan.
   - `led1`, `led2`, `led3`, `led4`, dan `led5` diatur sebagai output, mewakili lima buah LED yang dikendalikan.

Variabel:
   - `buttonState1`, `buttonState2`, dan `buttonState3` digunakan untuk menyimpan keadaan (HIGH atau LOW) dari push button.
   - `ledState` digunakan untuk menyimpan keadaan (HIGH atau LOW) dari LED yang berkedip.
   - `previousMillis` menyimpan waktu terakhir LED berkedip.
   - `interval` menentukan interval waktu berkedipnya LED (dalam milidetik).

Setup
   - Menetapkan PIN sebagai input atau output sesuai kebutuhan.

Loop:
   - Membaca keadaan dari tiga push button.
   - Jika `button1` ditekan, maka `led1` akan menyala.
   - Jika `button2` ditekan, maka `led1` dan `led2` akan berkedip dengan interval waktu tertentu.
   - Jika `button3` ditekan, maka kelima LED (`led3`, `led4`, dan `led5`) akan menyala secara berurutan dari kiri ke kanan dan sebaliknya.

Running LED:
   - Bagian ini dijalankan jika `button3` ditekan.
   - LED3, LED4, dan LED5 akan menyala secara berurutan dari kiri ke kanan dan sebaliknya dengan interval waktu tertentu.


**5. Kesimpulan**

Program ini menciptakan efek visual yang menarik dengan mengendalikan LED berdasarkan input dari push button, yang dapat digunakan dalam proyek-proyek berbasis mikrokontroler.
