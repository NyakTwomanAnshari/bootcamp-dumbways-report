# WEB SERVER NGINX

## Install Nginx
- Jalankan perintah ```sudo apt install nginx -y``` <br>
![image repository](assets/webserver1.png)

- Kemudian cek status dari nginx ```sudo systemctl status nginx``` <br>
![image repository](assets/webserver2.png)

## Reverse proxy dan load balancing
### Frontend
- Membuat sebuah folder di /etc/nginx ```sudo mkdir frontend``` dan masuk ke directory tersebut ```sudo nano frontend``` dengan konfigurasi sebagai berikut <br>
![image repository](assets/server5.png)

- Kembali ke directory /etc/nginx masuk ke konfigurasi ```sudo nano nginx.conf``` dan masukkan directory yang telah kita buat konfigurasi <br>
![image repository](assets/server7.png)

- Install certbot ```sudo snap install core; sudo snap refresh core``` lalu ```sudo snap install --classic certbot```
- Jalankan certbot dan pilih domain yang ingin diberi SSL <br>
![image repository](assets/webserver7.png)

### Backend
- Membuat sebuah folder di /etc/nginx ```sudo mkdir backend``` dan masuk ke directory tersebut ```sudo nano frontend``` dengan konfigurasi sebagai berikut <br>
![image repository](assets/server6.png)

- Kembali ke directory /etc/nginx masuk ke konfigurasi ```sudo nano nginx.conf``` dan masukkan directory yang telah kita buat konfigurasi <br>
![image repository](assets/server7.png)

- Install certbot ```sudo snap install core; sudo snap refresh core``` lalu ```sudo snap install --classic certbot```
- Jalankan certbot dan pilih domain yang ingin diberi SSL <br>
![image repository](assets/webserver4.png)

### CI/CD
- Membuat sebuah folder di /etc/nginx ```sudo mkdir jenkins``` dan masuk ke directory tersebut ```sudo nano jenkins``` dengan konfigurasi sebagai berikut <br>
![image repository](assets/webserver8.png)

- Kembali ke directory /etc/nginx masuk ke konfigurasi ```sudo nano nginx.conf``` dan masukkan directory yang telah kita buat konfigurasi <br>
![image repository](assets/server7.png)

- Install certbot ```sudo snap install core; sudo snap refresh core``` lalu ```sudo snap install --classic certbot```
- Jalankan certbot dan pilih domain yang ingin diberi SSL <br>
![image repository](assets/webserver5.png)

### Prometheus
- Membuat sebuah folder di /etc/nginx ```sudo mkdir prometheus``` dan masuk ke directory tersebut ```sudo nano prometheus``` dengan konfigurasi sebagai berikut <br>
![image repository](assets/webserver9.png)

- Kembali ke directory /etc/nginx masuk ke konfigurasi ```sudo nano nginx.conf``` dan masukkan directory yang telah kita buat konfigurasi <br>
![image repository](assets/server7.png)

- Install certbot ```sudo snap install core; sudo snap refresh core``` lalu ```sudo snap install --classic certbot```
- Jalankan certbot dan pilih domain yang ingin diberi SSL <br>
![image repository](assets/)

### Grafana
- Membuat sebuah folder di /etc/nginx ```sudo mkdir grafana``` dan masuk ke directory tersebut ```sudo nano grafana``` dengan konfigurasi sebagai berikut <br>
![image repository](assets/webserver10.png)

- Kembali ke directory /etc/nginx masuk ke konfigurasi ```sudo nano nginx.conf``` dan masukkan directory yang telah kita buat konfigurasi <br>
![image repository](assets/server7.png)

- Install certbot ```sudo snap install core; sudo snap refresh core``` lalu ```sudo snap install --classic certbot```
- Jalankan certbot dan pilih domain yang ingin diberi SSL <br>
![image repository](assets/webserver6.png)