# TCExam Mobile Friendly Docker
Install TCE Mobile Friendly dengan cepat menggunakan Docker.

## Instalasi
### 1 - Spesifikasi server
- Sistem operasi : Ubuntu atau Debian (semua versi dengan akses root)
- RAM : 1GB (minimal) atau 8GB (direkomendasikan)
- Penyimpanan : 10GB (minimal) atau 40GB (direkomendasikan)
- Jumlah core : 1 (minimal) atau 4 (direkomendasikan)
### 2 - Depedensi
Untuk bisa menjalankan perangkat lunak ini diperlukan Git, Docker dan Docker Compose. Petunjuk instalasi Docker dan Docker Compose : [Ubuntu](https://docs.docker.com/engine/install/ubuntu/) / [Debian](https://docs.docker.com/engine/install/debian/). Sedangkan untuk menginstall git menggunakan perintah sebagai berikut :
```shell
apt install git
```
### 3 - Download dan Menjalankan Docker Compose
- clone repository dengan perintah berikut
```shell
git clone https://github.com/teguh-santoso/tcemf-docker.git
```
- ubah permission folder tcemf-docker
```shell
chown -R www-data:www-data tcemf-docker
```
- Masuk ke folder tcemf-docker
- Ubah file .env sesuai kebutuhan
- Jalankan perintah berikut
```shell
docker compose up -d
```
### 4 - Konfigurasi TCEMF
- Buka halaman instalasi TCEMF : http://localhost/install/install.php
- Sesuaikan parameter isian instalasi tersebut dengan file .env yang telah anda ubah sebelumnya
- Pada hostname mysql masukkan ```mysql```
- Akun default untuk login administrator adalah
```shell
username : admin
password : 1234
```
- Segera ubah akun default setelah berhasil login
