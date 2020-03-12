## REST API

REST, singkatan bahasa Inggris dari  _Representational State Transfer_, adalah suatu gaya arsitektur perangkat lunak untuk untuk pendistibusian sistem hipermedia, sedangkan CodeIgniter merupakan aplikasi sumber terbuka yang berupa framework PHP dengan model MVC (Model, View, Controller) untuk membangun website dinamis dengan menggunakan PHP. Repository ini adalah penerapan REST API pada Codeigniter 3.

## Requirements

 NAMA | DOWNLOAD
 ------ | ------ 
 XAMPP | https://www.apachefriends.org/download.html
Visual Studio Code (Text Editor) | https://code.visualstudio.com/download
CodeIgniter | https://codeigniter.com/download
 Postman | https://www.postman.com/downloads/

## Persiapan

1.  Mendownload repository ini dan simpan ke dalam folder htdocs anda. Jangan lupa memberi nama folder project ini, contoh : REST_CI
2.  Mengakses link _[http://localhost/REST_CI/](http://localhost/REST_CI/)_  menggunakan browser anda, maka akan muncul halaman Welcome to CodeIgniter.
3.  Membuka XAMPP, klik start pada Apache dan MySQL.
4.  Membuat database baru di PHPMyAdmin dengan cara mengimport file  `kontak.sql`  lalu beri nama database tersebut dengan nama  _**kontak**_
5.  Membuka Text Editor (saya menggunakan Visual Studio Code).
6.  Melakukan konfigurasi pada file  `application/config/database.php`  menggunakan Text Editor seperti di bawah ini :
```php
defined('BASEPATH') OR exit('No direct script access allowed');
$active_group = 'default';
$query_builder = TRUE;

$db['default'] = array(
    'dsn'   => '',
    'hostname' => 'localhost',
    'username' => 'root',
    'password' => '',
    'database' => 'kontak',
    'dbdriver' => 'mysqli',
    'dbprefix' => '',
    'pconnect' => FALSE,
    'db_debug' => (ENVIRONMENT !== 'production'),
    'cache_on' => FALSE,
    'cachedir' => '',
    'char_set' => 'utf8',
    'dbcollat' => 'utf8_general_ci',
    'swap_pre' => '',
    'encrypt' => FALSE,
    'compress' => FALSE,
    'stricton' => FALSE,
    'failover' => array(),
    'save_queries' => TRUE
);
```
4.  Membuat function untuk melakukan  _**Get, Post, Put,**_  dan  _**Delete**_  pada file  `application/controllers/Kontak.php` menggunakan Text Editor
5.  Membuka Postman lalu membuka Tab baru dengan cara mengklik  _**tombol +**_  
6.  Masukkan link berikut  [http://localhost/REST_CI/index.php/kontak](http://localhost/REST_CI/index.php/kontak)  dan silahkan mencoba untuk melakukan manipulasi data seperti  _**Get, Post, Put,**_  dan  _**Delete.**_
7.  Lihat perubahan data pada  tabel  _**telepon**_ di database _**kontak**_ dan pastikan data berubah sesuai dengan aksi yang anda lakukan pada Postman.
