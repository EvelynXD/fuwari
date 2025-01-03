---
title: Observer Tools For Bug Bounty
published: 2022-07-07
description: 'Skrip ini membutuhkan banyak perbaikan, yang pasti akan saya tambahkan seiring waktu.'
image: 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj1OEgPBlZGcLTg9OuQ_d3P4_GnudeWbLuprUgyUZxIeeONq6OZF9db9XQeOlk0uRAr7PkXdF0TH4mTmNvTjj2J2D7mgRrNN0ogB4Zwr_Z7iD8t8KzaqlxVWT-AHbY854LC-vK-y-Apv4vIZsCl8r5goZzu5AWkOyujQkK1vi4hJI9YpbAawDv3Fy5AYZI/s1600-rw/bug-bounty.png'
tags: [Wireless Attack]
category: 'Technology'
draft: false 
lang: 'id'
---

Hai Internet, kali ini gw mau bahas tools yang lagi rame yaitu Layla, bukan layla mobel lejen jir.  
Layla adalah skrip python yang secara otomatis melakukan pengintaian pada URL yang diberikan. Ini menggabungkan output dari alat lain yang dikenal menjadi satu.

  

Cara Install
------------

Untuk mulai menginstall, pastikan anda menggunakan distro berbasis Debian, seperti Kali Linux, atau Ubuntu. Karena skrip menggunakan Python3 untuk dijalankan, penting untuk menginstalnya di mesin anda.

  

  
```bash
git clone https://github.com/mthf0/layla.git  

cd layla 

chmod +x install.sh & sudo ./install.sh  

python3 layla.py --url owasp.org

```
  

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjvhvTVJkPrnieKGqzKq8_ygK8aKHz3Jx2Zt_x2ffIGJFZsCb63xwIWaO8WmEQCuQXY7YGUDXRrsF12WM4KAPIffZHkvbsktiLq6XRnefPV-vpCM3rRNnbQzsjr7r2FRJJ9p0nqR_kfS2yuVT2UzowHOQ3-Rtmm9a4u_Unay1xaWHbPy5Mttc31WR-8AQ/s649-rw/image.png)

  

Fitur
-----

**Deteksi Firewall Aplikasi Web**
1.  [wafw00f](https://github.com/EnableSecurity/wafw00f "wafw00f")


  
**Pemindaian Port**
1.  [nmap](https://nmap.org/ "nmap")


  
**Deteksi Subdomain**
1.  [subfinder](https://github.com/projectdiscovery/subfinder "subfinder")
2.  [Sublist3r](https://github.com/aboul3la/Sublist3r "Sublist3r")
3.  [assetfinder](https://github.com/tomnomnom/assetfinder "assetfinder")
4.  [Amass](https://github.com/OWASP/Amass/ "Amass")


  
**Pemindai Directory**
1.  [dirsearch](https://github.com/maurosoria/dirsearch "dirsearch")

  

TODO
----

Skrip ini membutuhkan banyak perbaikan, yang pasti akan saya tambahkan seiring waktu. Saya akan mencantumkan beberapa di antaranya di bawah ini:

Sempurnakan beberapa parameter dari:

*   NMAP
*   AMASS

okoklah mungkin sekian aja pembahasan [Tool Pengintai/Pengamat Bug Bounty](https://eevelynxd.blogspot.com/2023/01/observer-tools-for-bug-bounty.html) semoga bermanfaat 😁