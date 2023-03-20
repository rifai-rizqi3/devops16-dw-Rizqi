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
    
### apt update, install nginx dan open port

![Screenshot from 2023-03-20 18-40-55](https://user-images.githubusercontent.com/84585203/226329230-0f295199-4119-4e56-8cb5-06ef91167d10.png)
![Screenshot from 2023-03-20 18-40-39](https://user-images.githubusercontent.com/84585203/226329241-51ad17ed-d288-4e13-b560-b2442af8f65a.png)
![Screenshot from 2023-03-20 18-39-30](https://user-images.githubusercontent.com/84585203/226329244-6d30c05b-c6d2-4bf8-9a2b-b21e3115835d.png)
![Screenshot from 2023-03-20 18-38-44](https://user-images.githubusercontent.com/84585203/226329248-042c46cc-0645-466d-beb5-4d7c8d4970b9.png)
![Screenshot from 2023-03-20 18-38-00](https://user-images.githubusercontent.com/84585203/226329253-bad620b4-79f6-4e84-909c-7fa69ffcb8ac.png)


## Aplikasi untuk monitoring

### htop

![Screenshot from 2023-03-20 18-28-30](https://user-images.githubusercontent.com/84585203/226327491-3f933260-4657-4b37-a25b-0dc0c2598075.png)


### nmon 

![Screenshot from 2023-03-20 18-29-19](https://user-images.githubusercontent.com/84585203/226327487-20c5d987-be99-4412-a09c-c202b2d50d34.png)
![Screenshot from 2023-03-20 18-30-48](https://user-images.githubusercontent.com/84585203/226327467-489f90b4-0f8b-47ab-a58c-05836abf6247.png)
![Screenshot from 2023-03-20 18-30-31](https://user-images.githubusercontent.com/84585203/226327476-f27a1307-55fc-4b4e-8169-6ce4ee46b78f.png)
![Screenshot from 2023-03-20 18-29-50](https://user-images.githubusercontent.com/84585203/226327478-fb455647-28d8-456d-8342-572f2a7462e9.png)
![Screenshot from 2023-03-20 18-29-40](https://user-images.githubusercontent.com/84585203/226327482-8c53f552-993c-43d5-9038-1880aa5e94fe.png)

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
