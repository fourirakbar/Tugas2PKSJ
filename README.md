# Pendahuluan

**Anggota Kelompok**
1. Aviananda Dwirahma - 5114100085
2. Fourir Akbar - 5114100115
3. Afif Ridho Kamal Putra - 5114100173

# Dasar Teori 
**1. OS yang digunakan**
##### * Ubuntu Server
Ubuntu server adalah sebuah sistem operasi linux berbasis debian yang digunakan untuk membangun sebuah server.

##### * Kali Linux
Kali Linux adalah sebuah distro linux yang merupakan sebuah OS pembaharuan dari BackTRack dan dikembangkan oleh Offensive Security yang mempunyai fungsi untuk kebutuhan professional penetration tester. 

**2. Tools yang digunakan**
##### * Wordpress Plugin - Video Player
Adalah plugin Wordpress yang menyediakan fitur untuk memasukkan video ke website Wordpress.
##### * Wordpress Plugin - League Manager
adalah plugin Wordpress yang digunakan untuk menampilkan hasil dari pertandingan sepak bola pada website wordpress.
##### * Sql Map
adalah sebuah tools opensource yang mendeteksi dan melakukan exploit pada bug SQL injection secara otomatis, dengan melakukan serangan SQL injection, seorang attacker dapat mengambil alih serta memanipulasi sebuah database di dalam sebuah server.
##### * Wpscan
adalah tools vulnerability scanner untuk CMS Wordpress yang ditulis dengan menggunakan bahasa pemrograman ruby. Wpscan mampu mendeteksi kerentanan umum serta daftar semua plugin dan themes yang digunakan oleh sebuah website yang menggunakan CMS Wordpress.

# Uji Penetrasi 2
### Tugas:
* Instal Wordpress pada sebuah virtual OS
* Install plugin yang vulnerable terhadap SQL injection
* Instal / gunakan tools untuk uji SQL injection pada Wordpress

* ## Langkah Instalasi Wordpress pada Sebuah Virtual OS
    Kelompok kami menginstall wordpress pada ubuntu server yang telah digunakan pada Uji Penetrasi 1 sebelumnya.
    
    * Pastilkan LAMP Server sudah terinstal pada OS Anda. Kelompok kami menginstall LAMP Server saat pertama kali menginstal OS.

    ![1](/img/1.png)
    <br>
    * Masuk ke dalam ubuntu server, download wordpress dari web resmi wordpress.

    ![2](/img/2.png)
    <br>
    * Setelah itu extract file wordpress tersebut ke /var/www/html

    ![3](/img/3.png)
    <br>
    * Setelah berhasil di extract, masuk ke mysql yang sudah Anda install

    ![4](/img/4.png)
    <br>
    * Lalu buat sebuah database untuk wordpress yang akan Anda install. Disini kelompok kami menggunakan database dengan nama "wordoress".

    ![5](/img/5.png)
    <br>
    * Lalu buat sebuah user yg berfungsi untuk mengakses database tersebut. Disini kelompok kami membuat sebuah user dengan nama wordpress.

    ![6](/img/6.png)
    <br>
    * Lalu coba Anda cek apakah user yang barusan Anda buat sudah tersedia apa belum.

    ![7](/img/7.png)
    <br>
    * Setelah itu berikan akses untuk user yang barusan Anda buat ke database wordpress. Setelah itu flush privileges.

    ![8](/img/8.png)
    <br>
    * Untuk memastikannya, coba login ke mysql dengan user yang barusan Anda buat, dan juga coba cek apakah ada database wordpress.

    ![9](/img/9.png)
    <br>
    * Masuk ke dalam direktori /var/www/html/wordpress, dan copykan file wp-config-sample.php menjadi wp-config.php.

    ![10](/img/10.png)
    <br>
    * Buka file wp-config.php, lalu edit bagian 'DB_NAME', 'DB_USER', dan 'DB_PASSWORD' sesuai yang Anda buat.

    ![11](/img/11.png)
    <br>
    * Setelah itu, silahkan Anda akses wordpress yang sudah Anda buat dari device lain. Caranya dengan mengakses [ip_wordpress]/wordpress

    ![12](/img/12.png)
    <br>
    * Lalu isikan informasi yang dibutuhkan.

    ![13](/img/13.png)
    <br>
    * Setelah ada pemberitahuan sukses, klik Log In

    ![14](/img/14.png)
    <br>
    * Lalu login dengan username dan password yang telah Anda buat.

    ![15](/img/15.png)
    <br>
    * Jika Anda berhasil login, maka akan muncul halaman admin seperti pada gambar dibawah. Instalasi wordpress telah selesai.

    ![16](/img/16.png)
    <br>

    * Setelah itu kita akan menginstall plugin Video Player. Pertama download dulu plugin tersebut dari web wordpress.

    ![17](/img/17.png)
    <br>
    * Setelah selesai di download, klik plugin > add new.

    ![18](/img/18.png)
    <br>
    * Setelah itu klik upload plugin > choose file > lalu pilih file plugin yang sudah Anda download.

    ![19](/img/19.png)
    <br>
    * Terkadang ada beberapa error seperti pada gambar dibawah.

    ![20](/img/20.png)
    <br>
    * Jika terjadi seperti pada gambar diatas, maka buka kembali ubuntu server Anda, lalu edit file php.ini.

    ![21](/img/21.png)
    <br>
    * Pada file php.ini, cari kata "upload_max_filesize" dan ubah menadi 30M.

    ![22](/img/22.png)
    <br>
    * Setelah itu restart apache2 Anda.

    ![23](/img/23.png)
    <br>
    * Filesize sudah di ubah, terkadang ada error lagi seperti pada gambar dibawah.
    
    ![24](/img/24.png)
    <br>

    * Jika terjadi seperti pada gambar diatas, maka buka kembali ubuntu server Anda, lalu ganti akses ke direktori wordpress di server Anda.

    ![25](/img/25.png)
    <br>
    * Coba kembali install plugin tersebut, jika sukses maka akan muncul seperti pada gambar dibawah.

    ![27](/img/27.png)
    <br>