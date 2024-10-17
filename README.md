# RTOS PRIORITY PREEMPTIVE
Program ini mengontrol dua buah LED menggunakan RTOS pada mikrokontroler STM32F103C8T6. Terdapat dua task utama: green_led dan red_led, yang masing-masing mengatur LED hijau dan merah dengan pola tertentu. Program ini juga menggunakan fungsi HAL untuk konfigurasi GPIO dan pengaturan sistem clock. RTOS scheduler digunakan untuk manajemen task multitasking yang efisien.

alur task dan hubungannya:

### Dua Task Utama:
* green_led task mengontrol LED1 dan LED2.
* red_led task mengontrol LED3 dan LED4.
  
### Multitasking dengan RTOS:
Kedua task berjalan secara independen dan dikelola oleh RTOS scheduler.

Prioritas Task:

red_led task memiliki prioritas lebih tinggi daripada green_led task sehingga dieksekusi lebih sering.

Polanya Berbeda:

green_led task menjalankan pola 80 kali kedipan dengan jeda 6 detik.
red_led task menjalankan pola 10 kali kedipan dengan jeda 1,5 detik.

Meskipun task-task berjalan sendiri, mereka tidak saling mengganggu karena diatur oleh RTOS dengan jeda (osDelay).

Demo:



https://github.com/user-attachments/assets/235c1903-60f6-4c49-b664-c3640881bf38

