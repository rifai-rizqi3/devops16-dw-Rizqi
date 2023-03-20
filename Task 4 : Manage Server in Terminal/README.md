# Day 6

# Manage Server With Terminal

## Definisi Terminal

Terminal merupakan tampilan berbasis teks yang digunakan untuk
mengoperasikan sistem operasi

## Keuntungan menggunakan Terminal

-   Lebih ringan dalam penggunaan resource perangkat

-   Lebih mudah dalam melakukan automasi

-   Pengoperasian bisa lebih cepat

## Command untuk text manipulation

### cat

Digunakan untuk menampilkan isi file ke terminal


### sed

Digunakan untuk mereplace suatu text dalam file


### grep

Digunakan untuk mencari suatu text dalam file


### sort

Digunakan untuk mengurutkan text


### echo

Digunakan untuk menampilkan text pada terminal


### wc

Untuk menghitung ada berapa baris, kalimat, dan kata dalam file


### Bash Terminal Operator

Dalam penggunaan, ada operator yang dapat digunakan untuk menggabung
beberapa command menjadi satu. Beberapa operatornya antara lain adalah

-   `;` (sequence) untuk menjalankan beberapa command berurutan dan
    bergantian\
    ![](./images/media/image7.png) 

-   `&` (Parallel) untuk menjalankan beberapa command sekaligus\
    ![](./images/media/image8.png) 

-   `&&` (And) hanya akan menjalankan command kedua jika command pertama
    berhasil\
    ![](./images/media/image9.png) 

-   `||` (Or) hanya akan menjalankan command kedua jika command pertama
    gagal\
    ![](./images/media/image10.png) 

-   `|` (Pipe) akan mengirimkan ouput command pertama ke command kedua\
    ![](./images/media/image11.png) 

-   `|&` (Pipe error) akan mengirimkan output error dari command pertama
    ke command kedua\
    ![](./images/media/image12.png) 

-   `<` (Redirecting input) untuk memasukkan input dari file ke command\
    ![](./images/media/image13.png) 

-   `<<` (Redirecting input -- here documents) digunakan unuk memasukkan
    beberapa line input dari terminal ke suatu command\
    ![](./images/media/image14.png) 

-   `<<<` (Redirecting input -- here string) digunakan untuk memasukkan
    satu baris string input ke suatu command\
    ![](./images/media/image15.png)

-   `>` (Redirect Output Truncate) untuk memasukkan output dari suatu
    command ke file. Jika file sudah ada, maka isinya akan dihapus lalu
    output command akan dimasukkan\
    ![](./images/media/image16.png) 

-   `>>` (Redirect Output Append) untuk memasukkan output dari suatu
    command ke file. Jika file sudah ada, maka isinya tidak akan dihapus
    lalu output command akan dimasukkan ke line terakhir file\
    ![](./images/media/image17.png) 

## Aplikasi untuk monitoring

### htop

![](./images/media/image18.png) 

### nmon 

![](./images/media/image19.png) \
![](./images/media/image20.png) 

### ps 

Digunakan untuk melihat proses yang sedang berjalan

![](./images/media/image21.png) 

### lsof

lsof (list of open files) digunakan untuk melihat file yang saat ini
digunakan proses

![](./images/media/image22.png) 

![](./images/media/image23.png)

## Membuat script bash untuk update dan upgrade

### Step 1

Buat file kosong baru dan isikan berikut
```
#!/bin/bash

sudo apt-get -y update

sudo apt-get -y upgrade
```
![](./images/media/image24.png) 

### Step 2

Tambahkan permission execute di file dengan command `chmod`

```chmod +x <file-name>```

![](./images/media/image25.png) 

### Step 3

Jalankan script dengan command berikut

```./<filename>```

atau

```bash <filename>```

![](./images/media/image26.png) 

## Membuat script bash untuk mencari file sysctl.conf

### Step 1

Buat file kosong dan isikan berikut
```
#!/bin/bash

sudo find / -name sysctl.conf -type f
```
![](./images/media/image27.png) 

### Step 2

Tambahkan permission execute di file dengan command `chmod`

```chmod +x <file-name>```

![](./images/media/image28.png) 

### Step 3

Jalankan script dengan command berikut

```./<filename>```

atau

```bash <filename>```

![](./images/media/image29.png) 
## Membuat script bash untuk membuka firewall port 22, 80, dan 443

### Step 1

Buat file kosong dan isikan berikut
```
#!/bin/bash

sudo ufw allow ssh

sudo ufw allow http

sudo ufw allow https

yes | sudo ufw enable
```
![](./images/media/image30.png) 

### Step 2

Tambahkan permission execute di file dengan command `chmod`

```chmod +x <file-name>```

![](./images/media/image31.png) 

### Step 3

Jalankan script dengan command berikut

```./<filename>```

atau

```bash <filename>```

![](./images/media/image32.png) 
