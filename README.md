# FileCrypt-Hybrid-Cryptography
# Latar Belakang
Dengan memanfaatkan teknologi hybrid cryptography, yang menggabungkan kriptografi simetris menggunakan algoritma AES dan kriptografi asimetris menggunakan algoritma RSA, sistem ini bertujuan untuk mengamankan dan mengoptimalkan file dari risiko peretasan yang dapat mengakses atau memodifikasi data dalam file tanpa izin.

# Infrastruktur yang Digunakan
**1.Front-end**, Dalam membangun tampilan antarmuka, infrastruktur utama yang digunakan adalah HTML (Hypertext Markup Language) untuk menyusun struktur konten dan tampilan tersebut diperindah dengan menggunakan CSS (Cascading Style Sheets), sehingga menghasilkan desain yang lebih menarik dan user-friendly

**2. Back-end**, Untuk mengimplementasikan fungsi hybrid kriptografi, digunakan bahasa pemrograman PHP karena fleksibilitas dan mampu dalam menangani logika bisnis serta pengolahan data secara aman

**3. Framework**, Framework CodeIgniter 3 (CI3) memberikan struktur yang ringan namun powerful, mempermudah pengelolaan kode dan mempercepat proses pengembangan berbasis PHP 

# Alur Sistem FileCrypt
1. Mulailah petualangan Anda bersama FileCrypt dengan menjelajahi lima fitur unggulan: Enkripsi AES, Brute Force Dekripsi AES, Enkripsi RSA, Dekripsi, dan Log Hari ini. Untuk memulai, kami merekomendasikan Anda mencoba fitur Enkripsi AES terlebih dahulu.
2. Langkah pertama, pilih file plaintext Anda dalam format apapun. FileCrypt akan secara otomatis memeriksa ukuran file tersebut, memastikan tidak melebihi batas maksimal 100 MB. Jika file terlalu besar, Anda akan mendapatkan notifikasi, “Ukuran File Anda Terlalu Besar.” Namun, jika file memenuhi kriteria, proses enkripsi AES akan segera dimulai. Dalam hitungan detik, Anda akan menerima file hasil enkripsi AES, file kunci enkripsi AES, beserta file kunci IV enkripsi yang siap diunduh.
3. Selanjutnya, untuk menguji tingkat keamanan file, Anda dapat melakukan pengujian brute force dengan mengklik fitur “Brute Force Dekripsi AES” terlebih dahulu. Anda cukup memasukan file yang telah terenkripsi AES beserta file kunci IV. Tunggu beberapa saat, jika hasil file kunci IV ditemukan maka Anda harus mengulangi proses enkripsi AES akibat file berhasil dibuka paksa oleh pengujian brute force. Namun jika file kunci IV tidak ditemukan maka Anda dapat melanjutkan proses Enkripsi RSA dengan hanya mengklik tombol “Kembali ke Menu Utama” dan pilih menu Enkripsi RSA. Di sini, Anda dapat mengunggah file kunci yang telah terenkripsi AES sebelumnya. Jika Anda belum melakukan enkripsi AES, sistem akan memberikan notifikasi, “File Anda belum Terenkripsi AES, Harap untuk Enkripsikan Terlebih Dahulu.” Setelah proses selesai, Anda dapat mengunduh file kunci enkripsi RSA sebagai tanda bahwa file Anda telah terenkripsi RSA.
4. Apabila Anda ingin mengembalikan file yang telah melalui proses hybrid kriptografi, Anda dapat memilih menu Dekripsi dengan mengklik tombol “Kembali ke Menu Utama.” Proses dekripsi dimulai dengan mengunggah file kunci enkripsi RSA untuk mendapatkan file kunci dekripsi RSA. Kemudian, klik tombol “Kembali ke Menu Dekripsi” untuk mengunggah file terenkripsi AES beserta file kunci dekripsi RSA. Tunggu beberapa saat, dan FileCrypt akan mengembalikan file Anda ke bentuk aslinya (plaintext). Anda telah berhasil melewati proses perlindungan keamanan file dengan hybrid kriptografi dan Anda dapat melihat Log waktu proses hybrid kriptografi dengan mengklik fitur “Log Hari Ini”.

# File Konfigurasi & Pengaturan Sistem
enkripsi_projek/application/config/*.php
Berisi berbagai file konfigurasi untuk framework yang digunakan (kemungkinan CodeIgniter). Termasuk:
- config.php → Pengaturan umum aplikasi.
- database.php → Konfigurasi koneksi database.
- routes.php → Definisi rute aplikasi.
- autoload.php → Pengaturan autoload library dan helper.

# File Kunci Enkripsi
- enkripsi_projek/application/keys/private_key.pem
  → Kunci privat untuk enkripsi dan dekripsi menggunakan metode asimetris (misalnya RSA).
  
- enkripsi_projek/application/keys/public_key.pem
  → Kunci publik yang digunakan untuk proses enkripsi.

# Controller dan Logika Aplikasi
- enkripsi_projek/application/controllers/enkripsicontroller.php
  → Berisi logika utama dalam mengelola proses enkripsi dan dekripsi.
  
- enkripsi_projek/application/logs/log-2025-01-22.php
  → Berisi catatan log untuk pemantauan error atau aktivitas sistem.

# File Tampilan (Views)
- enkripsi_projek/application/views/brute_force_form.php
  → Formulir untuk melakukan uji brute force terhadap enkripsi.
  
- enkripsi_projek/application/views/decrypt_form.php
  → Formulir untuk melakukan dekripsi teks atau file.
  
- enkripsi_projek/application/views/encrypt_aes_form.php
  → Formulir untuk melakukan enkripsi menggunakan metode AES.
  
- enkripsi_projek/application/views/encrypt_rsa_form.php
  → Formulir untuk melakukan enkripsi menggunakan metode RSA.
  
- enkripsi_projek/application/views/encryption_menu.php
  → Menu utama untuk memilih jenis enkripsi yang ingin dilakukan.

# Sistem Framework
- enkripsi_projek/system/core/*.php
  → Berisi inti dari framework yang digunakan dalam proyek ini.

- enkripsi_projek/system/database/*.php
  → Kumpulan file yang menangani koneksi dan query database.

# Dokumentasi dan Metadata
- enkripsi_projek/license.txt
  → Informasi lisensi proyek.

- enkripsi_projek/readme.rst
  → Dokumentasi proyek, biasanya berisi cara instalasi dan penggunaan.
