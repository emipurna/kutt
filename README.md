# Kutt


## Sekilas Tentang Kutt

Kutt adalah sebuah aplikasi web untuk memendekkan URL yang sifatnya open-source. Aplikasi ini memungkinkan pengguna untuk memperpendek URL panjang menjadi URL yang lebih pendek dan mudah dikelola, serta dapat diintegrasikan ke dalam proyek lain. Kutt juga menyediakan fitur manajemen tautan dan dapat disesuaikan dengan kebutuhan pengembang. 

## Instalasi Menggunkan Docker

- Link Docker
  
https://hub.docker.com/r/kutt/kutt
  
  Jika anda ingin melakukan instalasi via dockernya secara langsung anda dapat mengaksesnya pada link tersebut, namun karena kali ini kita akan menggunakan railway sebagai platform hostnya maka kita sebenarnya tidak perlu menggunakan docker secara manual, semuanya akan disiapkan oleh railway dan kita hanya perlu konfigurasi variabel yang diperlukan nantinya
  
- Link Railway
  -Buka link Railwaynya
  
https://railway.com/

- Selesaikan pembuatan akun lalu masuk ke bagian dashboard
  
https://railway.com/dashboard

- Setelah itu tekan tombol (+ New) untuk membuat projek baru
- Jika berhasil maka layar akan berpindah ke bagian New Project
- Pilih Docker Image
- masukkan " kutt/kutt " di bagian "What would you like to deploy today?"
- Lalu tekan enter pada keyboard

  Railway akan melakukan setup dan deploy secara otomatis, sisanya kita hanya perlu mengkonfigurasi variabel agar websitenya berjalan sesuai keingin kita.


## Konfigurasi

Kita perlu setting beberapa variabel agar website dapat berjalan dengan baik, untuk list lengkap variabel yang bisa diatur di website kutt.it dokumentasinya dapat diakses pada link berikut:
[https://github.com/thedevs-network/kutt?tab=readme-ov-file#configuration]

``` Contoh konfigurasi variable:

DB_FILENAME="/var/lib/kutt/data.sqlite" //mengatur nama db yang akan kita pakai kebetukan kutt bisa menggunakan sqlite yang sangat memudahkan disini jadinya tidak perlu setup database tambahan lagi
DEFAULT_DOMAIN="https://kutt-kdjk-kel1-kiv.up.railway.app" //link default domainnya
JWT_SECRET="bfkk1by2gv0hxwot90wco50dyckd1w3a" //enkripsi untuk password
DISALLOW_REGISTRATION="false" //konfigurasi untuk mengizinkan registrasi atau tidak
DISALLOW_ANONYMOUS_LINKS="false" //konfigurasi untuk apakah user dapat mengakses fitur website secara anonim/tanpa akun
MAILER_SMTP_HOST="" //alamat email host
MAILER_SMTP_PORT="" //port untuk email registrasi
MAILER_SMTP_USER="" //alamat email user
MAILER_SMTP_PASS="" //alamat email untuk mengirim password
MAILER_FROM="" //alamat email pengirim registrasi
MAILER_SECURE="" //apakah email menggunakan ssl secure atau tidak
MAIL_ENABLED="true" //apakah fitur email untuk registrasi dan reset password aktif atau tidak
```
Anda dapat mengatur variable yang ada sesuai dengan preferensi anda sebagai konfigurasi untuk aplikasi ini, setelah anda selesai mengganti variabel jangan lupa restart/redeploy aplikasinya di dashboard railway.

## Deploy
Setelah anda selesai mengatur variabel anda dapat langsung mendeploy aplikasi kutt yang sudah anda konfigurasi dan railway akan menjalankan semua setup sesuai dengan konfigurasi yang telah anda buat.

<img width="1267" height="722" alt="Gambar Petunjuk Deploy Aplikasi di Project Railway" src="https://github.com/user-attachments/assets/49528a5d-6e73-42ca-a3a5-b66765470a7f" />
Tekan "Deploy the image kutt/kutt" untuk mendeploy aplikasi

Kalau deploy berhasil akan muncul tampilan seperti ini:
<img width="1207" height="696" alt="image" src="https://github.com/user-attachments/assets/cc4b98c8-f002-4bde-9b18-9efe8b616d91" />

Selamat Website aplikasi kutt anda telah berhasil dideploy.


## Cara Pemakaian

-Sebagai admin
Sebagai admin yang baru pertama kali membuka link aplikasi anda akan diarahkan ke halaman pembuatan akun admin
Masukkan email dan password yang ingin anda gunakan sebagai user admin di aplikasi
<img width="1914" height="944" alt="image" src="https://github.com/user-attachments/assets/c38e2658-f8e0-4322-8681-8260cd95fb01" />

Setelah pembuatan akun selesai anda dapat melakukan login menggunakan akun admin anda dan setelah login anda dapat mengakses menu admin yang di dalamnya ada menu sebagai berikut:
- Melihat dan mengatur link yang ingin dipendekkan oleh user
- Melihat dan mengatur user yang sudah ada
- Mengatur custom domain untuk short link

-Sebagai user
Sebagai user anda dapat mengakses aplikasi ini dengan dua cara tergantung konfigurasi aplikasinya
   - Sebagai user dengan akun:
      - login atau register terlebih dahulu ke website
      - setelah berhasil anda akan masuk ke dashboard utama
      - anda bisa langsung memendekkan url dengan cara memasukkan link yang ingin anda pendekkan ke kotak yang paling besar di tengah lalu tekan enter dan link shortened akan muncul di atas kotak dan dapat dicopy dengan cara menekan link dengan kursor
<img width="1916" height="668" alt="image" src="https://github.com/user-attachments/assets/d6c9d1c8-5c3a-4a8a-b60b-5854c8540e6e" />
<img width="1732" height="483" alt="image" src="https://github.com/user-attachments/assets/e041cecf-f83c-4175-a77f-453963d48be6" />

      - anda dapat mengaktifkan show advanced option untuk mengatur setting shorten url lebih detil sesuai preferensi anda (password, nama custom link, waktu expire, dan deskripsi)
<img width="1624" height="671" alt="image" src="https://github.com/user-attachments/assets/6e2968b9-4354-4d3d-b6e4-f1ae9dea0b3f" />
        
   - Sebagai User Anonim
     Jika aplikasi mengizinkan user anonim maka anda dapat langsung memendekkan link seperti halnya user dengan akun tanpa harus login, namun anda harus berhati-hati karena history link yang anda buat mungkin bisa hilang kalau anda meninggalkan website maka pastikan anda menyimpan link sesuai kebutuhan anda.
        



## Pembahasan

- Pendapat anda tentang aplikasi web ini
    - kelebihan
    - kekurangan
- Bandingkan dengan aplikasi web lain yang sejenis


## Referensi

Cantumkan tiap sumber informasi yang anda pakai.
