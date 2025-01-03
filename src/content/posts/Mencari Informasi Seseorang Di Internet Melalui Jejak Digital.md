---
title: Mencari Informasi Seseorang Di Internet Melalui Jejak Digital
published: 2022-06-04
description: 'Dengan tools sherlock ini kita bisa menyelami seluruh dunia internet atau sosial media hanya dalam satu perintah/command'
image: 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhQD69mljcR6MwRsEMVDwtwdQSBfEh8xvebuUrBg0Fl8InmlqCpbD1QO3YPl_qtPZ4DBd1gvh61YpRBrS3296-_kXutSOIsI_Xt2wCx0iBnMZmL3eayY-4kC2Txi3IDv3Zcr49mQxrhPiCXMXKO5IyiV31m0gKhoKoyK9a2Ls4IDEBFNYOGdT4ocYLG4Qg/s1600-rw/sherlock.png'
tags: [Osint]
category: 'Technology'
draft: false 
lang: 'id'
---
  

Dengan tools sherlock ini kita bisa menyelami seluruh dunia internet atau sosial media hanya dalam satu perintah/command, cara kerjanya kita tinggal input dari username seseorang yang ingin kita investigasi lalu sherlock akan mencari seluruh sosial media yang ada di internet yang memiliki username yang kita input sebelumnya.

Hai internet, pada kesempatan kali ini gw akan membahas suatu tools/alat yang bernama Sherlock.

  

Apa itu Sherlock
----------------

Singkatnya sherlock adalah tools/alat yang diperuntukan melakukan suatu teknik yang bernama osint.  
lebih jelasnya [Penjelasan sherlock](https://student-activity.binus.ac.id/csc/2021/03/sherlock/#:~:text=Sherlock%20(sherlock%2Dproject)%20adalah,sosial%20media%20seseorang%20menggunakan%20username.)

  

Apa itu Osint
-------------

Osint memiliki singkatan yaitu _**open source intellegence**_ adalah suatu teknik yang dimana dilakukan dengan cara melakukan pengumpulan berbagai macam informasi yang berasal dari publik dan juga sumber yang terbuka.  
[Pengertian Osint](https://csirt.umm.ac.id/2022/06/apa-itu-osint-opent-source-intelligence/)

### Berbagai Macam Osint Tools Yang Populer:

1.  [Maltego](https://www.maltego.com/categories/osint/)
2.  [Sherlock](https://student-activity.binus.ac.id/csc/2021/03/sherlock/)
3.  [theHarvester](https://securitytrails.com/blog/theharvester-tool)

Osint bisa kita lakukan dengan tujuan yang baik ataupun tujuan yang buruk.

### Tujuan baik:

misal kita kan punya hasil dari osint ini, kita akan menemukan banyak informasi dari seseorang yang coba kita investigasi.  
Nah, kalo kita menemukan sesuatu hal-hal yang bersifat privasi, dan orang ini umbar diinternet kita bisa kasih tau ke orangnya dan bilang kalo ini udah kelwatan batas ini tuh gaboleh diumbar-umbar karena ini adalah privasi karena takutnya nani bisa disalahgunakan. sebagai contoh, mungkin sebelumnya ada yang menggunakan nama temen lu (misal) si ujang, nah si ujang ini gk ngerasa kalo menyebarkan informasi pribadinya di internet, kita bisa bantu dia menggunakan tools yang bernama sherlock ini apakah ada orang lain yang menyebarkan informasi dirinya di initernet?.

### Tujuan buruk:

*   Menjual data pribadi secara ilegal
*   Penyalahgunaan data informasi seseorang
*   Penipuan menggunakan data pribadi seseorang

Kenapa Sherlock
---------------

Alasan saya memilih atau menggunakan tools/alat ini untuk mempelajari teknik osint. Dengan tools sherlock ini kita bisa menyelami seluruh dunia internet atau sosial media hanya dalam satu perintah/command, cara kerjanya kita tinggal input dari username seseorang yang ingin kita investigasi lalu sherlock akan mencari seluruh sosial media yang ada di internet yang memiliki username yang kita input sebelumnya.  
Untuk stalker cocok nih tools yang satu ini, mungkin mau cari nomor whatsapp kosplayer atau idola.  
  
Contoh kita akan mencari dengan nama **"ujang"** misalnya, kita tinggal input username **"ujang"** lalu sherlock ini akan mencari semua sosial media di internet dengan username **"ujang"**

```bash
$ Input Username: Ujang

https://www.instagram.com/ujang
https://www.youtube.com/c/@ujang
https://www.twitter.com/ujang
https://www.tiktok.com/ujang
https://www.twitch.tv/ujang
https://www.github.com/ujang
https://www.spotify.com/ujang

```
  

kurang lebih gitu, okh sebelum prakteknya kita instalasi dulu ya.

Installasi
----------

Installasi tinggal ke github [sherlock-project](https://github.com/sherlock-project/sherlock)  
Pertama kita butuh git bash untuk cloning repository dari github ke directory laptop/pc kita, jika kalian menggunakan linux tidak perlu menginstall gitbash karena sudah pre-install di kali linux.

```bash
$ git clone https://github.com/sherlock-project/sherlock.git
```

Setelah itu masuk ke directory sherlock dengan mengetikan **'cd sherlock'** lalu install requirementsnya pake command/perintah **'python3'**

```bash
$ python3 -m pip install -r requirements.txt
```

Kenapa pake python3, karena sherlock ini berbasis python maka penggunaannya pun harus pake perintah python3 diawal, dan temen-temen bagi yang pake linux gak perlu install python3 lagi karena ini emang udah pre-install di kali linux jadi gak usah install lagi.  
  
Jika sudah diinstall maka yang kita lakukan selanjutnya adalah mengeksekusi scriptnya dengan memasukann perintah:

```bash
$ python3 sherlock ujang
```

Nantinya sherlock akan mencari keseluruhan data yang ada di internet atau sosial media dengan nama ujang.  
Nah, dari sini kita bisa tau nih si ujang kerjanya apa dan ngapain aja di internet.

[![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjhsag2cEajSbyfmUIS5nDc4cbWb2KU4B1cSKkMX9qlKDnc8ecYYc2KrGvsF4Rj7XI84QyZTa1nvhXqSsy8iFVkUSxbDCWW-Afriy6LVgX3spRkVDLHL2TflS_ToQ7VuIrCIBzOWX8e3MYMIEoP7mQaRAK4pmWz8h_vOU21xlbsblNCMtuQZ0byzo3KcAo/s1600/ujang.png)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjhsag2cEajSbyfmUIS5nDc4cbWb2KU4B1cSKkMX9qlKDnc8ecYYc2KrGvsF4Rj7XI84QyZTa1nvhXqSsy8iFVkUSxbDCWW-Afriy6LVgX3spRkVDLHL2TflS_ToQ7VuIrCIBzOWX8e3MYMIEoP7mQaRAK4pmWz8h_vOU21xlbsblNCMtuQZ0byzo3KcAo/s1600/ujang.png)

Melihat laporan hasil investigasi sherlock
------------------------------------------

Di sherlock kita juga bisa melihat hasil laporan tanpa harus mengetikan ulang perintah.

[![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhFySPnO28OqU2A1xozM9J0eUizOeaQ_daC6lHXSRmcXXHIq2Qr7oo7Mb4YqSX4ZL3HQ7yLLpPqbUV7C9nRfpTePOt72U0XskMIg0yJUok3mNHcP1cWz_NnZ62aJNj5fJoOUDl4smJUsJ1Li3cL6iz4JsRnYhxpRjZIfW8mtMm1LD993jRKI9TEbN2A140/s1600/laporanUjang.png)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhFySPnO28OqU2A1xozM9J0eUizOeaQ_daC6lHXSRmcXXHIq2Qr7oo7Mb4YqSX4ZL3HQ7yLLpPqbUV7C9nRfpTePOt72U0XskMIg0yJUok3mNHcP1cWz_NnZ62aJNj5fJoOUDl4smJUsJ1Li3cL6iz4JsRnYhxpRjZIfW8mtMm1LD993jRKI9TEbN2A140/s1600/laporanUjang.png)

Okh jadi sekian pembahasan kali ini, mohon maaf kalo ada salah-salah kata.  

<!-- Source:  
https://student-activity.binus.ac.id/  
https://csirt.umm.ac.id -->