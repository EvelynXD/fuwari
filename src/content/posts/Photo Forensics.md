---
title: Photo Forensics：Melihat data rahasia pada suatu file image melalui metadata
published: 2022-07-03
description: 'Mencari Informasi Seseorang Di Internet Melalui Jejak Digital'
image: 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgRNwFzs5tutriCCATxXqNuwgcfq28eEPBS4ICTqFU_6v232EWvYzf1tcpK-C2-aVi6Vj857Arbu_YZP2SaKv-XFPpzwUWjuEyboAHUCRbbm3RzRqbqxF07psRP7xWtYJ22g6IBJQFAcyOaq3APv8jIJwsxIbyNzj0EaZJ-PUNy1bpnTt8e1UBhg9eRFPQ/s1600-rw/New%20Project%20%5B560704C%5D.png'
tags: [Osint]
category: 'Technology'
draft: false 
lang: 'id'
---

Hai Internet, pada kesempatan kali ini kita akan membahas teknik osint lagi, untuk penjelasan osint bisa di lihat pada artikel sebelumnya yaitu [Mencari Informasi Seseorang Di Internet Melalui Jejak Digital](https://eevelynxd.blogspot.com/2023/01/mencari-informasi-seseorang-di-internet.html) karena pembahasan artikel sebelumnya sama pembahasan yang ini tuh masih dalam satu tema yaitu tentang tools osint. okh, disini langsung aja kita bahas materi hari ini yaitu photo forensics.

Apa itu photo forensics
-----------------------

singkatnya photo forensics adalah teknik mencari data yang ada pada file image, seperti device apa yang mengambil foto, dimana foto itu di ambil, dan kapan fotonya diambil.  
Penjelasan lebih lanjut bisa baca di [suwitopoms.id](https://suwitopoms.id/tools-untuk-forensik-foto-atau-image/)  
Photo forensics sangat dibutuhkan sekarang, banyak foto AI yang bersebaran di internet, parahnya lagi ada yang mengira itu nyata apa lagi kalau masuk ke grup ibu-ibu langsung dah tuh kemakan howak.

Let's go!
---------

disini gw udh siapin 3 foto kita teliti satu per satu yh kita mulai baca data yang ada di file gambar pertama

![siapin 3 gambar](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjgdyj0TyZIuov_m_lR5fde-_IRDyw79KHdnUFNT4DXIwxPadD0z4c76IK2bXup-tdQxM7xjy8e_uX3lUEuxfoNbFhmBkUhN1QXWcKSqGdtdTf8FpHFmXq42947XinFR4xid8EkHIX0d2TPFfvQJReol1Z_a88GXml5gDyTZoFgowfJoWtWUZyyeWdUyx4/s1600-rw/siapin3gambar.png)

langsung aja kita masuk ke terminal favorit kalian, temen-temen bisa install toolsnya dulu di sini [Photo Forensics](https://github.com/Jieyab89/OSINT-Cheat-sheet)  

caranya kek biasa tinggal **git clone** terus masukin link githubnya contoh:  

> **git clone https://github.com/Jieyab89/OSINT-Cheat-sheet**  

disini nama toolsnya OSINT-Cheat-sheet install dulu aja sampai selesai, jika sudah masuk ke directorynya **OSINT-Cheat-sheet** setelah masuk ke directory langsung aja ketikan sintaksnya **exiftool** dan di ikuti dengan path file image yang akan kita baca metadatanya contoh:

```bash
$ exiftool /home/evelynxd/Downloads/1.jpg
```

Lalu enter, bisa kalian lihat disini dalam file image1.jpg banyak data yang muncul bisa dilihat dalam kasus ini terdapat nama device yang mengambil gambar tersebut dan waktu pada foto itu diambil.

![metadata](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi5hWfChemJ0vSN1rRDsswsbMUOo3-GdA4GTtTbzrxWUc9-PVJ1ME7pndezWD8-RqeXOvQCIczGdDzLgko6Jej_uyobYVjsecMBTRE1xApZbF4mIFfSKHWRt2a7T8z0LKCDVm4ghErmb7K_PkvbHfnpB6tMZbbdxQ8rWlH4iGW5ppMQs7WNRB9ofn-fZrs/s1600-rw/terminalSS.png)

```bash
ExifTool Version Number         : 12.64
File Name                       : 1.jpg
Directory                       : /home/evelynxd/Downloads
File Size                       : 379 kB
File Modification Date/Time     : 2023:08:02 06:08:42+07:00
File Access Date/Time           : 2023:08:02 06:13:05+07:00
File Inode Change Date/Time     : 2023:08:02 06:13:05+07:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Exif Byte Order                 : Big-endian (Motorola, MM)
X Resolution                    : 1
Y Resolution                    : 1
Resolution Unit                 : None
Modify Date                     : 2023:05:18 10:51:56
Y Cb Cr Positioning             : Centered
Copyright                       : fuafua2017
Exif Version                    : 0231
Date/Time Original              : 2023:05:18 10:51:56
Create Date                     : 2023:05:18 10:51:56
Components Configuration        : Y, Cb, Cr, -
Flashpix Version                : 0100
Color Space                     : Uncalibrated
GPS Version ID                  : 2.2.0.0
GPS Time Stamp                  : 01:31:09.6
GPS Img Direction Ref           : Magnetic North
GPS Img Direction               : 0
GPS Map Datum                   : WGS-84
GPS Date Stamp                  : 2023:05:18
Current IPTC Digest             : b9b64e1c74514b660ad71a1c99ec9f2a
Special Instructions            : FBMD2300096b0100005b650000cf8a00003dbe0000f5f001002e7802001b2f030074cc03002e59040030b70500
Application Record Version      : 4
Release Date                    : 2023:06:09
Release Time                    : 05:59:47+09:00
Time Created                    : 10:51:56+09:00
Copyright Notice                : fuafua2017
XMP Toolkit                     : Image::ExifTool 10.96
Rights                          : fuafua2017
Date/Time Digitized             : 2023:05:18 10:51:56.00
Date Created                    : 2023:05:18 10:51:56.00
Instructions                    : FBMD2300096b0100005b650000cf8a00003dbe0000f5f001002e7802001b2f030074cc03002e59040030b70500
Artist                          : fuafua2017
Image Width                     : 1080
Image Height                    : 1350
Encoding Process                : Progressive DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 1080x1350
Megapixels                      : 1.5
GPS Date/Time                   : 2023:05:18 01:31:09.6Z
GPS Latitude                    : 35 deg 43' 49.76" N
GPS Longitude                   : 139 deg 42' 54.50" E
Date/Time Created               : 2023:05:18 10:51:56+09:00
GPS Latitude Ref                : North
GPS Longitude Ref               : East
GPS Position                    : 35 deg 43' 49.76" N, 139 deg 42' 54.50" E


```

jika scroll lagi ke bawah maka kalian akan melihat data GPS nya dima foto itu diambil, kita coba copy koordinatnya langsung aja kita paste ke google maps hal pertama yag kita lakukan adalah mengganti **'deg'** ini menjadi simbol **(\[ ° \]degree symbol)** kalau udah tinggal enter kita search biar google maps cari lokasinya dimana.

***sebelum before:***
```bash
35 deg 43' 49.76" N, 139 deg 42' 54.50" E
```
***sesudah after***
```bash
35°43'49.76"N, 139°42'54.50"E
```

![metadata](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjKO-iK8CTeqdm-jmu3wyS2gYTO865rr-Ms6gUlzBG9I1TErIdc0bU5EkDd6gsSARyYbhYh8JYQrAUCLKhrp7EpxkBHDxpISx0EAzPtTymGi-MSQnWFN25KAX4rAyhZlF58vzkt5NuDVHtoaUWBg2VwtUC9ikCBrJV94iOMq6nR8cCi991w9sjLfjQE5lI/s1600-rw/jepang.png)

oke udah keliatan dari gambar tersebut bisa dipastikan foto itu diambil di [Higashiikebukuro, Toshima City, Tokyo 170-0013, Jepang](https://www.google.com/maps/place/35%C2%B043'49.8%22N+139%C2%B042'54.5%22E/@35.7304143,139.713564,419m/data=!3m1!1e3!4m4!3m3!8m2!3d35.7304889!4d139.7151389!5m1!1e4?entry=ttu) kemungikinan dia sedang berada di restoran lantai satu di outdoor karena pas gw research di lokasi itu terdapat restoran [MAD CHEFs マッドシェフ 池袋東口店](https://www.google.com/maps/place/MAD+CHEFs+%E3%83%9E%E3%83%83%E3%83%89%E3%82%B7%E3%82%A7%E3%83%95+%E6%B1%A0%E8%A2%8B%E6%9D%B1%E5%8F%A3%E5%BA%97/@35.7304946,139.7125605,17z/data=!3m1!4b1!4m6!3m5!1s0x60188d0c82b0f01f:0x6246f3fb3b6ee622!8m2!3d35.7304946!4d139.7151354!16s%2Fg%2F11kjg9tffy?entry=ttu)  
  
Lanjut ke gambar2.jpg ketikan ulang perintah yang sama seperti pada cara pertama tinggal arahkan ke file dua setelah itu enter.

```bash
$ exiftool /home/evelynxd/Downloads/2.jpg
```

Nah, ini bisa dilihat kalo datanya gak sebanyak seperti yang pertama tadi

```bash
ExifTool Version Number         : 12.64
File Name                       : 2.jpg
Directory                       : /home/evelynxd/Downloads
File Size                       : 78 kB
File Modification Date/Time     : 2023:08:02 04:29:51+07:00
File Access Date/Time           : 2023:08:02 04:30:14+07:00
File Inode Change Date/Time     : 2023:08:02 04:30:14+07:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 609e592a2c2f44334ac76a98742a87ee
Special Instructions            : FBMD23000965010000e92a00004b2b0000ba2b000011670000e88d000009ae0000b8e20000d706010051300100
Image Width                     : 1080
Image Height                    : 1080
Encoding Process                : Progressive DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 1080x1080
Megapixels                      : 1.2


```

kenapa?  
1. Karena filenya udah di compress sama si pemiliknya 
2. Atau hal kedua kemungkinan foto itu telah diedit pas diekspor metadata yang ada dalam foto itu kereset/kehapus (sudah tidak original lagi) atau hal ketiga 
3. foto itu udah tersebar luas, bagaimaa tuh kira-kira bisa sampai tersebar luas?

![osint](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhhdRKk6vCVXqfeU2Zl6hOwkFCiHwowfQgehWLtEzoNM79U9-ZOSAqecZVnutfhcEAKhip0LOCeYj_fvPniFyVCADYeZ1H8QXLlM6ugDyhEM9iaGcALHcBW3wJEyukqJLQ5K0wXqgckqugyE8wEpq3g5PVCGfAPpj9XuYhQRomULsJU4w6FxF2Jv5VLh34/s1600-rw/osint.png)

Mungkin pemilik telah mempostingnya ke facebook karena Facebook dapat mereset metadata exif termasuk lokasi foto itu diambil, lalu mengirim lagi ke WhatsApp dan WhatsApp itu mirip seperti Facebook dapat mereset metadata lalu di repost sama orang lain ke instagram, di Instagram gw kuranh tawu apakah sama seperti Facebook dan WhatsApp yang dapat mereset metadata yang ada dalam file image, buktinya semua gambar yang gw jadiin eksperimen ini semua berasal dari Instagram.  
  
Lanjut ke gambar yang terakhir..

![metadata](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEilwVer5qflnTlOklzruL_Ty3NowmCYONFQYJLj2Nxo4RQ5f-Ur13IvNRr_RaFkxRWItv5mcMSVsvUeCQei3ryfAG0DkIEKrHJFmUgYUSvZIYJz1_UQHOXmLJk144Md5aSTHq5-nzrW4sN4Cdlfe_klMpJxT6m3GB7l51DGUse5Yql9UZ4QRRomv_AesWs/s1600-rw/ss.png)

Nah, disini sama seperti hasil output yang pertama

```bash
ExifTool Version Number         : 12.64
File Name                       : 3.jpeg
Directory                       : /home/evelynxd/Downloads
File Size                       : 22 kB
File Modification Date/Time     : 2023:08:02 04:38:06+07:00
File Access Date/Time           : 2023:08:02 06:13:05+07:00
File Inode Change Date/Time     : 2023:08:02 06:13:05+07:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Exif Byte Order                 : Big-endian (Motorola, MM)
X Resolution                    : 96
Y Resolution                    : 96
Resolution Unit                 : inches
Modify Date                     : 2022:09:28 08:35:40
Y Cb Cr Positioning             : Centered
Exif Version                    : 0231
Date/Time Original              : 2022:09:28 08:35:40
Create Date                     : 2022:09:28 08:35:40
Components Configuration        : Y, Cb, Cr, -
Flashpix Version                : 0100
Color Space                     : Uncalibrated
GPS Version ID                  : 2.2.0.0
GPS Time Stamp                  : 04:21:02.4
GPS Img Direction Ref           : Magnetic North
GPS Img Direction               : 0
GPS Map Datum                   : WGS-84
GPS Date Stamp                  : 2023:08:02
Current IPTC Digest             : 9d418e1738430abca03b6c325917ce37
Province-State                  : Jawa Barat
Country-Primary Location Code   : IDN
Country-Primary Location Name   : Indonesia
Application Record Version      : 4
Release Date                    : 2023:08:02
Release Time                    : 04:36:32+07:00
Time Created                    : 08:35:40+07:00
XMP Toolkit                     : Image::ExifTool 10.96
Country Code                    : IDN
Date/Time Digitized             : 2022:09:28 08:35:40.00
City                            : Bogor
Country                         : Indonesia
Date Created                    : 2022:09:28 08:35:40.00
State                           : Jawa Barat
Artist                          : Maria Jesselyn Alvina
Comment                         : CREATOR: gd-jpeg v1.0 (using IJG JPEG v80), quality = 90.
Image Width                     : 191
Image Height                    : 255
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:4:4 (1 1)
Image Size                      : 191x255
Megapixels                      : 0.049
GPS Date/Time                   : 2023:08:02 04:21:02.4Z
GPS Latitude                    : 6 deg 34' 37.24" S
GPS Longitude                   : 106 deg 47' 26.67" E
Date/Time Created               : 2022:09:28 08:35:40+07:00
GPS Latitude Ref                : South
GPS Longitude Ref               : East
GPS Position                    : 6 deg 34' 37.24" S, 106 deg 47' 26.67" E


```

terdapat nama device yang mengabil foto dan koordinat lokasi foto itu diambil, oke kita lihat lagi lokasinya kita copy koordinatnya dari terminal lalu paste ke google maps dan seperti biasa jangan lupa untuk mengganti **deg** dengan **\[ ° \](degree/derajat)** lalu tekan enter dan boom wallaa...  

Lokasinya ada di bogor cuyy.. [Jl. Cimanggu Kecil 40-36, RT.01/RW.07, Ciwaringin, Kecamatan Bogor Tengah, Kota Bogor, Jawa Barat 16124](https://www.google.com/maps/place/6%C2%B034'37.2%22S+106%C2%B047'26.7%22E/@-6.5770111,106.7881668,780m/data=!3m2!1e3!4b1!4m4!3m3!8m2!3d-6.5770111!4d106.7907417!5m1!1e4?entry=ttu)

![metadata](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgObWMuadoQI6OY8aM2VV_V82xuFwJxPlp-fvoc3N4Iq0bqP_zuUVk9j3EwOdOvRpx9Gjc3pXrF1fk3LYWT3jkp4zkJ8kn1DKO9I_tM6aWJ2zQqCPi7HjlaoDqT7CQ0xmw5UlK28yJifSBfv0f8MPaW2aPXEZ09v2P8ixWRmu8QJEnXETI0t2wTQ_0XPmU/s1600-rw/bogor.png)

okh mungkin segini dulu yh untuk materi hari ini menuruku sih ini tools cukup mengerikan juga yah kalo udah mempelajari hal-hal kek gini terutama **osint** karena jejak digital itu sangat bebahaya, dari foto aja kita bisa tau lokasinya bagaimana kalo foto itu penting dan lokasinya itu rahasia, bisa aja dilacak makannya hati-hati juga si terutama ke pihak-pihak yang kurang jelas informasinya, kalian bisa tanya dahulu ""buat apa fotonya?" sama semisal kyak webinar gitu takutnya disalahgunakan atau ada hal-hal lain lah yang meminta foto bareng, foto kn sumber itu terpercaya takutnya disalahgunakan, sebenernya ada juga sih exiftool online kurang gw rekomendasikan karena kurang secure sih dan informasi yang didapat tudak akurat.  

Janga lupa share ke temen-temen kalian biar pada tau kalo post foto sebarangan bisa mendatangkan masalah, sebelum upload ke sosmed alangakh baiknya kalian compress foto tersebut.  
Atau kalian bisa baca postingan [cara menghapus meta data pada foto](https://fuwari-khaki.vercel.app/posts/reset-metadata-yang-ada-di-dalam-fotogambar/)  
  
okelah sekian pembahasan hari ini kali ada salah-salah kata mohon dimaafkan. 
