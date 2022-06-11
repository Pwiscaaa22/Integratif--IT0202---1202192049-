# Final Project

## Catharina Prisca Titi Larasati | 1202192049 | IT0202

### First Step

* Buka website https://windows.php.net/download#php-8.1 untuk mendownload php, dan pilih file zip Thread Safe.

  ![](pict step 1/1.png)



* Extract file php, lalu copy dan paste di lokasi "C:\Program Files". Kemudian cari file bernama "php.ini development", lalu buat salinan dan rename file salinan tersebut menjadi "php.ini". Buka text editor, lalu ubah setting menjadi seperti gambar dibawah ini, dan simpan.

  ![](pict step 1/2.png)

​		![](pict step 1/3.png)



* Tekan Windows dan klik Environment, kemudian buka The Edit System Environment Variables, dan pilih Environment Variables

  ![](pict step 1/4.png)

  

* Pilih variable path untuk menambahkan alamat dari file php, kemudian pilih ok.

  ![](pict step 1/5.png)



* Buka terminal dan ketikkan php -v. Jika tampilan yang muncul seperti pada gambar dibawah ini, maka tandanya php telah berhasil terinstall.

  ![](pict step 1/6.png)



### INSTALL COMPOSER

* Buka website https://getcomposer.org/download/ untuk mendownload composer

  ![](pict step 1/7.png)



* Install file composer yang sudah di download. Selanjutnya buka terminal dan ketik "composser", maka akan muncul tampilan seperti pada gambar dibawah ini. Ini menandakan bahwa composer sudah berhasil di install.

  ![](pict step 1/8.png)



### INSTALL LARAVEL VIA COMPOSER

* Buka website https https://laravel.com/docs/9.x#installation-via-composser untuk menyalin command instalasi laravel via composer.

* Buat folder seperti biasa lalu buka terminal dan masuk ke dalam folder yang telah dibuat, lalu install laravelnya. 

* Buat project untuk install laravel dengan command 


  ```markdown
  composer create-project laravel/laravel nama_project
  ```

  ![](pict step 1/9.png)

![](pict step 1/10.png)



* Copy server laravel, untuk dibuka di browser

  ![](pict step 1/11.png)