# 1. Node Js

Cek Versi NodeJs dengan cara ```node -v```

![Screenshot from 2023-03-15 20-41-57](https://user-images.githubusercontent.com/84585203/225331243-b27e2dbb-780e-4831-ad58-f96327866b12.png)

Clone repo 

```git clone https://github.com/dumbwaysdev/dumbflix-frontend```

![Screenshot from 2023-03-15 20-39-46](https://user-images.githubusercontent.com/84585203/225331226-bdbaef8d-0563-4847-900e-9d02ff250279.png)

Masuk ke directory ```dumbflix-frontend``` lalu instal npm dengan cara ```npm install```

![Screenshot from 2023-03-15 20-42-55](https://user-images.githubusercontent.com/84585203/225331251-c9400a91-3e66-47e3-bbf5-1bf6f12caf61.png)

Lalu configurasi ```api.js```

![Screenshot from 2023-03-15 20-47-07](https://user-images.githubusercontent.com/84585203/225331258-225e81d1-f41b-4470-98dc-cefa94473216.png)


# 2. Golang

Download dan Install engine Go dengan command berikut :

```wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su```

Selanjutnya tambahkan line berikut di akhir file ```~/.bashrc```

```
export PATH=$PATH:/usr/local/go/bin
```

![Screenshot from 2023-03-15 19-35-09](https://user-images.githubusercontent.com/84585203/225312418-ae0ec815-9ef7-4d0a-b510-9473942e1e8b.png)

Cek instalasi engine Go dengan command berikut ```exec bash``` lalu ```go version```

![Screenshot from 2023-03-15 19-36-05](https://user-images.githubusercontent.com/84585203/225312431-28677322-7284-4d60-8748-cde587fdd7ba.png)

Buat file ```index.go``` lalu isikan script berikut

```
package main

import "fmt"

func main() {
    fmt.Println("Hello World!")
}
```
![Screenshot from 2023-03-15 19-39-44](https://user-images.githubusercontent.com/84585203/225312438-52fae9a7-c919-47e2-bbe7-7357d41f6fae.png)

![Screenshot from 2023-03-15 19-40-13](https://user-images.githubusercontent.com/84585203/225312442-199bdcc2-84ee-4986-a2ea-306647c9e331.png)


Jalankan aplikasi dengan command berikut :

```
go run index.go
```

Jalankan command berikut untuk build aplikasi ```go build index.go```

![Screenshot from 2023-03-15 19-40-41](https://user-images.githubusercontent.com/84585203/225312443-e23403d5-161b-4cb0-9250-2e7da6d43ffc.png)

Setelah selesai build, jalan berikut untuk menjalankan aplikasi ```./index```

![Screenshot from 2023-03-15 19-41-21](https://user-images.githubusercontent.com/84585203/225312447-cc6528ee-0375-46b9-8746-419e844c3161.png)

# 3. Python

Secara default,python sudah terinstall secara default di instalasi ubuntu. Pastikan dengan menjalankan command berikut ```python3 -V```

![Screenshot from 2023-03-15 20-11-33](https://user-images.githubusercontent.com/84585203/225322230-9f3b7372-0b68-429d-bce3-877dda585137.png)

Jalankan command berikut jika belum terinstal ```sudo apt-get install python3```

Install package manager python yang bernama pip dengan command berikut ```sudo apt install python3-pip```

![Screenshot from 2023-03-15 20-12-20](https://user-images.githubusercontent.com/84585203/225322234-5cd93189-e760-447d-a286-f33ac74fcca2.png)

Kita akan membuat aplikasi web dengan framework Flask. Install Flask melalui pip ```pip install flask```

![Screenshot from 2023-03-15 20-12-57](https://user-images.githubusercontent.com/84585203/225322240-cac7f5e2-8fa1-47d3-b917-6189ae49f38f.png)

Buat file ```index.py``` lalu isikan script berikut

```
from flask import Flask
app = Flask(__name__)
@app.route("/")
def helloworld():
    return "Hello Dumbways!"
if __name__ == "__main__":
    app.run()
```

![Screenshot from 2023-03-15 20-15-27](https://user-images.githubusercontent.com/84585203/225322243-714036a8-8dc6-4a3a-a8db-380d20050d49.png)

Pada bagian ```app.run()``` rubah menjadi seperti ini agar bisa diakses dari ip lain atau pc lain

```
app.run(host="0.0.0.0")
```

Jalankan aplikasi dengan command berikut ```python3 index.py```

![Screenshot from 2023-03-15 20-18-04](https://user-images.githubusercontent.com/84585203/225322246-f7e7d379-7243-4a4b-aca2-65093bee985d.png)

Buka ip server dengan port ```5000``` melalui browser

![Screenshot from 2023-03-15 20-20-19](https://user-images.githubusercontent.com/84585203/225322252-b38e37a5-7b8d-4899-a30b-4a7b14de4514.png)
