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

# VERSION CONTROL WITH GIT
Version Control Systems adalah alat yang digunakan untuk mengelola perubahan kode. Tools ini dapat membantu pengembang untuk melacak setiap perubahan yang dilakukan secara terus menerus, VCS (Version Control System) pada dasarnya memiliki database terpusat yang online, jika ingin menggunakannya harus terhubung ke jaringan. <br>

Contoh Version Control Application: <br>
- GIT
- SVN
- CSV
- Mercurial

## Dokumentasi Perintah Setiap Perintah GIT
### Tahapan pada GIT
- Modified adalah tahapan dimana perubahan dilakukan dalam file namun belum ditandai dan disimpan pada git.
- Staged adalah tahapan menandai revisi yang sudah dilakukan tetapi belum disimpan dalam git (biasanya menggunakan perintah ```git add```)
- Commited adalah tahapan rivisi sudah disimpan dalam git (menggunakan perintah ```git commit```)
### Install GIT dan Konfigurasi SSH Key
- Pertama install git pada terminal terlebih dahulu apabila belum terinstall git pada linux dengan perintah ```sudo apt install git -y```
- Jika proses instalasi selesai maka bisa megecek version dari git yang terinstall dengan perintah ```git --version``` <br>
![image git](assets/59.png) <br>
- ```git config``` adalah suatu perintah git untuk mengatur suatu konfigurasi tertentu sesuai keinginan pengguna seperti membuat username dan password
  - ```git config --global user.name"oman"``` perintah untuk mengatur email dari user
  - ```git config --global user.email"oman.anshari@gmail.com"``` perintah untuk mengatur email user
  - ```git config --list``` perintah yang digunakan untuk melihat user dan email yang digunakan <br>
  ![image git](assets/58.png) <br>
- Konfigurasi SSH Key dengan menajalankan perintah ```ssh-keygen``` <br>
![image git](assets/55.png) <br>
  - Kemudian jalankan perintah ```cd .ssh``` dan ```cat id_rsa.pub``` untuk melihat SSH Key <br>
    ![image git](assets/56.png) <br>
  - Copy SSH Key yang muncul dan masukkan ke dalam config github dengan cara membuka github.com, lalu pilih menu setting. Kemudian pilih SSH and GPG Keys, selanjutnya pilih new SSH Key dan isi dengan SSH Key yang sudah di copy, berikan judul dan pilih Add SSH Key. <br>
    ![image git](assets/60.png) <br>
  -  Jika sudah maka akan muncul SSH Key tadi pada menu setting, maka SSH Key akan otomatis masuk ke profil. <br>
    ![image git](assets/61.png) <br>
  - Bisa juga di cek pada terminal linux dengan menggunakan perintah ```ssh -T git@github.com``` maka akan menghasilkan output seperti dibawah <br>
    ![image git](assets/57.png) <br>
- ```git init``` adalah suatu perintah untuk membuat repository baru <br>
  - contoh: ```git init oman``` maka akan menghasilkan satu repository baru dengan nama "oman" <br>
  ![image git](assets/62.png) <br> 
- ```.gitignore``` adalah suatu perintah untuk membuat suatu file yang berisi daftar file atau directory yang akan di abaikan oleh git <br>
  - contoh: ```touch .gitignore``` dan buat beberapa file dengan perintah ```touch file1 file2 file3``` <br>
  ![image git](assets/64.png) <br>
  - Kemudian ketik perintah ```nano .gitignore``` untuk memasukkan file yang akan diabaikan oleh git
  - ```git status``` perintah untuk menampilkan daftar file yang berubah bersama dengan file yang ingin ditambahkan atau di commit <br>
  ![image git](assets/66.png) <br>
- ```git add``` perintah untuk menambahkan file atau directory ke index
  - contoh: ```git add .``` perintah untuk menambahkan semua file kecuali, yang terdaftar pada ```.gitignore``` <br>
  ![image git](assets/67.png) <br>
- ```git commit``` perintah untuk melakukan commit pada perubahan ke head
  - ```git commit -m "first commit"``` untuk melakukan commit dengan pesan "first commit" <br>
  ![image git](assets/68.png) <br>
  - Masukkan perintah ```git status`` untuk melihat file sudah tersimpan pada database git <br>
  ![image git](assets/69.png) <br>
- ```git remote``` perintah untuk membuat user terhubung ke remote repository 
  - ```git remote -v``` perintah untuk menampilkan repository yang terkonfigurasi <br>
  ![image git](assets/71.png) <br>
  - contoh: Melakukan remote pada layanan github
  - Pertama membuat repository github 
  - Kemudia masukkan deskripsi atau optional
  - Lalu tentukan repository berjenis public atau private
  - Selanjutnya create repository <br>
  ![image git](assets/72.png) <br>
  - Apabila proses pembuatan repository selesai, maka jalankan perintah ```git branch -M main``` perintah ini digunakan untuk mengubah nama branch master menjadi main <br>
  ![image git](assets/73.png)<br>
  - Kemudian ketik perintah ```git remote add origin git@github.com:NyakTwomanAnshari/oman.git``` perintah ini digunakan untuk menambahkan remote <br>
  ![image git](assets/70.png) <br>
  - Lalu ketik perintah ```git push -u origin main``` perintah ini digunakan untuk mengupload data dari repository komputer ke repository github, pada kasus ini terupload pada branch main <br>
  ![image git](assets/74.png) <br>
  - Apabila sudah selesai maka cek repository github <br>
  ![image git](assets/75.png) <br>
- ```git branch``` perintah yang digunakan untuk membuat versi/branch dari repository. ```git branch -a``` perintah yang digunakan untuk melihat branch aktif. ```git branch nama-branch-baru``` perintah yang digunakan untuk membuat branch baru. ```git branch -d nama-branch``` perintah yang digunakan untuk menghapus branch. <br>
- ```git checkout``` perintah yang digunakan untuk berpindah antar branch. <br>
![image git](assets/77.png) <br>
- ```git push``` perintah yang digunakan untuk mengupload data dari repository komputer ke repository github.
  - contoh: Membuat branch dengan nama production ```git branch production``` kemudian untuk melihat branch yang aktif sekarang ```git branch -a``` <br>
  ![image git](assets/76.png) <br>
  - Lalu pindah dari branch main ke branch production dengan perintah ```git checkout production```
  - Jika sudah berpindah ke branch production untuk melihatnya ketik perintah ```git branch -a``` <br>
  ![image git](assets/78.png) <br>
  - ```git add .``` untuk menambahkan semua file
  - Apabila sudah maka ketik perintah ```git commit -m "update production"``` <br>
  ![image git](assets/79.png) <br>
  - Ketik perintah ```git push -u origin production``` <br>
  ![image git](assets/80.png) <br>
  - Jika sudah periksa branch di github, jangan lupa untuk berpindah branch <br>
  ![image git](assets/81.png) <br>
- ```git pull``` perintah untuk memperbaharui repository pada komputer atau menyamakan dengan repository github.
  - contoh: Masuk ke github lalu pilih menu add file dan selanjutnya create new file <br>
  ![image git](assets/83.png) <br>
  - Kemudian masukkan nama file dan isi dari file tersebut lalu pilih commit <br>
  ![image git](assets/82.png) <br>
  - Apabila sudah masuk ke terminal ketik perintah ```git pull origin production``` <br>
  ![image git](assets/84.png) <br>
- ```git clone``` perintah untuk mengunduk repository github ke repository komputer
  - contoh: Clone repository dari tensorflow untuk mendeteksi objek menggunakan tensorflow
  - Ketik perintah ```git clone https://github.com/tensorflow/models.git``` <br>
  ![image git](assets/86.png) <br>
- ```git rm``` perintah untuk menghapus file dari directory.
  - contoh: ```git rm file1``` <br>
  ![image git](assets/87.png) <br>
- ```git show``` perintah untuk menampilkan informasi objek pada git <br>
![image git](assets/88.png) <br>
- ```git merge``` perintah untuk menggabungkan sebuah branch ke branch yang aktif <br>
![image git](assets/105.png) <br>

## Study Case GIT Merge Branch Development, Staging, dan Production
- Pertama membuat repository baru di github dengan nama study-case <br>
![image git](assets/89.png) <br>
- Kemudian ketik perintah ```git init study-case``` pada terminal <br>
![image git](assets/90.png) <br>
- Lalu masuk ke diretory study-case dengan perintah ```cd study-case```<br>
![image git](assets/91.png) <br>
- Buat suatu file bernama ```main.py``` <br>
![image git](assets/92.png) <br>
- Jika sudah buka text editor lalu diisi dengan print ("Hello World!") dengan perintah ```nano main.py```<br>
![image git](assets/93.png) <br>
- Ketik perintah ```git status``` untuk melihat daftar file <br>
![image git](assets/94.png) <br>
- Selanjutnya ketik perintah ```git add .``` untuk menambahkan semua file ke index <br>
![image git](assets/95.png) <br>
- Lalu cek dengan perintah ```git status``` <br>
![image git](assets/96.png) <br>
- Ketik perintah ```git commit -m "first commit"``` untuk melakukan commit <br>
![image git](assets/97.png) <br>
- Kemudia cek kembali menggunakan peritah ```git status``` <br>
![image git](assets/98.png) <br>
- Ubah nama branch menjadi ```main``` dengan perintah ```git branch -m main```<br>
![image git](assets/99.png) <br>
- Selanjutnya buat remote dengan perintah ```git remote add origin git@github.com:NyakTwomanAnshari/study-case.git``` <br>
![image git](assets/100.png)<br>
- Lalu push terlebih dahulu branch ```main``` dengan perintah ```git push -u origin main``` <br>
![image git](assets/101.png)<br>
- Jika sudah buat branch Development, Staging, dan Production dengan perintah ```git branch Development``` ```git branch Staging``` ```git branch Production``` <br>
![image git](assets/102.png)<br>
- Lihat dari daftar branch yang telah dibuat dengan perintah ```git branch -a``` <br>
![image git](assets/103.png)<br>
- Kemudian pindah ke branch Development dengan perintah ```git checkout Development``` <br>
![image git](assets/104.png)<br>
- Gunakan perintah ```git merge Development``` ```git merge Staging``` ```git merge Production``` untuk menggabungkan branch dengan branch aktif <br>
![image git](assets/105.png)<br>
- Apabila sudah, push satu persatu branch dengan perintah ```git push -u origin Development``` ```git push -u Staging``` ```git push-u Production``` <br>
![image git](assets/106.png)<br>
![image git](assets/107.png)<br>
![image git](assets/108.png)<br>
- Jika sudah selesai cek repository github pada masing-masing branch sudah ada file ```main.py``` <br>
![image git](assets/109.png)<br>
![image git](assets/110.png)<br>
![image git](assets/111.png)<br>