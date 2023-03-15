# PM2

Download dan Install pm2 dengan command berikut:

```
npm install pm2@latest -g
```

![Screenshot from 2023-03-15 21-16-12](https://user-images.githubusercontent.com/84585203/225338806-8615804b-80e2-49c4-b42b-8f17b454f93f.png)

Jalankan aplikasi node yang sudah dibuat sebelumnya dengan command berikut :

```
pm2 start app-nodejs/index.js
```
![Screenshot from 2023-03-15 21-18-54](https://user-images.githubusercontent.com/84585203/225338820-af90e549-6ad0-48f2-af21-ad2f94650754.png)

Jalankan aplikasi python yang sudah dibuat sebelumnya dengan command berikut :

```
pm2 start app-python/index.py --interpreter python3
```
![Screenshot from 2023-03-15 21-19-45](https://user-images.githubusercontent.com/84585203/225338826-ed48b652-dafa-42f5-ac66-095a6821055d.png)

Untuk melihat process pm2 yang sudah perjalan, gunakan command berikut:

```
pm2 list
```

![Screenshot from 2023-03-15 21-20-07](https://user-images.githubusercontent.com/84585203/225338833-e31430df-ef27-4314-83ae-e5836a937f2a.png)

Cek melalui browser untuk mengecek apakah aplikasi sudah berjalan:

![Screenshot from 2023-03-15 21-21-32](https://user-images.githubusercontent.com/84585203/225338841-db09dd69-7fe1-49af-ba81-4c89e7073d9d.png)
![Screenshot from 2023-03-15 21-21-35](https://user-images.githubusercontent.com/84585203/225338863-89f1b92f-6954-448b-b983-de1be3b9dca4.png)
