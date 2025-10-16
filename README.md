# Kutt


## Sekilas Tentang Kutt

Kutt adalah sebuah aplikasi web untuk memendekkan URL yang sifatnya open-source. Aplikasi ini memungkinkan pengguna untuk memperpendek URL panjang menjadi URL yang lebih pendek dan mudah dikelola, serta dapat diintegrasikan ke dalam proyek lain. Kutt juga menyediakan fitur manajemen tautan dan dapat disesuaikan dengan kebutuhan pengembang. 

## Instalasi Menggunkan Docker

- Instal Docker
   - Buka Link Dibawah ini
  
  https://www.docker.com/products/docker-desktop/
  
   - Lalu Download
   - Setelah itu install docker nya
- Clone Project
   - Contoh:
     
  ```bash
   git clone https://github.com/thedevs-network/kutt.git
  
cd kutt
- Siapkan file Konfigurasi
   - Contoh :
     
     ```bash
     cp .env.example .env
     
   - Lalu Buka file .env dan Ubah :

     PORT=3000

     DB_HOST=db

     DB_PORT=5432

     DB_USER=postgres

     DB_PASSWORD=password123

     DB_NAME=kutt

     SITE_NAME=Kutt

     DEFAULT_DOMAIN=kutt.local
     
- Jalankan Docker Compose
   - Contoh:

  ```bash
     docker-compose.yml
  
- Jalankan Aplikasi
   - Jalankan semua service
 
     ```bash
     docker compose up -d
     
   - up untuk menjalankan container
   - -d → artinya detached mode
   - 
- Cek Status Container
   - Ketikan
   - 
     ```bash
     docker ps
     
   - Hasil nya menampilkan daftar container yang sedang Berjalan:

     CONTAINER ID   IMAGE             COMMAND                  PORTS                    NAMES

     1a2b3c4d5e6f   kutt_app          "node dist/server.js"    0.0.0.0:3000->3000/tcp   kutt-app

     7g8h9i0j1k2l   postgres:15       "docker-entrypoint..."   5432/tcp                 kutt-db
     
- Akses Dibrowser

  http://localhost:3000
  
- Kutt sudah Aktif
- Jika Mau Stop
  ```bash
  docker compose down


## Konfigurasi (opsional)

Setting server tambahan yang diperlukan untuk meningkatkan fungsi dan kinerja aplikasi, misalnya:
- batas upload file
- batas memori
- dll

Plugin untuk fungsi tambahan
- login dengan Google/Facebook
- editor Markdown
- dll


##  Maintenance (opsional)

Setting tambahan untuk maintenance secara periodik, misalnya:
- buat backup database tiap pekan
- hapus direktori sampah tiap hari
- dll


## Otomatisasi (opsional)

Skrip shell untuk otomatisasi instalasi, konfigurasi, dan maintenance.


## Cara Pemakaian

- Tampilan aplikasi web
- Fungsi-fungsi utama
- Isi dengan data real/dummy (jangan kosongan) dan sertakan beberapa screenshot


## Pembahasan

- Pendapat anda tentang aplikasi web ini
    - kelebihan
    - kekurangan
- Bandingkan dengan aplikasi web lain yang sejenis


## Referensi

Cantumkan tiap sumber informasi yang anda pakai.
