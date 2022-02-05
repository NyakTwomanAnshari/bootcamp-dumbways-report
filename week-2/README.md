# INSTALATION UBUNTU SERVER AND BASIC SHELL SCRIPTING (BASH)
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
- Lalu tes apakah sudah terhubung ke internet dengan mengetik perintah ```ping google.com``` jika berhasil maka akan menghasilkan output seperti dibawah <br>
![image VMware](assets/29.png) <br>
- Sekarang coba masuk menggunakan SSH lewat terminal pada operating system linux dengan mengetik perintah ```ssh oman@192.168.100.5``` <br>
![image VMware](assets/30.png) <br>
- Untuk keluar dari linux server menggunakan perintah ```logout``` <br>
![image VMware](assets/31.png) <br>

## Basic Shell Scripting (Bash)
BASH (Bourne Again Shell) adalah bahasa yang berjalan di atas kernel (linux/unix), yang berfungsi sebagai interpreter antara pengguna dan sistem operasi.

### Linux Commands
- ```mkdir``` perintah yang digunakan untuk membuat sebuah directory <br>
![image linux commands](assets/32.png) <br>
- ```ls``` perintah yang digunakan untuk menampilkan file dan directory dalam suatu sistem <br>
![image linux commands](assets/33.png) <br>
- ```la -la``` perintah yang digunakan untuk menampilkan semua file dan directory yang tersembunyi dalam suatu sistem <br>
![image linux commands](assets/34.png) <br>
- ```cd``` perintah yang digunakan untuk berpindah dari directory ke directory lain
![image linux commands](assets/35.png) <br>
- ```touch``` perintah yang digunakan untuk membuat suatu file kosong <br>
![image linux commands](assets/36.png) <br>
- ```cp``` perintah yang digunakan untuk menduplikat suatu file <br>
![image linux commands](assets/37.png) <br>
- ```mv``` perintah yang digunakan untuk memindahkan file dan merubah nama dari suatu file <br>
![image linux commands](assets/38.png) <br>
- ```echo``` perintah yang digunakan untuk menampilkan string dan memasukkan text kedalam file <br>
![image linux commands](assets/39.png) <br>
- ```cat``` perintah yang digunakan untuk menampilkan text di dalam suatu file <br>
![image linux commands](assets/40.png) <br>
- ```find type -f``` perintah yang digunakan untuk mencari file <br>
![image linux commands](assets/41.png) <br>
- ```find type -d``` perintah yang digunakan untuk mencari directory <br>
![image linux commands](assets/42.png) <br>
- ```grep``` perintah yang digunakan untuk mencari text di dalam file <br>
![image linux commands](assets/43.png) <br>
- ```chmod``` perintah yang digunakan untuk mengubah permisson file atau directory <br>
![image linux commands](assets/44.png) <br>
- ```chwon``` perintah yang digunakan untuk mengubah kepemilikan dari file atau directory <br>
![image linux commands](assets/46.png) <br>
- ```history``` perintah yang digunakan untuk menampilkan riwayat dari commands sistem <br>
![image linux commands](assets/47.png) <br>
- ```history | grep``` perintah yang digunakan untuk mencari text dari riwayat commands sistem <br>
![image linux commands](assets/48.png) <br>
- ```ping``` perintah yang digunakan untuk mengecek koneksi internet <br>
![image linux commands](assets/49.png) <br>
- ```wget``` perintah yang digunakan untuk mendownload file <br>
![image linux commands](assets/50.png) <br>
- ```unzip``` perintah yang digunakan untuk mengekstrak suatu file .zip <br>
![image linux commands](assets/51.png) <br>
- ```zip``` perintah yang digunakan untuk mengcompress suatu file atau directory menjadi file .zip <br>
![image linux commands](assets/52.png) <br>
- ```adduser``` perintah yang digunakan untuk menambahkan user baru di sistem <br>
![image linux commands](assets/45.png) <br>
- ```usermod``` perintah yang digunakan untuk menambahkan user ke dalam group sudo, sehingga pengguna bisa menggunakan syntax sudo <br>
![image linux commands](assets/53.png) <br>
- ```deluser``` perintah yang digunakan untuk menghapus user dari sistem <br>
![image linux commands](assets/54.png) <br>