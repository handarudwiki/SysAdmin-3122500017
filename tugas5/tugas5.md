**Tugas 5**

**“Instalasi dan Konfigurasi Web Server, Database Server, dan Mail Server”**

**Disusun Untuk Memenuhi Tugas Mata Kuliah**

` `Workshop Administrasi Jaringan

**Dosen Pengampu : Dr Ferry Astika Saputra ST, M.Sc**

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.001.png)

Disusun oleh :

Handaru Dwiki Yuntara 

3122500017

2 D3 IT A

***Program Studi Teknik Informatika***

***Department Teknik Informatika dan Komputer***

***Politeknik Elektronika Negeri Surabaya***

1. NTP SERVER 
1. Installasi paket sinkronisasi 

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.002.png)

1. Konfigurasi timezone, RTC, dan NTP client

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.003.png)

1. Menyunting file timesyncd.conf untuk mengarah ke NTP server terdekat untuk mendapatkan waktu delay terpendek. Biasanya setiap organisasi atau negara mempunyai NTP Server sendiri → sudo nano /etc/systemd/timesyncd.conf

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.004.png)


1. Restart dan cek status

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.005.png)

1. Lakukan pengecekan kesesuaian tanggal

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.006.png)








1. Menampilkan status sinkronisasi

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.007.png)


1. **Apache 2 dan PHP-FM**
1. Install apache 2

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.008.png)

1. Melakukan konfigurasi apache 2
- sudo nano /etc/apache2/conf-enabled/security.conf

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.009.png)

- sudo nano /etc/apache2/moa/ds-enabled/dir.conf

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.010.png)








- sudo nano /etc/apache2/apache2.conf

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.011.png)

- sudo nano /etc/apache2/sites-enabled/000-default.conf

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.012.png)

- reload apache

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.013.png)


1. Melakukan test ke web server

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.014.png)

1. Install PHP 8.2

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.015.png)

1. Cek versi php

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.016.png)

1. Test PHP

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.017.png)

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.018.png)


1. Install PHP-FM

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.019.png)


1. Konfigurasi file /etc/apache2/sites-available/default-ssl.conf dengan menambahkan yang dikotaki merah

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.020.png)

1. Akktifkan modul-modul proxy\_fcgi dan setenvif dalam server Apache.

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.021.png)

1. Mengaktifkan modul php8.2-fpm

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.022.png)

1. Restart Sevice php

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.023.png)

1. Test validasi

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.024.png)

1. Melakuka test ke browser membuka file php.ini

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.025.png)








1. Maria DB dan PHPMyAdmin
1. Install mariadb

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.026.png)

1. Konfigurasi  /etc/mysql/mariadb.conf/50-server.cnf

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.027.png)

   Pada line 95 --> Mengkonfirmasi default charset menggunakan utf8mb4.

1. Restart Mariadb

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.028.png)










1. ` `Inisial Konfigurasi dan testing database MariaDB Server - sudo mysql\_secure\_installation

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.029.png)

- Connect to mariadb

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.030.png)







- Menampilkan hak akses yang dimiliki oleh user roo

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.031.png)

- Menampilkan semua daftar user

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.032.png)

- Melihat semua databsase

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.033.png)


- Membuat databse test\_db

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.034.png)

- Membuat table test\_table

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.035.png)

- Memasukkan 1 row ke table

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.036.png)

- Menampilkan isi table test

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.037.png)

- Menghapus database test\_db

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.038.png)









1. Install phpMyAdmin

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.039.png)

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.040.png)
**


`	`**![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.041.png)**

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.042.png)









1. Melakukan konfigurasi phpMyAdmin di apache2

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.043.png)

1. Coba membuka phpMyAdmin di web browser

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.044.png)

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.045.png)

1. Menambahkan privillege ke user phpmyadmin - Login ke mariadb → sudo mariadb -u root -p - Lalu berikan hak akses penuh kepada user phpmyadmin → GRANT ALL PRIVILEGES ON \*.\* TO 'phpmyadmin'@'localhost' IDENTIFIED BY 'password' WITH GRANT OPTION; FLUSH PRIVILEGES;

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.046.png)

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.047.png)


1. **Email System**
1. Install postfis sasl2-bin

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.048.png)

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.049.png)

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.050.png)

   Pilih no configuration



1. Mencopy file /usr/share/postfix/main.cf.dist ke /etc/postfix/main.cf --> sudo cp /usr/share/postfix/main.cf.dist /etc/postfix/main.cf

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.051.png)

1. Konfigurasi file /etc/postfix/main.cf
- Uncomment line 82

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.052.png)













  - uncomment line 98 dan isi dengan email hostname kelompok4.local

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.053.png)

- Uncomment line 106 dan isi dengan hostname kelompok6

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.054.png)



- Uncomment line 127

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.055.png)

- Uncomment line 141

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.056.png)






- Uncomment line 189

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.057.png)

- Uncomment line 232

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.058.png)













- Uncomment line 277
- ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.059.png)

- Uncomment line 294 dan tambahkan local network

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.060.png)






- Uncomment line 416

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.061.png)

- Uncomment 427

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.062.png)

- uncomment line 

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.063.png)

- Comment line 558 dan tambahkan di line 589 konfigurasi smtpd\_banner

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.064.png)


- Tambahkan sendmail\_path di line 659

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.065.png)





- Tambahkan newaliases\_path di line 664

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.066.png)

- Tambahkan sedgid grup di line 675

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.067.png)

- Comment line 679

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.068.png)

- Comment line 683 dan 688

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.069.png)




- ` `Comment line 692 dan tambahkan inet\_protocol

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.070.png)

- Menambahkan config di line terakhir. Yaitu mematikan SMTP VRFY command, require HELO command to sender hosts, Mengatur limit an email size, dan mengatur SMTP-Auth settings

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.071.png)


1. Update database alias untuk system postfix

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.072.png)

1. Restart layanan postfix

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.073.png)





1. Menambahkan konfigurasi anti spam

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.074.png)

1. Restart lagi

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.075.png)














1. Install Dovecot IMAP4 (TCP 143) and POP 3 (TCP10)

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.076.png)

1. Konfigurasi file /etc/dovecot/dovecot.conf

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.077.png)





1. Konfigurasi file /etc/dovecot/conf.d/10-auth.conf

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.078.png)

1. Uncomment line 10 dan izinkan plain text auth tambahkan auth\_mechanism

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.079.png)

1. Konfigurasi file /etc/dovecot/conf.d/10-mail.conf

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.080.png)

 

1. Konfigurasi file /etc/dovecot/conf.d/10-master.conf

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.081.png)


1. ` `Restart dovecot

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.082.png)

















1. Check all service 

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.083.png)

Akan terlihat hasilnya dengan status Server (LISTEN) : MariaDB(MySQL), IMAP, POP3, DNS(domain - http), IMAPS, POP3S, SSH, Postfix (SMTP)

1. Cek terhadap layanan postfix

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.084.png)

1. Install thunderbird

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.085.png)

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.086.png)


1. Tambahkan user untuk saling email

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.087.png)

1. Email dari user handaru ke ari

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.088.png)

1. Email udah masuk di ari

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.089.png)








1. **Roundcube Webmail**
1. Membuat database yang nantinya digunakan untuk roundcube

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.090.png)

1. Install roundcube

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.091.png)




1. Masuk ke direktori roundcube

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.092.png)

1. Mengimpor file mysql ke dalam database roundcube dengan menggunakan akun pengguna (-u roundcube) dan database (-D roundcube) yang sesuai. --> sudo mysql -u roundcube -D roundcube -p < mysql dan masukkan password mariaDB user roundcube (password)

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.093.png)

1. Melakukan set database informasi  pada file /etc/roundcube/Debian-db.php

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.094.png)










1. Konfigurasi file /etc/roundcube/config.inc.php

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.095.png)


1. Konfigurasi file /etc/apache2/conf-enabled/roundcube.conf

   ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.096.png)


1. Test kirim email antar user 
- User handaru kirim email ke user ari

![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.097.png)

- User ari menerima email

  ![](Aspose.Words.5c4a0bae-de95-47ae-9dcf-9adf2955163b.098.png)


# PRAKTIKUM MENGUNAKAN WEBMAIL DALAM 1 JARINGAN

## SETUP AWAL

Pertama-tama sambungkan komputer dengan kabel ethernet lokal yang tersedia. Setelah tersambung dengan jaringan lokal pastikan IP sesuai dengan kelompok/meja gunakan command `ipconfig/all` pada kasus ini saya mendapatkan IP `192.168.4.1` karena saya merupakan kelompok 4

![awalsetup](awalsetup1.png)

Lalu ubah pada setting network pada virtual machine ke Bridged Adapter dan ganti adapter sesuai dengan hasil command `ipconfig/all` yaitu `Realtek PCIe GbE Family Controller`

![awalsetup](awalsetup2.png)



## SETUP DEBIAN 12

Jalankan VM anda lalu pergi ke `sudo nano /etc/bind/named.conf.options`
![setup](setup1.png)

Rubah konfigurasi forwarders dengan `10.10.10.1` dan `192.168.4.10` ganti IP listen on ke `192.168.4.10` terakhir ganti konfigurasi `allow-query` dan `allow-recursion `ke `any`. Konfigurasinya akan menjadi seperti berikut:

![setup](setup2.png)
![setup](setup3.png)

Rubah juga konfigurasi di `sudo nano /etc/resolv.conf` tambahkan `nameserver 192.168.4.10` seperti dibawah berikut:

![setup](setup4.png)

Setelah itu coba tes ping IP kelompok lain yaitu kelompok 2 dengan command `ping 192.168.2.10` jika konfigurasi network benar maka maka hasilnya akan seperti berikut:

![tes](test1.png)

Coba juga tes ping ke sebagai contoh `detik.com` dengan command `ping detik.com` jika konfigurasi network benar maka akan seperti dibawah ini:

![tes](test2.png)

Buka browser dan coba test apakah bisa mengakses webmail (roundcube) kelompok lain disini saya mencoba mengakses ke webmail kelompok 2 dengan alamat `mail.kelompok2.local` Jika berhasil maka akan tampil seperti berikut:

![tes](test3.png)

Buka browser dan coba test apakah bisa mengakses webmail (roundcube) dengan alamat `mail.kelompok4.local/roundcube` Jika berhasil maka akan tampil seperti berikut:

![tes](test4.png)

Jika network static tidak bekerja dan tidak bisa tampil seperti diatas maka coba buka `sudo nano /etc/network/interfaces` buat auto network dengan mengcomment konfigurasi static pada seperti dibawah ini:

![setup](setup5.png)

Lalu setup manual IPv4 dengan IP addres `192.168.4.10` netmask `255.255.255.0` gateway `192.168.4.1` dan DNS `10.10.10.1`

![setup](setup6.png)


## KONFIGURASI WINBOX

Buka winbox di windows lalu pergi ke menu bridge. Setelah itu remove bridge yang ada dan buat baru. langsung next next saja hingga bertemu setting DNS inputkan `10.10.10.1`

![winbox](winbox1.png)


## HASIL AKHIR

Login ke rouncube dengan user dan password yang sudah disetup. pada kasus ini saya bisa menerima pesan dari user `iqbal@kelompok6.local` seperti pada gambar dibawah ini:

![hasil](hasil1.png)
![hasil](hasil2.png)

Disini saya ingin mencoba mengirim pesan email ke `user@kelompok2.local` dan berhasil
![hasil](hasil3.png)















