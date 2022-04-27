# Setup Node Exporter, Prometheus, and Grafana

## Install Node Exporter
- Pada konfigurasi ```Inventrory``` masukkan semua IP server untuk menginstall node_exporter <br>
![image monitoring](assets/server1.png)

- Buat konfigurasi ```sudo nano docker-compose-node_exporter.yml``` dengan konfigurasi berikut <br>
![image monitoring](assets/monitoring8.png)

- Buat konfigurasi ansible ```sudo nano node_exporter.yml``` dengan konfigurasi berikut <br>
![image monitoring](assets/monitoring9.png)

- Jalankan ```ansible-playbook node_exporter.yml``` tunggu hingga selesai

## Install Prometheus & Grafana
- Buat konfigurasi untuk membaca node_exporter pada file ```prometheus.yml``` <br>
![image monitoring](assets/monitoring10.png)

- Buat file ```docker-compose-monitoring.yml``` untuk menginstall prometheus dan grafana <br>
![image monitoring](assets/monitoring11.png)

- Buat konfigurasi ansible untuk mendeploy prometheus dan grafana menggunakan docker ```monitoring.yml``` <br>
![image monitoring](assets/monitoring12.png)

- Jalankan ```ansible-playbook monitoring.yml``` <br>

- Buka web browser ketik ```https://monitoring.oman.studentdumbways.my.id``` untuk grafana dan prometheus ```https://prometheus.oman.studentdumbway.my.id``` <br>
![image monitoring](assets/monitoring13.png)
![image monitoring](assets/monitoring4.png)
![image monitoring](assets/monitoring3.png)
![image monitoring](assets/monitoring2.png)
![image monitoring](assets/monitoring14.png)