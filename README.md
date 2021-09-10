# Laporan ADJ

Nama : Jefry Lianto

NIM  : 191402027

KOM  : C

# Buatlah sebuah web statis menggunakan docker.

1. Download Docker Desktop 
https://docs.docker.com/get-docker/

![image](https://user-images.githubusercontent.com/65750641/132794036-3467e415-22ea-41dc-af91-fa4bae28f50c.png)

2. Setelah menginstall docker, buatlah sebuah folder untuk project web statis. Tambahkan 
sebuah file dengan nama Dockerfile tanpa ekstensi.

![image](https://user-images.githubusercontent.com/65750641/132794064-68eb8531-9156-46f1-9078-ef1ff1eed293.png)

![image](https://user-images.githubusercontent.com/65750641/132794072-c674ecbe-661f-48f3-880c-af604b134bc8.png)

3. Pada Dockerfile ketikkan code berikut.

![image](https://user-images.githubusercontent.com/65750641/132794156-282cc69b-4c59-4283-b97c-23c86a6c75cd.png)

Kode tersebut bertujuan juga menerapkan docker image nginx versi alpine dan bertujuan 
untuk menerapkan semua file website statis pada direktori tersebut sebagai docker image.

4. Setelah selesai, editlah file html tersebut dan jalankan perintah untuk membentuk docker 
image di cmd. Pastikan docker sudah terhubung. 

docker build -t nama-images:versi-app . 

![image](https://user-images.githubusercontent.com/65750641/132794346-11f0a5aa-ead9-4097-9003-1eebba297d62.png)


5. Setelah itu buat container baru dari docker image yang sudah dibentuk dan jalankan. 

docker run -d –name nama-container -p destination-port:request-port images 

![image](https://user-images.githubusercontent.com/65750641/132794395-babf8c06-a958-49b0-b593-3fa50da9f67b.png)

![image](https://user-images.githubusercontent.com/65750641/132794399-ea4e4d1c-6931-427c-b609-6902e7cc97d6.png)


6. Masuk ke localhost:127 untuk mengecek apakah container yang kita buat dengan port:127 
sudah bisa diakses atau tidak. 

![image](https://user-images.githubusercontent.com/65750641/132794418-ec417975-4c1c-4e8d-b29d-0c9b3e23d450.png)


7. Untuk menghentikan container, dapat menggunakan perintah docker stop container-name. 

![image](https://user-images.githubusercontent.com/65750641/132794433-f939e4be-41c1-4967-8010-2637b0bbc37d.png)

![image](https://user-images.githubusercontent.com/65750641/132794442-eaee8e25-5049-41b6-a662-38aa413beae2.png)


# Publish docker images ke github.

1. Buat repository baru di github.

![image](https://user-images.githubusercontent.com/65750641/132794825-d4fe88ed-1a20-42b5-b9b2-4c6a9a8d71d0.png)

2. Buatlah token baru yang akan digunakan. 

![image](https://user-images.githubusercontent.com/65750641/132794836-104ea42f-ac3d-47c4-be6e-4431dbb2c7b4.png)

3. Setelah membuat token, buka cmd dan login docker pada cmd, token berfungsi sebagai 
password. 

![image](https://user-images.githubusercontent.com/65750641/132794850-307a126b-4e41-4e54-b2b4-1f90dc95ae33.png)

4. Setelah itu, copy id dari image pictures yang akan di upload. Setelah itu buatlah duplikat 
docker images nya.

![image](https://user-images.githubusercontent.com/65750641/132794865-97be493a-f791-4431-b772-caae70c3d854.png)

![image](https://user-images.githubusercontent.com/65750641/132794875-1588c2f6-2199-44a7-987f-26c62c4f6e75.png)

5. Publish docker image ke github dengan command push. 

![image](https://user-images.githubusercontent.com/65750641/132794888-3f5f2634-051e-453b-bdaf-ee88906f2551.png)

6. Images telah di publish di github

![image](https://user-images.githubusercontent.com/65750641/132794907-498136ad-1fe5-40ff-94b2-b92838cf7adf.png)
