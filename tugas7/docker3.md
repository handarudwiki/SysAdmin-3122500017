**Tugas 7**

**Docker 101 Tutorial**

Disusun Untuk Memenuhi Mata Kuliah

Workshop Administrasi Jaringan

**Dosen Pengampu : Dr Ferry Astika Saputra ST, M.Sc**

![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.001.png)

Disusun Oleh :

Handaru Dwiki Yuntara

3122500017

2 D3 IT A

***Program Study Teknik Informatika***

***Department Teknik Informatika dan Komputer***

***Politeknik Elektronika Negeri Surabaya***

1. Getting Started

   ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.002.png)

   Menjalankan container yang terdapat di docker registry dan memforward di port 80

   Maka akan muncul

   ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.003.png)

   Dan Ketika diklik tampil

   ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.004.png)

   Dan Ketika dilhat container yang aktif ada 1 

   ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.005.png)


1. Our Aplication
- Buat file dengan nama Dockerfile dan isi sesuai dengan yang dibawah ini

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.006.png)

- Masukan app.zip yang didapat dari website

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.007.png)

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.008.png)

- Lalu build docker image

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.009.png)

- Lalu buat container dan forward ke port 3000

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.010.png)

- Maka akan tampil halaman todolist

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.011.png)





1. Updating Our App
- Ubah line 57 di app.js

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.012.png)

- Build container ulang maka akan terjadi error karena port 3000 sudah terpakai. Kita bisa mematikan duu containernya dan mengahpusnya

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.013.png)

- Lalu build ulang containernya dan forward ke port 3000

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.014.png)

1. Sharring Our App
- Buat repository di docker hub

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.015.png)

- Lalu push 

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.016.png)

  Mengapa gagal? Perintah push sedang mencari gambar bernama dockersamples/101-todo-app, tetapi tidak menemukannya. Jika Anda menjalankan docker image ls, Anda juga tidak akan melihatnya.

  Untuk memperbaikinya, kita perlu "memberi tag" pada gambar kita, yang pada dasarnya berarti memberinya nama lain.

- Beri tag lalu push lagi

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.017.png)


- Maka akan berhasil dipush ke docker hub

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.018.png)

- Buat instance baru

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.019.png)







- Build container dan forward ke port 3000

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.020.png)

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.021.png)

  Maka akan tampil halaman yang sama yang kita dapat dari docker registry bukan dari local

1. Persisiting Our DB
- Start container ubuntu yang akan membuat file Bernama /data.txt dengan nomor acak antara  1 dan 10000
- ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.022.png)

  Ketika dieksekusi filenya maka aka nada angka random

- Run ubuntu ulang dan tidak ada /data.txt

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.023.png)

- Create volume

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.024.png)

- **-v todo-db:/etc/todos**: Menggunakan volume Docker. Ini memetakan volume yang bernama todo-db di host ke direktori /etc/todos di dalam container. Volume ini digunakan untuk menyimpan data persisten yang digunakan oleh aplikasi di dalam container, sehingga data tetap ada meskipun container dihentikan atau dihapus.

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.025.png)

- Buka halaman web dan isi beberapa data

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.026.png)

- Hapus container yang telah dibuild

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.027.png)

- Jalankan ulang maka hasilnya sama karena diambil dari volume

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.028.png)






- Inspect volumne 

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.029.png)

  Penjelasan :

- CreatedAt: Menunjukkan waktu kapan volume ini dibuat, yaitu pada 2019-09-26T02:18:36Z.
- Driver: Menunjukkan driver yang digunakan untuk volume ini. Dalam hal ini, local, yang berarti volume disimpan di sistem file host.
- Labels: Menunjukkan label yang diterapkan pada volume. Dalam hal ini, tidak ada label ({}).
- Mountpoint: Menunjukkan lokasi di host di mana data volume disimpan, yaitu /var/lib/docker/volumes/todo-db/\_data. Ini adalah direktori fisik di host yang digunakan Docker untuk menyimpan data volume todo-db.
- Name: Menunjukkan nama volume, yaitu todo-db.
- Options: Menunjukkan opsi yang diterapkan pada volume. Dalam hal ini, tidak ada opsi ({}).
- Scope: Menunjukkan scope dari volume, yaitu local, yang berarti volume hanya dapat diakses oleh container di host yang sama.

1. Using Bind Mounts
- Run seperti ini

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.030.png)

  -dp 3000:3000:

  -d: Menjalankan container dalam mode terpisah (background).

  -p 3000:3000: Membuat pemetaan port, memetakan port 3000 di host ke port 3000 di dalam container. Ini berarti aplikasi di dalam container dapat diakses melalui http://localhost:3000.

  -w /app: Menetapkan direktori kerja (working directory) di dalam container ke /app. Ini berarti semua perintah akan dijalankan dari direktori ini.

  node:10-alpine: Image yang digunakan. Ini adalah image dasar untuk aplikasi kita dari Dockerfile, yang berbasis Node.js versi 10 dengan versi Alpine Linux yang ringan.

  sh -c "yarn install && yarn run dev":

  sh -c: Menjalankan shell menggunakan sh (karena Alpine Linux tidak memiliki bash).

  "yarn install && yarn run dev": Perintah yang dijalankan di dalam shell. Ini akan:

  yarn install: Menginstal semua dependensi yang terdaftar dalam package.json.

  yarn run dev: Menjalankan skrip dev yang didefinisikan dalam package.json. Jika melihat ke dalam package.json, skrip dev biasanya digunakan untuk memulai nodemon, yang akan secara otomatis me-restart server ketika ada perubahan pada file sumber.

- Cek container log

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.031.png)


- Ubah kodenya maka lognya akan otomatis ke refresh karena menggunakan nodemoon

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.032.png)

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.033.png)

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.034.png)

  Dan halamannya akan otomatis berubah

1. Multi Container Apps
- Buat network dengan nama todo-app

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.035.png)



- Jalankan container mysql 

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.036.png)

- Ekseskusi container dan coba tampilkan database yang ada

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.037.png)


- Pastikan untuk menghubungkannya ke jaringana/netshoot. Pastikan untuk menghubungkannya ke jaringan yang sama.

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.038.png)

- Masukkan data

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.039.png)

- Tampilkan semua dari todo\_items

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.040.png)






1. Using Docker Compose
- Lihat versi docker compose

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.041.png)

- Siapkan docker-compose.yaml

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.042.png)


- Docker compose up

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.043.png)

- Cek docker logs

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.044.png)

- Docker compose down 

  ![](asset/Aspose.Words.57fdc538-b20a-4214-b252-386319cc2466.045.png)







