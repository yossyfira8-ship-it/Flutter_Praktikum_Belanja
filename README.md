Konsep Navigasi dan Rute pada Layout Belanja

Praktikum 5: Penerapan Navigasi di Flutter
Langkah 1 – Membuat Project Baru
Pertama-tama buatlah project Flutter baru yang akan digunakan sebagai dasar aplikasi belanja. Project ini akan menjadi wadah untuk menambahkan halaman dan fitur navigasi.
![1](https://github.com/user-attachments/assets/5cee8fd0-14e2-4355-8833-9db40216fc63)

Langkah 2 – Mendefinisikan Router
Gunakan routes pada MaterialApp agar aplikasi dapat berpindah antar halaman. Dengan pendekatan ini, setiap halaman memiliki nama rute yang bisa dipanggil menggunakan Navigator.
![2](https://github.com/user-attachments/assets/f2c0a5fc-f93e-4301-9134-d8fe6b97ab48)

Langkah 3 – Melengkapi main.dart
Di file main.dart, daftarkan rute yang akan digunakan, misalnya halaman Home sebagai beranda dan halaman Item untuk detail produk.
Selain itu, buat folder models untuk menyimpan struktur data seperti Item.
![3](https://github.com/user-attachments/assets/2823ebec-8da3-43a8-a534-fa6184885d2c)

Langkah 4 – Membuat Halaman HomePage

Pada HomePage, tampilkan daftar produk menggunakan ListView dengan itemBuilder. Setiap produk bisa diklik untuk membuka halaman detail. Tampilan akhir akan menampilkan list produk seperti di toko online sederhana.
![4](https://github.com/user-attachments/assets/f8e34ab4-85b2-48f0-87d2-ec05f90dab56)

Tugas Praktikum 2
1. Mengirim Data Antar Halaman
Gunakan Navigator.pushNamed untuk mengirim data produk yang dipilih ke halaman detail:
Navigator.pushNamed(context, '/item', arguments: item);
Dengan begitu, informasi produk dapat dibawa ke halaman berikutnya.
<img width="1660" height="1750" alt="carbon (14)" src="https://github.com/user-attachments/assets/d8b807b3-df5a-4e1c-a3c1-d4737a46a077" />

2. Mengambil Data di ItemPage
Di halaman ItemPage, data yang dikirim bisa diambil dengan:
final itemArgs = ModalRoute.of(context)!.settings.arguments as Item;
Hal ini memungkinkan detail produk (nama, harga, dll.) ditampilkan.
![5](https://github.com/user-attachments/assets/7f5012e6-e295-4312-8ef5-f06be0215447)

3. Menambahkan Atribut Tambahan & GridView
Selain nama dan harga, tambahkan atribut lain seperti foto produk, stok, dan rating.
Untuk mempercantik tampilan, ganti ListView menjadi GridView sehingga produk ditampilkan dalam 2 kolom, mirip aplikasi marketplace.
![6](https://github.com/user-attachments/assets/6bb79eef-37e8-49d0-860a-a428314ec168)

4. Mengimplementasikan Hero Widget
Tambahkan animasi transisi dengan Hero widget, agar gambar produk tampak lebih interaktif saat berpindah dari daftar ke detail produk.
![7](https://github.com/user-attachments/assets/f5e5a4bc-00f7-48b7-9ef2-84bf2d295099)

Hasil
![8](https://github.com/user-attachments/assets/bdb311cf-ace6-4023-a817-071997aeab35)

5. Identitas Mahasiswa
Sebagai bagian dari tugas, sertakan Nama dan NIM pada halaman aplikasi untuk menandai hasil kerja pribadi.
![9](https://github.com/user-attachments/assets/ee5ec013-9366-4e80-94ca-5e6104459296)
