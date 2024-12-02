**Exercise 8: Using Semaphores to Protect Critical Sections**

**Tujuan**

Untuk menunjukkan cara menghilangkan kontensi sumber daya dengan cara selektif menggunakan semaphore untuk melindungi bagian kode kritis.

**Peralatan**

1. STM32103C8T6
2. STM32CubeIDE.
3. FreeRTOS library.
4. Debugger
5. LED

**Langkah Percobaan**
Inisialisasi dan Konfigurasi:

1. Konfigurasi GPIO untuk mengendalikan LED (Green, Red, Blue, Orange).
2. Inisialisasi sistem FreeRTOS di CubeMX.
3. Tambahkan semaphore untuk melindungi kode akses bersama (Critical Resource).
4. Pastikan FreeRTOS diatur untuk menggunakan semaphore dan task.
5. Definisikan semaphore untuk melindungi akses ke bagian kode yang kritis (misalnya, CriticalResourceSemaphore).
6. Setelah semua task dan semaphore didefinisikan, lakukan build dan flashing ke board STM32.
7. Observasi LED behavior yang menunjukkan tidak adanya kontensi sumber daya—Blue LED tidak akan menyala, menandakan bahwa semua task berfungsi tanpa konflik.

**Hasil Percobaan**
1. Task berjalan tanpa gangguan
   

https://github.com/user-attachments/assets/58a309cf-3266-4fda-9988-33b0f4ffadcc


2. Percobaan menggunakan WaitTimeMilliseconds diatur menjadi 0


https://github.com/user-attachments/assets/fa8f8e59-e06f-49d4-82f6-d3517c8c98a9

