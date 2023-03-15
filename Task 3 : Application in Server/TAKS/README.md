# 1. Node Js

## 1. Install NodeJS di server kalian dan gunakan versi 10.24.1

# 2. Golang

Download dan Install engine Go dengan command berikut :

```wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su```

Selanjutnya tambahkan line berikut di akhir file ```~/.bashrc```

```
export PATH=$PATH:/usr/local/go/bin
```

![Screenshot from 2023-03-15 19-35-09](https://user-images.githubusercontent.com/84585203/225312418-ae0ec815-9ef7-4d0a-b510-9473942e1e8b.png)

Cek instalasi engine Go dengan command berikut ```exec bash``` lalu ```go version```



Buat file ```index.go``` lalu isikan script berikut

```
package main

import "fmt"

func main() {
    fmt.Println("Hello World!")
}
```

![Screenshot from 2023-03-15 19-36-05](https://user-images.githubusercontent.com/84585203/225312431-28677322-7284-4d60-8748-cde587fdd7ba.png)

Jalankan aplikasi dengan command berikut :

```
go run index.go
```

Jalankan command berikut untuk build aplikasi ```go build index.go```


![Screenshot from 2023-03-15 19-39-44](https://user-images.githubusercontent.com/84585203/225312438-52fae9a7-c919-47e2-bbe7-7357d41f6fae.png)

Setelah selesai build, jalan berikut untuk menjalankan aplikasi ```./index```


![Screenshot from 2023-03-15 19-40-13](https://user-images.githubusercontent.com/84585203/225312442-199bdcc2-84ee-4986-a2ea-306647c9e331.png)
![Screenshot from 2023-03-15 19-40-41](https://user-images.githubusercontent.com/84585203/225312443-e23403d5-161b-4cb0-9250-2e7da6d43ffc.png)
![Screenshot from 2023-03-15 19-41-21](https://user-images.githubusercontent.com/84585203/225312447-cc6528ee-0375-46b9-8746-419e844c3161.png)


