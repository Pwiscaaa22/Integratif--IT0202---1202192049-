# Final Project

## Catharina Prisca Titi Larasati | 1202192049 | IT0202

### Phase 1

* Buka website https://windows.php.net/download#php-8.1 untuk mendownload php, dan pilih file zip Thread Safe.

  ![](pict/1.png)



* Extract file php, lalu copy dan paste di lokasi "C:\Program Files". Kemudian cari file bernama "php.ini development", lalu buat salinan dan rename file salinan tersebut menjadi "php.ini". Buka text editor, lalu ubah setting menjadi seperti gambar dibawah ini, dan simpan.

  ![](pict/2.png)

​		![](pict/3.png)



* Tekan Windows dan klik Environment, kemudian buka The Edit System Environment Variables, dan pilih Environment Variables

  ![](pict/4.png)

  

* Pilih variable path untuk menambahkan alamat dari file php, kemudian pilih ok.

  ![](pict/5.png)



* Buka terminal dan ketikkan php -v. Jika tampilan yang muncul seperti pada gambar dibawah ini, maka tandanya php telah berhasil terinstall.

  ![](pict/6.png)



### INSTALL COMPOSER

* Buka website https://getcomposer.org/download/ untuk mendownload composer

  ![](pict/7.png)



* Install file composer yang sudah di download. Selanjutnya buka terminal dan ketik "composser", maka akan muncul tampilan seperti pada gambar dibawah ini. Ini menandakan bahwa composer sudah berhasil di install.

  ![](pict/8.png)



### INSTALL LARAVEL VIA COMPOSER

* Buka website https https://laravel.com/docs/9.x#installation-via-composser untuk menyalin command instalasi laravel via composer.

* Buat folder seperti biasa lalu buka terminal dan masuk ke dalam folder yang telah dibuat, lalu install laravelnya. 

* Buat project untuk install laravel dengan command 


  ```markdown
  composer create-project laravel/laravel nama_project
  ```

  ![](pict/9.png)

![](pict/10.png)



* Copy server laravel, untuk dibuka di browser

  ![](pict/11.png)



### Phase 2

* Buat database di phpmyadmin

* Ubah dan sesuaikan DB_DATABASE dengan nama database yang telah dibuat

  ![](pict/2.1.png)

* Selanjutnya, buat 2 migration (migration untuk table Rss dan migration untuk table news), dengan script seperti dibawah ini : 


    ```markdown
  php artisan make:migration create_rss_table
    ```


    ```markdown
  php artisan make:migration create_news_table
    ```

  ![](pict/2.2.png)

* Pada create_rss_table, tambahkan kolom name dan url. Sehingga tampilan Visual Studio Code akan berubah seperti gambar dibawah ini :

  ![](pict/2.3.png)

* Pada create_news_table, tambahkan kolom title, img_url,description, source_url, dan rss_id. Sehingga tampilan Visual Studio Code akan berubah menjadi seperti gambara dibawah ini :

  ![](pict/2.4.png)

* Agar migrasi yang telah dibuat tadi dapat berjalan sesuai dengan fungsinya, maka tambahkan perintah 


    ```markdown
  php artisan migrate
    ```

  ![](pict/2.5.png)

​		![](pict/2.6.png)



* Selanjutnya, butalah koneksi dengan database, dengan menggunakan seeder dan controller untuk table Rss dan News, dengan script


    ```markdown
  php artisan make:model Rss --seed --controller
    ```


* Tambahkan script seperti dibawah ini pada file Rss.php


  ```markdown
  protected $table = 'rss';
  ```

  ![](pict/2.9.png)



* Ubah dan sesuaikan RssSeeder.php dan DatabaseSeeder.php seperti dibawah ini :

  ![](pict/2.7.png)

  ![](pict/2.8.png)



* Cek koneksi dengan perintah seperti dibawah ini, dan cek phpmyadmin


  ```markdown
  php artisan db:seed
  ```

  ![](pict/2.10.png)



* Jalankan Perintah 


  ```markdown
  php artisan make:model News --controller
  ```

  dan tambahkan script seperti dibawah pada News.php. Ubah dan sesuaikan NewsController.php, dan web.php sehingga menjadi seperti dibawah ini 


  ```markdown
  protected $table='news'
  ```

  ![](pict/2.11.png)	![](pict/2.12.png)

  ​	![](pict/2.13.png)



* Berikutnya, cek localhost http://127.0.0.1:8000/aggregrate/1

  ​	![](pict/2.14.png)



* Buatlah logic untuk get rss dengan menggunakan script seperti yang tertera pada gambar

  ​	![](pict/2.15.png)

​	

Maka hasilnya akan menjadi seperti dibawah ini :	

![](pict/2.16.png)



* Lakukan parsing xml to objecty dengan menggunakan script seperti dibawah ini :

  ​	![](pict/2.17.png)

​	lalu cek localhost http://127.0.0.1:8000/aggregrate/1 dan hasilnya akan menjadi seperti ini :		![](pict/2.18.png)



* Cek table news pada database

  ​	![](pict/2.19.png)

  

  Lalu akan mendapatkan hasil seperti dibawah ini:

  ​	![](pict/2.20.png)

  

* Jika sudah berhasil, maka tambahkan Rss dengan cara menambahkan name dan url pada RssSeeder, lalu jalankan, maka akan mendapatkan hasil seperti ini :

  ​	![](pict/2.21.png)

​			![](pict/2.22.png)