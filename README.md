# ESP32_CommProtocolSensor

ESP32 adalah nama dari mikrokontroler yang dirancang oleh perusahaan yang berbasis di Shanghai, China yakni Espressif Systems. ESP32 menawarkan solusi jaringan WiFi dan BLE. ESP32 menggunakan prosesor dual core yang berjalan di instruksi Xtensa LX16. Selain itu, ESP32 telah mendukung protokol komunikasi seperti I2C, UART dan SPI.

**ALAT DAN BAHAN**
1) ESP32
2) Breadboard
3) Kabel jumper
4) Sensor DHT 11, RFID
5) LED (5) dan Push Button (3)
6) Servo
7) Resistor 330,1K, 10K Ohm (@ 3)

**HASIL KELUARAN**

**1) ESP32 Capacitive Touch Sensor**

**Contoh**



https://user-images.githubusercontent.com/121251478/209267521-7a3cf69d-dfaf-4957-8ee5-8cb092198c56.mp4



Analisa : <br />
Dari contoh daiatas ESP32 dapat digunakan sebagai Touch Sensor dimana saat kabel jumper disentuh maka akan menghasilkan data pada serial plotter seperti pada video diatas. Ketika sensor(kabel) tidak disentuh nilai pada serial plotter akan tinggi sedangkan saat sensor(kabel) disentuh maka serial plotter akan rendah

**Kemudian Buatlah Rangkaian dibawah ini** <br />
![rangkaian1](https://user-images.githubusercontent.com/121251478/209268393-dfbf6276-c088-42fc-bb0a-81aa679456a3.png)
<br />

**Keluaran** <br />
a) Lampu LED On saat disentuh dan Off saat tidak disentuh <br />


https://user-images.githubusercontent.com/121251478/209267706-164b2cad-2277-41c5-8830-8a242d27ddd4.mp4


Analisa : <br />
Dari data contoh diatas kita dapat implementasikan nilai serial plotter untuk menghidupkan dan menyalkan lampu LED dengan perintah if else pada program yang menghasilkan LED akan menyala ketika sensor disentuh dan akan mati ketika sensor tidak disentuh. <br />

b) Lampu LED akan menyala Blink saat disentuh <br />


https://user-images.githubusercontent.com/121251478/209267750-514fdc03-617f-439f-8576-a2a431fde218.mp4


Analisa : <br />
Untuk percobaan kali ini masih mengimplementasikan hasil serial plotter hanya saja pada programnya dapat diatur seingga ketika sensor disentuh maka LED akan menyala BLINK dan mati ketika sensor tidak disentuh. <br />

c) Ketika LED menyala Serial Monitor akan menampilkan angka yang bertambah tiap kali sensor disntuh <br />


https://user-images.githubusercontent.com/121251478/209267789-60e9ad3f-cf14-4195-ad2d-5a98f582ac70.mp4


Analisa : <br />
Percobaan kali ini menghasilkan data ketika sensor disentuh maka akan mengirimkan data untuk menambahkan angka yang akan tampil pada serial monitor. <br />

d) Lampu LED akan menyala Running saat sensor disentuh <br />


https://user-images.githubusercontent.com/121251478/209267852-b4cec21d-9ea7-4a6f-943a-158935a5acbd.mp4


Analisa : <br />
Pada percobaan ini program diubah sehingga ketika sensor disentuh maka LED akan menyala running dari kiri ke kanan, kemudian kanan ke kiri secara kontinyue <br />

**2) DHT 11 Sensor** <br />
Pada Percobaan kali ini digunakan sensor suhu dan kelembapan DHT 11 yang dapat menghasilkan data sehingga dapat disimpan pada ESP32. Untuk rangkaiannya seperti ini <br />
![rangkaian2](https://user-images.githubusercontent.com/121251478/209268461-f4c80920-d443-4e8c-ac54-d66377b2a4c1.png)
<br />
rangkaian diatas kemudian ditambah buzzer yang akan menyala saat sensor membaca suhu 30 derajat celcius dan 3 buah LED yang akan menyala running saat suhu dibawah 30 derajat celcius <br />


https://user-images.githubusercontent.com/121251478/209267885-df8874d1-d4ee-4b1f-84e9-be683c4937cc.mp4


Analisa : <br />
Dengan data yang didapat sensor DHT 11 kita dapat membuat program dengan untuk memberikan sebuah state pada keadaan tertentu. <br />

**3) Sensor RFID**

**Buatlah rangkaian seperti berikut**


![rangkaian3](https://user-images.githubusercontent.com/121251478/209268482-66693de2-931e-477d-a94c-2f8bbcf69486.png)


Keluaran 

![keluaran](https://user-images.githubusercontent.com/121251478/209268495-bbcca170-46a8-4be8-9f27-8ff71e120e6d.png)


**Kondisi apabila Tag RFID didekatkan pada Reader, maka LED Hijau akan menyala, servo akan bergerak ke kanan (lalu kembali ke posisi semula setelah 3 detik) dan di Serial Monitor akan tertampil pesan “Akses Diterima, Silahkan Masuk”. Apabila Tag RFID tidak dikenali, maka LED Merah akan menyala, servo tidak bergerak dan di Serial Monitor akan tertampil pesan “Akses Ditolak”**

Keluaran 






