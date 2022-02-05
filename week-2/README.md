# INSTALATION UBUNTU SERVER AND BASIC SHELL SCRIPTING
## Instalation Ubuntu Server and VMware
### Instalation VMware
- Langkah pertama download VMware pada link ```https://www.vmware.com/products/workstation-player.html```
- Kemudian, masuk ke directory yang ada file VMware yang sudah terdownload
- Jika sudah di directory tersebut, maka buka terminal pada directory tersebut
- Lalu masukkan perintah ```sudo sh VMware-Player-Full-16.2.1-18811642.x86_64.bundle``` untuk melakukan instalasi <br>
![image VMware](assets/1.png) <br>
- Apabila proses instalasi selesai maka VMware siap digunakan.
  
### Instalation Ubuntu Server
Langkah-langkah menginstall: <br>
- Buka VMware yang sudah di install <br>
![image VMware](assets/2.png) <br>
- Download ISO Ubuntu Server terlebih dahulu pada link ```https://ubuntu.com/download/server``` pilih yang manual server installation
- Apabila sudah terdownload maka masuk ke VMware lalu pilih ```create a new virtual machine```
- Jika sudah maka pilih ```Use ISO image``` lalu masukkan ISO yang telah terdownload tadi <br>
![image VMware](assets/3.png) <br>
- Lalu pilih operating system yang akan di install <br>
![image VMware](assets/4.png) <br>
- Kemudian pilih directory mana yang ingin menyimpan instalasi ubuntu server tersebut <br>
![image VMware](assets/5.png) <br>
- Selanjutnya masukkan disk size yang di inginkan, recomended dari VMware 20GB <br>
![image VMware](assets/6.png) <br>
- Jika sudah, maka pilih customize hardware sesuai kebutuhan <br>
![image VMware](assets/7.png) <br>
![image VMware](assets/8.png) <br>
![image VMware](assets/9.png) <br>
![image VMware](assets/10.png) <br>
- Apabila semua step diatas sudah selesai maka pilih ```close``` dan ```finish```
- Selanjutnya masuk ke Virtual Machine yang sudha selesai dibuat lalu pilih ```power on``` <br>
![image VMware](assets/11.png) <br>
- Tunggu hingga sampai muncul pilihan bahasa, pastikan memilih seperti step dibawah <br>
![image VMware](assets/12.png) <br>
![image VMware](assets/13.png) <br>
![image VMware](assets/14.png) <br>
![image VMware](assets/15.png) <br>
- Jika sudah masuk ke tahapan Network Connections, pilih ```IPv4 Method Manual (DHCP)``` <br>
![image VMware](assets/16.png) <br>
- Apabila sudah selesai pilih save dan lanjut ke tahap selanjutnya <br>
![image VMware](assets/17.png) <br>
![image VMware](assets/18.png) <br>
![image VMware](assets/19.png) <br>
![image VMware](assets/20.png) <br>
![image VMware](assets/21.png) <br>
![image VMware](assets/22.png) <br>
- Kemudian jangan lupa pilih ```install OpenSSH server``` <br>
![image VMware](assets/23.png) <br>
- Jika sudah tunggu sampai instalasi selesai <br>
![image VMware](assets/24.png) <br>
- Apabila sudah selesai instalasi maka pilih ```reboot now```
- Kemudian masuk ke ubuntu server yang sudah selesai terinstall dengan memasukkan username dan password <br>
![image VMware](assets/25.png) <br>
- Selanjutnya ketik perintah ```ping google.com``` untuk mencoba terhubung ke internet atau tidak
- Jika ada notice ```ping google.com: temporary failure in name resolution``` berarti gagal terhubung ke internet <br>
![image VMware](assets/26.png) <br>
- Untuk itu perlu mengganti IP Address
- Ketik perintah ```cd /etc``` kemudian ```cd /netplan``` lalu masuk ke file ```sudo nano 00-installer-config.yaml``` <br>
![image VMware](assets/27.png)
- Kemudian ganti IP pada file tersebut dengan IP pada komputer yang digunakan
- Untuk melihat IP Address pada komputer dengan cara mengetik perintah ```ifconfig``` <br>
![image VMware](assets/28.png) <br>
- Selanjutnya masukkan IP Address sesuai dengan IP pada komputer dengan mengganti gateway 255 menjadi 1
- Apabila sudah IP sudah terganti maka ketik perintah ```netplan apply``` untuk mengkonfirmasi IP yang telah diubah tadi
- Lalu tes apakah sudah terhubung ke internet dengan mengetik perintah ```ping google.com``` jika berhasil maka akan menghasilkan outpu seperti dibawah <br>
![image VMware](assets/29.png) <br>
- Sekarang coba masuk menggunakan SSH lewat terminal pada operating system linux dengan mengetik perintah ```ssh oman@192.168.100.5``` <br>
![image VMware](assets/30.png) <br>
- Untuk keluar dari linux server menggunakan perintah ```logout``` <br>
![image VMware](assets/31.png) <br>