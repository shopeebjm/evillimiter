<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=YouTube+@shopee_banjarmasin" />
</p>
<p align="center">
<img src="https://readme-typing-svg.herokuapp.com?color=%2336BCF7&center=true&vCenter=true&lines=s+h+o+p+e+e+b+j+m" />
</p>

<p align='center'><a href="https://api.daily.dev/get?r=fisabiliyusri"><img src="https://raw.githubusercontent.com/fisabiliyusri/.github/main/kotori2.png?r=82s" width="150" alt="Hayuk"/></a></p>

<h2 align="center">
  
[![Powered By:shopeebjm](https://img.shields.io/badge/PoweredBy:shopeebjm-7%2B-blue.svg?style=flat)](http://shopee.co.id/infinixnote40bjm)

<img src="https://img.shields.io/badge/Version-1.0.0-blue.svg"></h2>

</p>

#
- Pasang Aplikasi Termux Di Android Tetapi Untuk Aplikasi Termux Jangan Di Unduh Di Playstore Karena Bisa Menyebabkan Error
<h2 align="center">

Unduh Aplikasi Termux Nya Dibawah Ini

👇👇

[![termux](https://img.shields.io/badge/termux-83%2B-yellow.svg?style=flat)](https://sfile.co/eZK8yBBtOiv)

<a href="https://play.google.com/store/apps/details?id=xyz.easypro.httpcustom">
<img alt="Get it on Google Play" src="https://play.google.com/intl/en_us/badges/images/generic/en_badge_web_generic.png" width="165" height="64" />
</a>

[![Android](https://img.shields.io/badge/Android-14-yellow.svg?style=flat)](https://developer.android.com/about/versions/14?hl=id)

<p align="center"><img src="https://i.imgur.com/CBGh0Yx.png" /></p>

# Evil Limiter

[![License Badge](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Compatibility](https://img.shields.io/badge/python-3-brightgreen.svg)](PROJECT)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity)
[![HitCount](http://hits.dwyl.io/bitbrute/evillimiter.svg)](http://hits.dwyl.io/bitbrute/evillimiter)
[![Open Source Love](https://badges.frapsoft.com/os/v3/open-source.svg?v=102)](https://github.com/ellerbrock/open-source-badge/)

A tool to monitor, analyze and limit the bandwidth (upload/download) of devices on your local network without physical or administrative access.<br>
```evillimiter``` employs [ARP spoofing](https://en.wikipedia.org/wiki/ARP_spoofing) and [traffic shaping](https://en.wikipedia.org/wiki/Traffic_shaping) to throttle the bandwidth of hosts on the network.

**Searching for a Windows-compatible version?**<br>
Check out the open-source alternative [EvilLimiter for Windows](https://github.com/bitbrute/evillimiter-windows).

## Requirements
- Linux distribution
- Python 3 or greater

Possibly missing python packages will be installed during the installation process.

## Installation

```bash
git clone https://github.com/bitbrute/evillimiter.git
cd evillimiter
sudo python3 setup.py install
```

Alternatively, you can download a desired version from the [Release page](https://github.com/bitbrute/evillimiter/releases).<br>

## Usage

Type ```evillimiter``` or ```python3 bin/evillimiter``` to run the tool.

```evillimiter``` will try to resolve required information (network interface, netmask, gateway address, ...) on its own, automatically.

#### Command-Line Arguments

| Argument | Explanation |
| -------- | ----------- |
| ```-h``` | Displays help message listing all command-line arguments |
| ```-i [Interface Name]``` | Specifies network interface (resolved if not specified)|
| ```-g [Gateway IP Address]``` | Specifies gateway IP address (resolved if not specified)|
| ```-m [Gateway MAC Address]``` | Specifies gateway MAC address (resolved if not specified)|
| ```-n [Netmask Address]``` | Specifies netmask (resolved if not specified)|
| ```-f``` | Flushes current iptables and tc configuration. Ensures that packets are dealt with correctly.|
| ```--colorless``` | Disables colored output |

#### ```evillimiter``` Commands

| Command | Explanation |
| ------- | ----------- |
| ```scan (--range [IP Range])``` | Scans your network for online hosts. One of the first things to do after start.<br>```--range``` lets you specify a custom IP range.<br>For example: ```scan --range 192.168.178.1-192.168.178.40``` or just ```scan``` to scan the entire subnet.
| ```hosts (--force)``` | Displays all the hosts/devices previously scanned and basic information. Shows ID for each host that is required for interaction.<br>```--force``` forces the table to be shown, even when it doesn't fit the terminal.
| ```limit [ID1,ID2,...] [Rate] (--upload) (--download)``` | Limits bandwidth of host(s) associated to specified ID. Rate determines the internet speed.<br>```--upload``` limits outgoing traffic only.<br>```--download``` limits incoming traffic only.<br>Valid rates: ```bit```, ```kbit```, ```mbit```, ```gbit```<br>For example: ```limit 4,5,6 200kbit``` or ```limit all 1gbit```
| ```block [ID1,ID2,...] (--upload) (--download)``` | Blocks internet connection of host(s) associated to specified ID.<br>```--upload``` limits outgoing traffic only <br>```--download``` limits incoming traffic only.
| ```free [ID1,ID2,...]``` | Unlimits/Unblocks host(s) associated to specified ID. Removes all further restrictions.
| ```add [IP] (--mac [MAC])``` | Adds custom host to host list. MAC-Address will be resolved automatically or can be specified manually.<br>For example: ```add 192.168.178.24``` or ```add 192.168.1.50 --mac 1c:fc:bc:2d:a6:37```
| ```monitor (--interval [time in ms])``` | Monitors bandwidth usage of limited host(s) (current usage, total bandwidth used, ...).<br>```--interval``` sets the interval after bandwidth information get refreshed in milliseconds (default 500ms).<br>For example: ```monitor --interval 1000```
| ```analyze [ID1,ID2,...] (--duration [time in s])``` | Analyzes traffic of host(s) without limiting to determine who uses how much bandwidth.<br>```--duration``` specifies the duration of the analysis in seconds (default 30s).<br>For example: ```analyze 2,3 --duration 120```
| ```watch``` | Shows current watch status. The watch feature detects when a host reconnects with a different IP address.
| ```watch add [ID1,ID2,...]``` | Adds specified host(s) to the watchlist.<br>For example: ```watch add 6,7,8```
| ```watch remove [ID1,ID2,...]``` | Removes specified host(s) from the watchlist.<br>For example: ```watch remove all```
| ```watch set [Attribute] [Value]``` | Changes current watch settings. The following attributes can be changed:<br>```range``` is the IP range to scan for reconnects.<br>```interval``` is the time to wait between each network scan (in seconds).<br>For example: ```watch set interval 120```
| ```clear``` | Clears the terminal window.
| ```quit``` | Quits the application.
| ```?```, ```help``` | Displays command information similar to this one.

## Restrictions

- **Limits IPv4 connctions only**, since [ARP spoofing](https://en.wikipedia.org/wiki/ARP_spoofing) requires the ARP packet that is only present  on IPv4 networks.

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

## Follow Me :

[![Messenger](https://img.shields.io/badge/Messengers-blue?style=for-the-badge&logo=messenger)](https://fb.me/shopee.bjm)
<a href="https://tiktok.com/@shopee.bjm"><img title="TikTok" src="https://img.shields.io/badge/-black?style=for-the-badge&logo=Tiktok"></a>
[![Instagram](https://img.shields.io/badge/Instagram-Follow-red?style=for-the-badge&logo=instagram)](https://instagram.com/shopee_banjarmasin)
[![Blog](https://img.shields.io/badge/Website-Visit-yellow?style=for-the-badge&logo=blogger)](https://kiplymacho.blogspot.com)
[![Facebook](https://img.shields.io/badge/Facebook-Like-red?style=for-the-badge&logo=facebook)](https://facebook.com/shopee.bjm)
[![HalamanFacebook](https://img.shields.io/badge/Halaman-Facebook-sky?style=for-the-badge&logo=facebook)](https://facebook.com/httpcustomkiplymacho)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-red?style=for-the-badge&logo=whatsapp)](https://wa.me/6285751032225)
[![Telegram](https://img.shields.io/badge/Forum-Diskusi-blue?style=for-the-badge&logo=forum)](https://t.me/shopeebjm)
<a href="https://youtube.com/@shopee_banjarmasin"><img title="YouTube" src="https://img.shields.io/badge/YouTube-@Shopee_Banjarmasin-red?style=for-the-badge&logo=Youtube"></a>
