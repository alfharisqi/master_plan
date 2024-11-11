**NAMA : ALFHA RISQI WICAKSONO**
**NIM : 362358302145**

# Praktikum 1: Dasar State dengan Model-View

**1. Jelaskan maksud dari langkah 4 pada praktikum tersebut! Mengapa dilakukan demikian?**
Pada , file `data_layer.dart` dibuat untuk menggabungkan ekspor model `plan.dart` dan `task.dart`. Tujuannya agar proses impor menjadi lebih mudah dan rapi, karena hanya perlu mengimpor satu file `data_layer.dart` untuk mengakses semua model yang dibutuhkan. Ini membuat kode lebih efisien, mudah dipelihara, dan lebih mudah dibaca.

**2. Mengapa perlu variabel plan di langkah 6 pada praktikum tersebut? Mengapa dibuat konstanta ?**
Variabel `plan` pada Langkah 6 diperlukan untuk menyimpan data rencana yang berisi daftar tugas dalam aplikasi. Variabel ini digunakan untuk memanipulasi dan memperbarui informasi rencana, seperti menambahkan tugas baru atau mengubah status tugas.

Dibuat sebagai konstanta karena pada saat pembuatan objek `Plan`, nilai-nilai default seperti nama dan daftar tugas ditetapkan melalui konstruktor. Menggunakan konstanta memastikan nilai awal objek tidak dapat diubah setelah objek dibuat, yang membantu menjaga integritas data dan menghindari perubahan yang tidak diinginkan.

**Capture Pratikum 1**

![Screenshot 2024-11-11 090109](https://github.com/user-attachments/assets/af367f28-f065-4bf1-810f-a5697f543119)

**3. Apa kegunaan method pada Langkah 11 dan 13 dalam lifecyle state ?**
Pada **Langkah 11** dan **Langkah 13**, dua metode penting dalam siklus hidup **StatefulWidget** digunakan, yaitu `initState()` dan `dispose()`.

- initState()` (Langkah 11): Metode ini dipanggil sekali saat `State` pertama kali dibuat. Di sini, kita menginisialisasi variabel seperti `scrollController` dan menambahkan listener untuk menangani peristiwa scroll. `initState()` memastikan bahwa pengaturan awal untuk scroll controller terjadi sebelum widget ditampilkan.

- dispose() (Langkah 13): Metode ini dipanggil ketika `State` widget tidak lagi digunakan, biasanya saat widget dihapus dari widget tree. Di sini, kita membersihkan `scrollController` dengan memanggil `dispose()` untuk mencegah kebocoran memori dan melepaskan sumber daya yang digunakan oleh controller.

Kedua metode ini mengelola siklus hidup objek dengan baik, memastikan pengaturan yang benar saat widget pertama kali muncul dan membersihkan sumber daya saat tidak diperlukan lagi.
