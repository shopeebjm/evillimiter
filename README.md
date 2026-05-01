<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=TikTok+@shopee.bjm" />
</p>
<p align="center">
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=e+v+i+l+l+i+m+i+t+e+r" />
</p>

<h2 align="center">
  
[![Powered By:shopeebjm](https://img.shields.io/badge/PoweredBy:shopeebjm-7%2B-blue.svg?style=flat)](http://shopee.co.id/infinixnote40bjm)

<img src="https://img.shields.io/badge/Version-1.0.0-blue.svg"></h2>

</p>

- Pasang Aplikasi Termux Di Android Tetapi Untuk Aplikasi Termux Jangan Di Unduh Di Playstore Karena Bisa Menyebabkan Error
<h2 align="center">

Unduh Aplikasi Termux Nya Dibawah Ini

👇👇

[![termux](https://img.shields.io/badge/termux-83%2B-yellow.svg?style=flat)](https://sfile.co/eZK8yBBtOiv)

[![Android](https://img.shields.io/badge/Android-15-green.svg?style=flat)](https://developer.android.com/about/versions/15?hl=id)

<p align="center"><img src="https://i.imgur.com/CBGh0Yx.png" /></p>

# Evil Limiter

[![License Badge](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Compatibility](https://img.shields.io/badge/python-3-brightgreen.svg)](PROJECT)

[![Open Source Love](https://badges.frapsoft.com/os/v3/open-source.svg?v=102)](https://github.com/ellerbrock/open-source-badge/)

Sebuah alat untuk memantau, menganalisis, dan membatasi bandwidth (unggah/unduh) perangkat di jaringan lokal Anda tanpa akses fisik atau administratif.<br>
```evillimiter``` Menggunakan [ARP spoofing](https://en.wikipedia.org/wiki/ARP_spoofing) dan [traffic shaping](https://en.wikipedia.org/wiki/Traffic_shaping) Untuk Membatasi Bandwidth host Dijaringan.

**Mencari Versi Yang Kompatibel Dengan Windows?**<br>
Coba Alternatif Open-Source [EvilLimiter for Windows](https://github.com/bitbrute/evillimiter-windows).

## Persyaratan
- Distribusi Linux
- Python 3 Atau Lebih Tinggi

Paket Python Yang Mungkin Hilang Akan Diinstall Selama Proses Installasi

## Command Prompt On Termux

```
$ apt update && apt upgrade -y
```
```
$ apt install git -y
```
```
$ apt install tsu
```
```
$ apt install python3
```
```
$ git clone https://github.com/shopeebjm/evillimiter.git
```
```
$ cd evillimiter
```
```
$ sudo python3 setup.py install
```

Alternatifnya, Anda Dapat Mengunduh Versi Yang Diinginkan Dari [Release page](https://github.com/shopeebjm/evillimiter/releases).<br>

## Penggunaan

Ketik ```evillimiter``` Atau ```python3 bin/evillimiter``` Untuk Menjalankan Tools Ini.

```evillimiter``` Akan Mencoba Untuk Menyelesaikan Informasi Yang Dibutuhkan (network interface, netmask, gateway address) Dengan Sendirinya, Secara Otomatis.

#### Command-Line Arguments

| Argumen | Penjelasan |
| -------- | ----------- |
| ```-h``` | Menampilkan Pesan Bantuan Yang Mencantumkan Semua Argumen Baris Perintah |
| ```-i [Interface Name]``` | Menemukan Antarmuka Jaringan (Akan Ditentukan Jika Tidak Ditentukan)|
| ```-g [Gateway IP Address]``` | Menentukan Alamat IP Gateway  (Akan Diresolusi Jika Tidak Ditentukan)|
| ```-m [Gateway MAC Address]``` | Menentukan Alamat MAC Gateway (Akan Diresolusi Jika Tidak Ditentukan)|
| ```-n [Netmask Address]``` | Menentukan Netmask (Akan Diresolusi Jika Tidak Ditentukan)|
| ```-f``` | Menghapus Konfigurasi iptables Dan tc Saat Ini.Memastikan Bahwa Paket Ditangani Dengan Benar.|
| ```--colorless``` | Menonaktifkan Output Berwarna |

#### ```evillimiter``` Commands

| Command | Penjelasan |
| ------- | ----------- |
| ```scan (--range [IP Range])``` | Memindai Jaringan Anda Untuk Host Online. Salah Satu Hal Pertama Yang Dilakukan Setelah Memulai.<br>```--range``` Memungkinkan Anda Menentukan Rentang IP Khusus Misalnya.<br>: ```scan --range 192.168.178.1-192.168.178.40``` Atau Hanya ```scan``` Untuk Memindai Seluruh subnet.
| ```hosts (--force)``` | Menampilkan Semua Host/Perangkat Yang Sebelumnya Dipindai Dan Informasi Dasar.Menunjukkan ID Untuk Setiap Host Yang Diperlukan Untuk Interaksi.<br>```--force``` Memaksa Tabel Untuk Ditampilkan,Bahkan Ketika Tidak Muat Di Terminal.
| ```limit [ID1,ID2,...] [Rate] (--upload) (--download)``` | Membatasi Bandwidth Atau Host Yang Terkait Dengan ID Yang Ditentukan.Rate Menentukan Kecepatan Internet.<br>```--upload``` Membatasi Lalu Lintas Keluar Saja.<br>```--download``` Membatasi Lalu Lintas Masuk Saja.<br>Tarif Yang Valid: ```bit```, ```kbit```, ```mbit```, ```gbit```<br>Misalnya: ```limit 4,5,6 200kbit``` atau ```limit all 1gbit```
| ```block [ID1,ID2,...] (--upload) (--download)``` | Memblokir Koneksi Internet Host Yang Terkait Dengan ID Yang Ditentukan.<br>```--upload``` Membatasi Lalu lintas Keluar Saja <br>```--download``` Membatasi Lalu Lintas Masuk Saja.
| ```free [ID1,ID2,...]``` | Membuka Batasan/Blokir host Yang Terkait Dengan ID Yang Ditentukan.Menghapus Semua Pembatasan Lebih Lanjut.
| ```add [IP] (--mac [MAC])``` | Menambahkan Host Kustom Kedaftar Host. Alamat MAC Akan Diselesaikan Secara Otomatis Atau Dapat Ditentukan Secara Manual.<br>Misalnya: ```add 192.168.178.24``` atau ```add 192.168.1.50 --mac 1c:fc:bc:2d:a6:37```
| ```monitor (--interval [time in ms])``` | Memantau Penggunaan Bandwidth Dari Host Yang Dibatasi (Penggunaan Saat Ini,Total Bandwidth Yang  Digunakan).<br>```--interval``` Mengatur Interval Setelah Informasi Bandwidth Diperbarui Dalam Milidetik(default 500ms).<br>Misalnya: ```monitor --interval 1000```
| ```analyze [ID1,ID2,...] (--duration [time in s])``` | Menganalisis Lalu Lintas Host Tanpa Batasan Untuk Menentukan Siapa Yang Menggunakan Berapa Banyak Bandwidth.<br>```--duration``` Menentukan Durasi Analisis Dalam Detik(default 30s).<br>Misalnya: ```analyze 2,3 --duration 120```
| ```watch``` | Menampilkan Status Pemantauan Saat Ini.Fitur Pemantauan Mendeteksi Ketika Sebuah Host Terhubung Kembali Dengan Alamat IP Yang Berbeda.
| ```watch add [ID1,ID2,...]``` | Menambahkan Host Yang Ditentukan Ke daftar Pantauan.<br>Misalnya: ```watch add 6,7,8```
| ```watch remove [ID1,ID2,...]``` | Menghapus Host Yang Ditentukan Dari Daftar Pantauan.<br>Misalnya: ```watch remove all```
| ```watch set [Attribute] [Value]``` | Mengubah Pengaturan Pemantaun Saat Ini.Atribut Berikut Dapat Di Ubah:<br>```range``` Adalah Rentang IP Yang Akan Dipindai Untuk Koneksi Ulang.<br>```interval``` Adalah Waktu Tunggu Antara Setiap Pemindaian Jaringan (Dalam Detik).<br>Misalnya: ```watch set interval 120```
| ```clear``` | Membersihkan Jendela Terminal.
| ```quit``` | Menutup Aplikasi.
| ```?```, ```help``` | Menampilkan Informasi Perintah Yang Mirip Dengan ini

## Pembatasan

- **Membatasi Koneksi IPv4 Saja**, since [ARP spoofing](https://en.wikipedia.org/wiki/ARP_spoofing) Karena ARP Spoofing Memerlukan Paket ARP Yang Hanya Ada Di Jaringan IPv4

## Disclaimer
[Evil Limiter](https://github.com/shopeebjm/evillimiter) is provided by [shopeebjm](https://github.com/shopeebjm) "sebagaimana adanya" dan "dengan segala kekurangannya". Penyedia tidak memberikan pernyataan atau jaminan apa pun mengenai keamanan, kesesuaian, ketiadaan virus, ketidakakuratan, kesalahan tipografi, atau komponen berbahaya lainnya dari perangkat lunak ini. Terdapat bahaya yang melekat dalam penggunaan perangkat lunak apa pun, dan Anda sepenuhnya bertanggung jawab untuk menentukan apakah Evil Limiter kompatibel dengan peralatan Anda dan perangkat lunak lain yang terpasang pada peralatan Anda. Anda juga sepenuhnya bertanggung jawab atas perlindungan peralatan Anda dan pencadangan data Anda, dan penyedia tidak akan bertanggung jawab atas kerugian apa pun yang mungkin Anda derita sehubungan dengan penggunaan, modifikasi, atau pendistribusian perangkat lunak ini. 

## License

Copyright (c) 2019 by [shopeebjm](https://github.com/shopeebjm). Some rights reserved.<br>
[Evil Limiter](https://github.com/shopeebjm/evillimiter) is licensed under the MIT License as stated in the [LICENSE file](LICENSE).

# Social Media

<h2 align="center">

[![shopee](https://img.shields.io/badge/shopee-200%2B-yellow.svg?style=flat)](https://shopee.co.id/infinixnote40bjm)

[![Youtube shopee_banjarmasin](https://img.shields.io/badge/YouTube-200%2B-yellow.svg?style=flat)](https://www.youtube.com/@shopee_banjarmasin)

[![Instagram shopee_banjarmasn](https://img.shields.io/badge/Instagram-2K%2B-yellow.svg?style=flat)](https://www.instagram.com/shopee_banjarmasin)

[![Twitter KipyMacho](https://img.shields.io/badge/Twitter-350%2B-yellow.svg?style=flat)](https://www.twitter.com/shopeebjm)
  
[![Tiktok Shopeebjm](https://img.shields.io/badge/TikTok-80%2B-yellow.svg?style=flat)](https://www.tiktok.com/@shopee.bjm)

[![Facebook shopee.bjm](https://img.shields.io/badge/Facebook-199%2B-yellow.svg?style=flat)](https://www.facebook.com/shopee.bjm)

[![Telegram](https://img.shields.io/badge/Telegram-77%2B-yellow.svg?style=flat)](http://t.me/shopeebjm)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-80%2B-yellow.svg?style=flat)](http://www.linkedin.com/in/kiplymacho)

</p>
<div height='45' align="center">
<h2>Contact me: <br>
<a href="https://github.com/shopeebjm"> <img src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/github.svg" height='50'> </a>
<a href="https://facebook.com/shopee.bjm"> <img src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/facebook.svg" height='50'> </a>
  
<a href="https://paypal.me/kiplymacho"> <img src="https://cdn.trakteer.id/images/embed/trbtn-red-6.png" height='50'> </a>
</h2>
</div>

# Follow Me :
‎‎[![Messenger](https://img.shields.io/badge/Messengers-blue?style=for-the-badge&logo=messenger)](https://fb.me/shopee.bjm)
‎<a href="https://tiktok.com/@shopee.bjm"><img title="TikTok" src="https://img.shields.io/badge/-black?style=for-the-badge&logo=Tiktok"></a>
‎<a href="https://linktr.ee/kiplymacho" target="_blank"><img src="https://img.shields.io/badge/Socials-grey?style=for-the-badge&logo=linktree"></a>
‎<a href="https://github.com/shopeebjm" target="_blank"><img src="https://img.shields.io/badge/Github-blue?style=for-the-badge&logo=github"></a>
‎</p>
‎‎[![Instagram](https://img.shields.io/badge/Instagram-Follow-red?style=for-the-badge&logo=instagram)](https://instagram.com/shopee_banjarmasin)
‎[![Blog](https://img.shields.io/badge/Website-Visit-yellow?style=for-the-badge&logo=blogger)](https://kiplymacho.blogspot.com)
‎[![Facebook](https://img.shields.io/badge/Facebook-Like-red?style=for-the-badge&logo=facebook)](https://facebook.com/shopee.bjm)
‎[![HalamanFacebook](https://img.shields.io/badge/Halaman-Facebook-sky?style=for-the-badge&logo=facebook)](https://facebook.com/httpcustomkiplymacho)
‎[![WhatsApp](https://img.shields.io/badge/WhatsApp-red?style=for-the-badge&logo=whatsapp)](https://wa.me/6285751032225)
‎[![Telegram](https://img.shields.io/badge/Forum-Diskusi-blue?style=for-the-badge&logo=forum)](https://t.me/shopeebjm)
‎<a href="https://youtube.com/@shopee_banjarmasin"><img title="YouTube" src="https://img.shields.io/badge/YouTube-@Shopee_Banjarmasin-red?style=for-the-badge&logo=Youtube"></a>
