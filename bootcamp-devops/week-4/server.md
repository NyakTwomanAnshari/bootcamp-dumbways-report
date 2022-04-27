# MEMBUAT SERVER
- Server app & database
- Server nginx
- Server monitoring
- Server CI/CD

## Menginstall docker di semua server
- Buat ```Inventory``` ansible dengan konfigurasi berikut <br>
![image repository](assets/server1.png)

- Buat ```ansible.cfg``` dengan konfigurasi berikut <br>
![image repository](assets/server2.png)

- Buat sshkey.pem ```sudo nano sshkey.pem``` dan copy id_rsa dari server ke sshkey.pem <br>
![image repository](assets/server3.png)

- Konfigurasi ansible meng-install docker dan docker-compose ```docker.yml```<br>
![image repository](assets/server4.png)

- Jalankan ```ansible-playbook docker.yml```

## Load Balancing
- Masuk ke server nginx
- Buat directory baru untuk menyimpan konfigurasi load balancing ```cd /etc/nginx``` lalu ```mkdir frontend``` dan ```mkdir backend```
- Masuk ke directory frontend ```cd frontend``` buat sebuah file ```sudo nano frontend``` dengan konfigurasi sebagai berikut <br>
![image repository](assets/server5.png)

- Kembali ke directory /etc/nginx

- Masuk ke directory backend ```cd backend``` buat sebuah file ```sudo nano backend``` dengan konfigurasi sebagai berikut <br>
![image repository](assets/server6.png)

- Kembali ke directory /etc/nginx jalankan perintah ```sudo nano nginx.conf``` tambahkan folder tadi pada baris include <br>
![image repository](assets/server7.png)