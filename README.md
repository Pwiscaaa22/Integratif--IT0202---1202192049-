# Integratif--IT0202---1202192049-
# Final Project

## Catharina Prisca Titi Larasati | 1202192049 | IT0202

### Phase 1

* Buka website https://windows.php.net/download#php-8.1 untuk mendownload php, dan pilih file zip Thread Safe.

* Extract file php, lalu copy dan paste di lokasi "C:\Program Files". Kemudian cari file bernama "php.ini development", lalu buat salinan dan rename file salinan tersebut menjadi "php.ini". Buka text editor, lalu ubah setting menjadi seperti gambar dibawah ini, dan simpan.
  
* Tekan Windows dan klik Environment, kemudian buka The Edit System Environment Variables, dan pilih Environment Variables

* Pilih variable path untuk menambahkan alamat dari file php, kemudian pilih ok.

* Buka terminal dan ketikkan php -v. Jika tampilan yang muncul seperti pada gambar dibawah ini, maka tandanya php telah berhasil terinstall.


### INSTALL COMPOSER

* Buka website https://getcomposer.org/download/ untuk mendownload composer

* Install file composer yang sudah di download. Selanjutnya buka terminal dan ketik "composser", maka akan muncul tampilan seperti pada gambar dibawah ini. Ini menandakan bahwa composer sudah berhasil di install.


### INSTALL LARAVEL VIA COMPOSER

* Buka website https https://laravel.com/docs/9.x#installation-via-composser untuk menyalin command instalasi laravel via composer.

* Buat folder seperti biasa lalu buka terminal dan masuk ke dalam folder yang telah dibuat, lalu install laravelnya. 

* Buat project untuk install laravel dengan command 

  ```markdown
  composer create-project laravel/laravel nama_project
  ```
  
* Copy server laravel, untuk dibuka di browser








### Phase 2

* Buat database dengan menggunakan phpmyadmin
* Ubah dan sesuaikan DB_DATABASE dengan nama database yang telah dibuat
* Selanjutnya, buat 2 migration (migration untuk table Rss dan migration untuk table news), dengan script seperti dibawah ini : 
    ```markdown
  php artisan make:migration create_rss_table
  ```

 ```markdown
  php artisan make:migration create_News_table
  ```
  
* Tambahkan kolom name dan rul pada create_rss_table
* Tambahkan kolom title, img_url, description, source_url, dan rss_id pada create_news_table
* Agar migrasi yang telah dibuat tadi dapat berjalan sesuai dengan fungsinya, maka tambahkan perintah 

    ```markdown
  php artisan migrate
    ```
    
* Selanjutnya, buatlah koneksi dengan database, dengan menggunakan seeder dan controller untuk table Rss dan News, dengan script


    ```markdown
  php artisan make:model Rss --seed --controller
    ```


* Tambahkan script seperti dibawah ini pada file Rss.php
  ```markdown
  protected $table = 'rss';
    ```
    
* Ubah dan sesuaikanlah RssSeeder.php dan DatabaseSeeder.php
* Cek koneksi dengan perintah seperti php artisan db:seed, dan cek phpmyadmin
* Jalankan Perintah php artisan make:model News --controller
* Dan tambahkan script protected $table='news' pada News.php. Ubah dan sesuaikan NewsController.php, dan web.php.
* Berikutnya, cek localhost http://127.0.0.1:8000/aggregrate/1
* Buat logic untuk get rss
* Lakukan parsing xml to objecty
* lalu cek localhost http://127.0.0.1:8000/aggregrate/1
* Cek table news pada database
* Jika sudah benar, isi tampilan localhost http://127.0.0.1:8000/aggregrate/1 akan berubah menjadi berita yang sudah dicantumkan.
