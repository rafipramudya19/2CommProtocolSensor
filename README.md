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

https://user-images.githubusercontent.com/121251478/209265768-ea191d2f-6554-4676-b204-a2470e2f6ecc.mp4

Analisa : <br />
Dari contoh daiatas ESP32 dapat digunakan sebagai Touch Sensor dimana saat kabel jumper disentuh maka akan menghasilkan data pada serial plotter seperti pada video diatas. Ketika sensor(kabel) tidak disentuh nilai pada serial plotter akan tinggi sedangkan saat sensor(kabel) disentuh maka serial plotter akan rendah

**Kemudian Buatlah Rangkaian dibawah ini** <br />
![image](https://user-images.githubusercontent.com/41616849/209115047-caf5c1ad-eff1-460f-a123-e68a182a7acd.png)  <br />

**Keluaran** <br />
a) Lampu LED On saat disentuh dan Off saat tidak disentuh <br />


https://user-images.githubusercontent.com/121251478/209265860-a2643655-d566-4e66-b180-649515b41937.mp4



Analisa : <br />
Dari data contoh diatas kita dapat implementasikan nilai serial plotter untuk menghidupkan dan menyalkan lampu LED dengan perintah if else pada program yang menghasilkan LED akan menyala ketika sensor disentuh dan akan mati ketika sensor tidak disentuh. <br />

b) Lampu LED akan menyala Blink saat disentuh <br />


https://user-images.githubusercontent.com/121251478/209265892-10149b46-f436-4bfc-b561-988f854591ae.mp4


Analisa : <br />
Untuk percobaan kali ini masih mengimplementasikan hasil serial plotter hanya saja pada programnya dapat diatur seingga ketika sensor disentuh maka LED akan menyala BLINK dan mati ketika sensor tidak disentuh. <br />

c) Ketika LED menyala Serial Monitor akan menampilkan angka yang bertambah tiap kali sensor disntuh <br />


https://user-images.githubusercontent.com/121251478/209265917-632c3872-86b4-4944-93d0-c0514e0f9685.mp4


Analisa : <br />
Percobaan kali ini menghasilkan data ketika sensor disentuh maka akan mengirimkan data untuk menambahkan angka yang akan tampil pada serial monitor. <br />

d) Lampu LED akan menyala Running saat sensor disentuh <br />



https://user-images.githubusercontent.com/121251478/209265942-5b888906-8415-429a-96a7-e031ec9f65b8.mp4



Analisa : <br />
Pada percobaan ini program diubah sehingga ketika sensor disentuh maka LED akan menyala running dari kiri ke kanan, kemudian kanan ke kiri secara kontinyue <br />

**2) DHT 11 Sensor** <br />
Pada Percobaan kali ini digunakan sensor suhu dan kelembapan DHT 11 yang dapat menghasilkan data sehingga dapat disimpan pada ESP32. Untuk rangkaiannya seperti ini <br />
![image](https://user-images.githubusercontent.com/41616849/209120548-e0bac69c-7d9b-4002-87f5-0a7e16526ae0.png) <br />
rangkaian diatas kemudian ditambah buzzer yang akan menyala saat sensor membaca suhu 30 derajat celcius dan 3 buah LED yang akan menyala running saat suhu dibawah 30 derajat celcius <br />


https://user-images.githubusercontent.com/121251478/209265960-b280b5bf-4671-4dc7-b763-9e6522d22cea.mp4


Analisa : <br />
Dengan data yang didapat sensor DHT 11 kita dapat membuat program dengan untuk memberikan sebuah state pada keadaan tertentu. <br />

**3) Sensor RFID**

**Buatlah rangkaian seperti berikut**

![image](https://user-images.githubusercontent.com/41616849/209123901-b261bf28-8be5-443a-aadf-cb393fa20e94.png)


Keluaran 

![image](https://user-images.githubusercontent.com/41616849/209123721-e27870b9-23ab-4e33-afd5-f146bd19903d.png)


**Kondisi apabila Tag RFID didekatkan pada Reader, maka LED Hijau akan menyala, servo akan bergerak ke kanan (lalu kembali ke posisi semula setelah 3 detik) dan di Serial Monitor akan tertampil pesan “Akses Diterima, Silahkan Masuk”. Apabila Tag RFID tidak dikenali, maka LED Merah akan menyala, servo tidak bergerak dan di Serial Monitor akan tertampil pesan “Akses Ditolak”**

Keluaran 






