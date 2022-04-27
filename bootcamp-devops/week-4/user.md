# Membuat user baru pada semua server

- Jalankan perintah ```sudo apt install whois``` lalu jalankan ```mkpasswd --method=sha-512``` untuk mengenerate enkripsi dari password <br>
![image repository](assets/user1.png)

- Membuat file ansible ```user.yml``` dengan konfigurasi sebagai berikut dan copy generate password yang terenkripsi ke dalam file konfigurasi ansible tersebut<br>
![image repository](assets/user2.png)

- Jalankan ```ansible-playbook user.yml```