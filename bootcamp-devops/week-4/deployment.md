# DEPLOYMENT APLIKASI BACKEND
- Masuk ke directory dumbflix-backend ```cd dumbflix-backend``` selanjutnya buat ```Dockerfile``` dan ```docker-copose.yml``` dengan konfigruasi berikut <br>
![image repository](assets/deploy4.png)
![image repository](assets/deploy5.png)

- Masuk ke directory config ```cd config``` dan ```sudo nano config.json``` ubah konfigurasi pada config.json sesuai dengan database <br>
![image repository](assets/deploy7.png)

- Jalankan perintah ```docker-compose build``` untuk membuat image
- Jalankan perintah ```docker-compose up -d``` untuk membuat container dan menjalankannya
- Cek hasil migrate database ```psql -U oman -d dumbflix -h localhost -p 5432``` <br>
![image repository](assets/deploy3.png)

- Masuk ke web browser dan ketik ```https://api.oman.studentdumbways.my.id``` untuk melihat apakah aplikasi backend sudah berjalan <br>
![image repository](assets/deploy1.png)

# DEPLOYMENT APLIKASI FRONTEND
- Masuk ke directory dumbflix-frontend ```cd dumbflix-frontend``` selanjutnya buat ```Dockerfile``` dan ```docker-copose.yml``` dengan konfigruasi berikut <br>
![image repository](assets/deploy8.png)
![image repository](assets/deploy9.png)

- Masuk ke directory src/config ```cd src/config``` lalu edit konfigurasi api.js ```sudo nano api.js``` masukkan url backend<br>
![image repository](assets/deploy6.png)

- Kembali ke directory dumbflix-frontend jalankan perintah ```docker-compose build``` untuk membuat image dan ```docker-compose up -d``` untuk membuat container dan menjalankannya

- Masuk ke web browser dan ketik ```https://oman.studentdumbways.my.id``` untuk melihat apakah aplikasi backend sudah berjalan <br>
![image repository](assets/deploy2.png)